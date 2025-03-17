### Modificar sus propiedades

A pesar de que los [[J7 Objetos|objetos]] se definen con [[J4 Variables Const|const]], podemos modificar sus propiedades, a diferencia de una variable.

La forma de hacerlo es la siguiente:

````JS
const producto = {
	nombre: "Tablet",
	precio: 300,
	disponible: true
}

// Reescribir un valor
producto.nombre = "Monitor Curvo"
````

### Añadir propiedades

Además, podemos añadir propiedades que no existan en nuestro objeto. Esto lo podemos hacer agregando una propiedad que no exista en el objeto:

````JS
const producto = {
	nombre: "Tablet",
	precio: 200,
	disponible: true
}

// Si no existe, lo va a añadir
producto.imagen = "imagen.jpg"
````

### Eliminar propiedades

Para eliminar una propiedad, podemos utilizar el método ``delete``:

````JS
const producto = {
	nombre: "Tablet",
	precio: 200,
	disponible: true
}

delete producto.disponible
````

Pero, ¿qué pasaría si eliminamos una propiedad que no existe?, pues simplemente nada, [JS](https://developer.mozilla.org/es/docs/Glossary/JavaScript) no nos mostrará ningún error.

### Proteger un objeto

Si queremos proteger nuestro objeto para que no lo podamos modificar, podemos usar el método ``freeze``:

````JS
const producto = {
	nombre: "Tablet",
	precio: 200,
	disponible: true
}

Object.freeze(producto)
````

También podemos usar ``seal``:

````JS
const producto = {
	nombre: "Tablet",
	precio: 200,
	disponible: true
}

Object.seal(producto)
````

lo diferente de ``seal`` a ``freeze``, es que ``seal`` si permite modificar las propiedades, pero no deja añadir o eliminarlas.