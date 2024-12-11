Metadata:
Fecha: 25-08-2023
Hora: 08:13
Título: Breve introducción a R.

## Apunte.
---
- ``R`` es un programa útil para el análisis y visualización de datos. Es abierto y gratuito.
- Es un lenguaje interpreta y tipado.
- Fue creado por Ross Ihaka y Robert Gentle-man.


### Instalación de ``R``.
---
Descargar ``R`` [aquí](https://cran.r-project.org/)
Descargar ``R Studio`` [aquí](https://posit.co/download/r-studio-desktop/)


### Reglas de sintaxis.
---
- ``R`` distingue entre mayúsculas y minúsculas.
- Los nombres de las variables pueden contener letras, números y puntos. Sin embargo, deben comenzar con una letra y no pueden contener espacios.


#### Nombres de variables correctos.
---
``monto_total<-1200``
``monto_mensual<-200``

#### Nombres de variables incorrectos.
---
``montoTotal<-1200``
``MontoMensual<-200``

- Usar espacios alrededor de todos los operadores binarios (=, +, -, <-, etc) y un espacio después de una coma.


### Ayuda.
---
````R
help(mean)
? mean
````


### Tipos de datos.
---
**Enteros, numéricos y complejos**.
- ``entero<-1L``
- ``numerico<-1``
- ``complejo<-3+4i``
- ``booleano<-TRUE``
- ``print(entero,str(entero))``


Continuación en [[Continuación de la introducción a R.]]
