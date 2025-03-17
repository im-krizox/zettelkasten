
## Notación.

Se usa la siguiente notación de manera formal:
$$C=E(P)\ \text{y}\ P=D(C)$$
Donde $C$ es el *ciphertext*, $E$


## Algoritmos de Encriptación

El criptosistema involucra un conjunto de reglas para encriptar un *plaintext* y para desencriptar un *ciphertext*.

Este conjunto de reglas es llamado algoritmo, el cual frecuentemente usa un dispositivo llamado *key* (llave), denotado por $K$, de manera que el *ciphertext* resultante depende del mensaje original

En algunos casos, la llave (*key*) para encriptar es la misma que se usa para desencriptar. A estos algoritmos se les llama simétricos, dado que los procesos $E$ y $D$ son imágenes espejo uno de otro. Esto es:
$$P=D(K,E(K,P))$$
>[!quote] Algoritmo simétrico

En otras ocasiones, las llaves para encriptar y desencriptar vienen en pares, por lo que la llave de desencriptación $K_D$ invierte a la llave de encriptación $K_E$. Esto es:
$$P=D(K_P)$$
>[!Quote] Algoritmo asimétrico

Recordemos que $E$ es un conjunto de algoritmos y la llave $K$ selecciona un algoritmo específico para el conjunto. Esto es, podemos tener diferentes encriptaciones (*ciphertexts*) de un mismo *plaintext* usando el mismo algoritmo pero una llave diferente.

Más aún, usar una llave da seguridad adicional, dado que si un mensaje cae en manos de un intruso, si este no tiene la llave no podrá conocer otros mensajes.

Un criptoanalista estudia algoritmos de encriptación y mensajes encriptados para tratar de hallar el mensaje escondido.


## Criptoanálisis

El objetivo de un criptoanalista es romper la encriptación. Esto es, obtener el mensaje original de un *ciphertext*. Más aún, trata de determinar que algoritmo de desencriptación combina con el algoritmo de encriptación de manera que otros mensajes codificados de la misma manera puedan ser leídos.

>[!Quote] Principio de Kerckhoff
>Un cripstosistema debe ser seguro aún si el atacante (Eva) conoce todos los detalles acerca del sistema, con excepción de la llave secreta. En particular, el sistema debe ser seguro cuando el atacante conoce los algoritmos de encriptación y desencriptación.

## Longitud de la llave

La discusión de la longitud de la llave en sistemas simétricos es sólo relevante sólo si el ataque de fuerza bruta es el mejor ataque conocido.

Si un análisis analítico se puede llevar a cabo, entonces no importe el largo de la llave. Lo mismo sucede si se puede llevar un ataque de ingeniería social.

Una condición necesaria, pero no suficiente, para un sistema simétrico seguro es un espacio grande de llaves.

Además el sistema debe ser fuerte contra ataques analíticos.

| **Longitud de la llave** | ****                                    |
| ------------------------ | --------------------------------------- |
| 56-64 bits               | Corto plazo: Unas horas hasta unos días |

Casi todos los algoritmos criptográficos, tanto simétricos como asimétricos, están basados en aritmética con un número finito de elementos.

La aritmética modular es una manera simple de hacer aritmética en un conjunto finito de números enteros.

Consideremos el conjunto siguiente de $9$ números: $\{0,1,2,3,4,5,6,7,8\}$.

Podemos hacer aritmética regular: $2\times3=6;\ 4+4=8$, pero que pasa si sumamos $8+4$?

Seguimos la siguiente regla: hacer aritmética regular y dividimos el resultado entre $9$ y consideramos sólo el residuo 

>[!info] Definición.
>Sean $a,r,m\in\mathbf{Z}$ (donde $\mathbf{Z}$ es el conjunto de los enteros) y $m>0$. Escribimos
>$$a\equiv r\text{ mod }m$$
>Si $m$ divide $a-r$.
>$m$ es llamado módulo y $r$ es llamado residuo.

## ¿Qué residuo debemos escoger?

Escogemos un residuo $r$ tal que $0\leq r<m$





