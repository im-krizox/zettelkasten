Integrantes:
- Baeza Guerrero Roberto
- Van Steemberghe Luján Kristoffer


Para nuestro proyecto utilizaremos [MongoDB](https://www.mongodb.com/), la cual es una base de datos NoSQL.

### Proceso de conexión

Primero creamos nuestra base de datos con el servicio de MongoDB llamado Atlas y la enlazamos a una herramienta llamada Compass para facilitar la manipulación y configuración de esta.

![[Pasted image 20240422110321.png]]
*Imagen de conexión de la herramienta Compass*

![[Pasted image 20240422110409.png]]
*Imagen de la interfaz de Compass*


### Conexión de la base de datos con el Backend

Para la manipulación de los datos utilizaremos [GraphQL](https://graphql.org/). La forma en que conectamos la base de datos al backend es con [Mongoose](https://mongoosejs.com/) que es una biblioteca de modelado de datos orientada a objetos (ODM) para MongoDB y Node.js.

![[Pasted image 20240422110718.png]]
*Código de la función que conecta la base de datos al backend*

>[!Tip]
>Cabe resaltar que el enlace para conectarse a la base de datos se encuentra en un archivo .env que por cuestiones de seguridad no se puede mostrar.


### Conexión de la base de datos con el Frontend

Para conectar la base de datos al frontend debemos de hostear el backend en un servidor local o en uN VPS (en nuestro caso lo hosteamos en [Render](https://render.com/)), y agregar el enlace que nos devuelva nuestro hosting y colocarlo en la configuración del frontend con el cliente que elijamos (en nuestro caso [Apollo Server](https://www.apollographql.com/docs/apollo-server/getting-started/) ya que este mismo permite utilizar GraphQL).

![[Pasted image 20240422111429.png]]
*En la paete de la uri es donde ponemos el enlace del hosting del backend*


### Hosting de la base de datos

Como lo mencionamos anteriormente la base de datos se encuentra hosteada con el servicio de Atlas que el propio MongoDB ofrece.