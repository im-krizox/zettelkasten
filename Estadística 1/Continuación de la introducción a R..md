Metadata:
Fecha: 28-08-2023
Hora: 07:50
Título: Continuación de la introducción a R.

Continuación de [[Breve introducción a R.]]


## Operadores aritméticos.
- Suma (``+``)
- Resta (``-``)
- Multiplicación (``*``)
- División (``/``)
- División entera (``%/%``)
- Módulo (``%%``)
- Exponente (``^``)
### Ejemplo.
Ejemplo con 
```R
>31.65%/%780
>4
```


## Operadores de asignación.
```R
valor_1<-5 ✅
valor_2=6 ❌
7->valor_3 ❌
```


## Operadores de comparación e identidad.
- Menor (``<``)
- Mayor (``>``)
- Menor o igual (``<=``)
- Mayor o igual (``>=``)
- Igual (``==``)
- Distinto (``!=``)

### Ejemplo.
```R
5>9
False
7!=8
True
```


## Funciones para cadenas de texto.
- ``paste()`` concatena varias cadenas en una sola cadena.
- ``rep()`` repite un objeto o $n$ cantidad de veces.
- ``grepl()`` busca un patrón en una cadena de texto y devuelve un vector lógico.
- ``regexpr`` busca un patrón en una cadena y devuelve la posición
- ``nchar()`` devuelve la longitud de una cadena
### Ejemplo.
```R
cadena_1 <- "Hola"
cadena_2 <- "estoy mejorando"
paste(cadena_1,cadena_2,sep=",")
"Hola,estoy mejorando"
rep(cadena_1, 3)
"Hola" "Hola" "Hola"
```


## Convertir tipo de dato.
- ``as.integer()``
- ``as.numeric()``
- ``as.complex()``
- ``as.factor()``
- ``as.logical()``


## Estructura de datos.

### Vector.
- ``vector_entero <- 1:10``
- ``vector_cadena <- c("manzana","uva")``
- ``vector_logico <- c(TRUE,FALSE)``

#### Ejemplo.
```R
vector <- c(1,"manzana")
"1" "manzana"
```

### Listas.
- ``lista <- list(1,"manzana")

### Matrices.
- ``matriz_1 <- matrix(1:10,nrow=2,ncol=5)``

**Representación:**
$$\begin{matrix} \text{matriz\_1}\\ &\text{[,1]}&\text{[,2]}&\text{[,3]}&\text{[,4]}&\text{[,5]} \\ \text{[1,]}&1&3&5&7&9\\ \text{[2,]}&2&4&6&8&10 \end{matrix}$$

#### Ejemplo.
```R
matriz_1[1, ] #Fila 1
matriz_1[ ,5] #Columna 5
matriz_1[2,3] #Devuelve 6
```


## Data Frame.
```R
data_frame <- data.frame (
	"entero" = 1:4,
	"texto" = c("a", "b", "c", "d")
	"numerico" = c(1.1, 1.2, 1.3, 1.4)
)
```

**Representación:**

| entero | texto | numerico |
| --- | --- | --- |
| 1 | a | 1.1 |
| 2 | b | 1.2 |
| 3 | c | 1.3 |
| 4 | d | 1.4 |
``data_frame $entero``

### Funciones con Data Frames.
- ``str()``
- ``head()``
- ``tail()``
- ``summary()``


## Estructuras de control.

### Estructuras condicionales.
- ``if``
```R
numero <- 10
if (numero %% 2 === 0) {
	print("El número es par")
} else {
	print("El número es impar")
}
```

- ``for``
```R
for (i in 1:10) {
	print(i * 2)
}
```

- ``while``
```R
numero <- 5
fin <- 0
while (numero > fin) {
	numero <- numero-1
	print(numero)
}
4
3
2
1
```





