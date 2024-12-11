
Para la autenticación de usuarios usaremos la API llamada JSON Web Token.


Para esto, en el backend creamos un nuevo ``Mutation``, llamado

![[Pasted image 20240510190010.png|500]]

el cual nos va a regresar un ``Token``

![[Pasted image 20240510190116.png|500]]

y le pasaremos el input ``AutenticarInput``

![[Pasted image 20240510190156.png|500]]



## Definición del Mutation

Para definir nuestro ``Mutation`` necesitamos importar lo siguiente:

![[Pasted image 20240510190644.png|500]]

- *bcryptjs* nos servirá para comparar una contraseña almacenada en la base de datos con la contraseña ingresada por el usuario.
- *jwt* nos ayudará a crear los JSON Web Tokens.
- *variables.env* contendrá la palabra secreta con la que se firmarán los tokens.


Creamos la función para crear y firmar los tokens:

![[Pasted image 20240510190836.png|500]]


Nuestro ``Mutation`` quedaría de la siguiente forma:

![[Pasted image 20240510190326.png]]

De esta forma, usamos JSON Web Tokens para la autenticación de los usuarios y la búsqueda de estos mismos en la base de datos.


### Aplicación del JSON Web Token

Este JSON Web Token lo guardaremos en el *local storage* del navegador:

![[Pasted image 20240510191705.png]]

![[Pasted image 20240510191723.png]]

al momento de copiar este token y pegarlo en la web de la API ([jwt.io](https://jwt.io/)) podemos descifrar la información que este contiene:

![[Pasted image 20240510191838.png]]
