Metadata:
Fecha: 30-08-2023
Hora: 07:28
Título: Funciones en R.

Seguimiento de [[Breve introducción a R.]] y [[Continuación de la introducción a R.]], [[Herramientas.]].

## Funciones.
Sintaxis:
```R
nombre_funcion <- function(argumentos) {
	operaciones
	return(resultado)
}
```

### Ejemplo de función.
```R
area_rect <- function(largo, ancho) {
	area <- largo*ancho
	return(area)
}
```

**Sugerencia:** Intentar hacer el ejemplo con 
``area_rect(largo=10, ancho=5)``.