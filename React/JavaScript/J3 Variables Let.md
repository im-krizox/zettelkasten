[JS](https://developer.mozilla.org/es/docs/Glossary/JavaScript) es un lenguaje de [tipo dinámico](https://developer.mozilla.org/es/docs/Glossary/Dynamic_typing), por lo que una variable puede contener diferentes tipos de dato, porque el tipo de dato se almacena en el valor de la variable y no en la variable como tal.

###### Ejemplo

````JS
let cliente = "Juan"
console.log(cliente)
````

A diferencia de otros lenguajes, en [JS](https://developer.mozilla.org/es/docs/Glossary/JavaScript) no es necesario definir el tipo de dato de la variable. En JS puedes definir las variables de la siguiente forma:

````JS
let cliente = "Juan"
let edad = 22
````

Al momento de mandar imprimir nuestras variables

````JS
console.log(cliente)
console.log(edad)
````

las variables de tipo String estarán de color negro, mientras que las variables de tipo número serán azules.

## Características de las variables ``let``
- Se pueden reasignar
- Pueden iniciar sin un valor
- [Camel case](https://es.wikipedia.org/wiki/Camel_case)

### Reasignar variables

Como mencionamos anteriormente, en [JS](https://developer.mozilla.org/es/docs/Glossary/JavaScript) una variable puede tener distintos tipos de datos, esto se hace reasignándole su valor:

````JS
let cliente = "Juan"

// Reasignamos el valor de la variable cliente
cliente = 20

console.log(cliente)
````

y la respuesta que obtenemos es ``20``.

### Iniciar una variable sin un valor

En [JS](https://developer.mozilla.org/es/docs/Glossary/JavaScript) podemos declarar nuevas variables sin la necesidad de asignarles un valor en ese momento:

````JS
let precio
console.log(precio)
````

la respuesta que obtendríamos sería ``undefined``.

Una vez que se vaya ejecutando el programa podemos ya asignarle un valor:

````JS
let precio
precio = 1000
console.log(precio)
````

la consola nos mostraría ``1000``.

### Camel case

En las variables de [JS](https://developer.mozilla.org/es/docs/Glossary/JavaScript) se usa una buena práctica llamada [camelCase](https://es.wikipedia.org/wiki/Camel_case), la cual al momento de definir una variable de dos palabras, la primera inicia con minúscula y la segunda con mayúscula:

````JS
let precioDescuento = 220 // Usamos camelCase en la variable
````

De igual forma, si la variable contiene 3 palabras, la tercera también iniciaría con mayúscula

````JS
let precioDescuentoTemporada = 500 // camelCase
````
