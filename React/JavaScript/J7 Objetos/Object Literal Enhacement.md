El [Object Literal Enhacement](https://medium.com/@narenss/es6-enhanced-object-literals-bbae848e1750) permite colocar distintas variables en un objeto (prácticamente es el contrario al [[Destructuring|destructuring]]).

##### Ejemplo

````JS
const autenticado = true
const usuario = "Kris"

const nuevoObjeto = {
	autenticado: autenticado,
	usuario: usuario
}
````

>[!tip] Importante. 
>Cuando la variable y el valor es el mismo, podemos deshacernos del lado derecho:
>````JS
>	const nuevoObjeto = {
>		autenticado,
>		usuario
>	}
>````

