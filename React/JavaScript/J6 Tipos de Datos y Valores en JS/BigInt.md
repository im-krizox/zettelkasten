En [JS](https://developer.mozilla.org/es/docs/Glossary/JavaScript), [[BigInt]] es un tipo de dato numérico que puede representar números enteros en el [formato de precisión arbitrario](https://en.wikipedia.org/wiki/Arbitrary-precision_arithmetic).

##### Ejemplo

````JS
const numeroGrande = BigInt(864786598365)
````

>[!tip] Importante.
>No se puede mezclar datos de tipo ``Number`` con ``BigInt``, por ejemplo:
>````JavaScript
>const numero = 20
>const numeroGrande = BigInt(247398579807)
>console.log(numero + numeroGrande)
>````
>la respuesta que obtendríamos sería un error.

En [JS](https://developer.mozilla.org/es/docs/Glossary/JavaScript) existe un término que se llama [coerción](https://developer.mozilla.org/es/docs/Glossary/Type_coercion), que es donde básicamente con una función cambiamos el tipo de dato de una variable.

De esta forma, siguiendo el ejemplo anterior, podría solucionarse de la siguiente forma:

````JS
const numero = 20
const numeroGrande = BigInt(247398579807)
console.log(numero + Number(numeroGrande))
````

Más info [aquí](https://developer.mozilla.org/es/docs/Glossary/BigInt).