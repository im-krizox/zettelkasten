Una estructura sin datos. Esta simplemente es una forma abreviada para funciones, aunque cada constructor de funciones se deriva del constructor ``Object``.

##### Ejemplo

````JS
function sumar(a, b) {
	return a + b;
}

// Asignando la función a una variable
const suma = sumar

//Invocando la función
const resultado = suma (2,3);
````

Más info [aquí](https://developer.mozilla.org/es/docs/Glossary/Function).