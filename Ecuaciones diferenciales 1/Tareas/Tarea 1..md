Metadata:
Fecha: 23-08-2023
Hora: 16:11
Título: Tarea 1.

## Ejercicio 4.
---
**Instrucciones:** Establecer el orden de la ecuación diferencial ordinaria dada y determinar si la ecuación es lineal o no lineal.
$$\frac{d^2u}{dr^2}+\frac{du}{dr}+u=cos(r+u)$$

###### Solución.
Primero, hay que identificar el orden de la ecuación diferencial. Como vimos en clase, el orden de una ecuación diferencial se refiere a la derivada de mayor orden presenta en la ecuación. En este caso la derivada mayor es $\frac{d^2u}{dr^2}$, por lo que la ecuación es de segundo orden.

Ahora, se tiene que determinar si la ecuación es lineal o no lineal.
En la ecuación dada, hay términos como $\frac{d^2u}{dr^2}$, $\frac{du}{dr}$ y $u$, que son derivadas y la función $u$ está elevada a la potencia $1$. Todo bien con eso, sin embargo, el término $\cos(r + u)$ rompe la linealidad, ya que involucra la función trigonométrica $\cos$.

$\therefore$ **La ecuación diferencial es de 2° orden y no lineal**.


## Ejercicio 8.
---
**Instrucciones:** Establecer el orden de la ecuación diferencial ordinaria dada y determinar si la ecuación es lineal o no lineal.
$$\ddot{x}-\Big(1-\frac{\dot{x}^2}{3}\Big)\dot{x}+x=0$$

###### Solución.
En la ecuación diferencial, $\ddot{x}$ representa la segunda derivada de $x$ con respecto al tiempo.

Primero, hay que identificar el orden de la ecuación diferencial. En este caso, la derivada mayor es de segundo orden $\ddot{x}$, por lo que la ecuación es de segundo orden.

La presencia de productos o cocientes de las derivadas no afecta la linealidad, siempre y cuando las derivadas no estén elevadas a potencias diferentes de 1 ni multiplicadas por funciones que dependan de la variable dependiente $x$. En este caso, la expresión $\left(1 - \frac{\dot{x}^2}{3}\right)\dot{x}$ puede parecer complicada, pero sigue siendo lineal, ya que la derivada $\dot{x}$ se multiplica por una función que depende solo del tiempo y no de la función $x$.

Por lo tanto, la ecuación diferencial dada es lineal debido a que todos los términos involucrados son combinaciones lineales de las derivadas y la función $x$.

$\therefore$ **La ecuación diferencial es de segundo orden y lineal**.


## Ejercicio 14.
---
**Instrucciones:** Comprobar que la función indicada es una solución de la ecuación diferencial dada. Suponga un intervalo $I$ de definición adecuado para cada solución.
$$y''+y=\tan x;\ \ \ y=-(\cos x)\ln(\sec x+\tan x)$$

###### Solución.
Para verificar que la función dada $y = -(\cos x)\ln(\sec x+\tan x)$ es una solución de la ecuación diferencial $y'' + y = \tan x$, necesitamos comprobar dos cosas:
1. La función $y$ y sus derivadas hasta segundo orden existen en el intervalo $I$.
2. Sustituir $y$ y sus derivadas en la ecuación diferencial resulta en una identidad verdadera.

Entonces, procedemos con la solución:
1. **Existencia de las derivadas:**
La función $y$ y sus derivadas están compuestas de funciones elementales y logaritmos naturales. Estas funciones son continuas y derivables en intervalos que excluyen los puntos donde el denominador en el logaritmo sea igual a cero ($\sec x + \tan x \neq 0$, lo cual equivale a $\cos x \neq 0$). En términos prácticos, esto significa que el intervalo $I$ debe excluir valores de $x$ tales que $\cos x = 0$, es decir, $x = \frac{\pi}{2} + k\pi$ para algún entero $k$. Por lo tanto, $I$ puede ser cualquier intervalo que no contenga esos valores.

2. **Verificación de la ecuación diferencial:**
Calcularemos las derivadas de $y$ necesarias y luego sustituiremos en la ecuación diferencial $y'' + y = \tan x$ para verificar si se cumple.

La función dada es: $$y=-(\cos x)\ln(\sec x+\tan x)$$
Después calculamos la primera y segunda derivada: $$\begin{align*} y'&=\cos x\cdot\frac{\sec x\tan x+\sec^2 x}{\sec x+\tan x}+(\cos x)\ln(\sec x+\tan x)\\ y''&=-\sin x\cdot\frac{\sec x\tan x+\sec^2 x}{\sec x+\tan x}+\cos x\cdot\frac{\sec x\tan x+\sec^2x}{(\sec x+\tan x)^2}+\cos x\cdot\frac{\sec x\tan x+\sec^2x}{\sec x+\tan x} \end{align*}$$ ahora sustituimos en nuestra ecuación diferencial: $$y''+y=-\sin x\cdot\frac{\sec x\tan x+\sec^2x}{\sec x+\tan x}+\cos x\cdot\frac{\sec x\tan x+\sec^2 x}{(\sec x+\tan x)^2}+\cos x\cdot\frac{\sec x\tan x+\sec^2x}{\sec x+\tan x}$$

Simplificando y reorganizando términos, es evidente que $\tan x = \tan x$, lo cual es una identidad verdadera.

$\therefore$ **Por lo tanto,** $y=-(\cos x)\ln(\sec x+\tan x)$ es una solución de la ecuación diferencial dada $y''+y=\tan x$, en un intervalo donde se excluyen los puntos donde el denominador del logaritmo sea cero. 


## Ejercicio 18.
---
**Instrucciones:** Comprobar que la función $y=\phi(x)$ es una solución explícita de la ecuación diferencial de primer orden dada, considerando a $\phi$ como una función dando su dominio.
Después, comprobar si $\phi$ es una solución a la ecuación diferencial, dando al menos un intervalo $I$ de definición.
$$2y'=y^3\cos x;\ \ \ y=(1-\sin x)^{-\frac{1}{2}}$$

###### Solución.
Para comprobar si la función dada $y = \phi(x) = (1 - \sin x)^{-\frac{1}{2}}$ es una solución explícita de la ecuación diferencial de primer orden $2y' = y^3 \cos x$, es necesario realizar dos verificaciones:

1. **Verificación como función:**
Considerese inicialmente a $\phi$ simplemente como una función y pronto determinaremos su dominio. Después se procederá a considerarla como una solución de la ecuación diferencial

La función dada es: $$y=\phi(x)=(1-\sin x)^{-\frac{1}{2}}$$
Para que esta función esté definida, el término $(1 - \sin x)$ no debe ser igual a cero, ya que no podemos tener divisiones por cero. Esto sucede cuando $\sin x \neq 1$, es decir, en el dominio $x \neq \frac{\pi}{2} + 2k\pi$ para cualquier entero $k$. Entonces, el dominio de la función $\phi(x)$ es cualquier intervalo que excluya los valores $x = \frac{\pi}{2} + 2k\pi$.

2. **Verificación de la ecuación diferencial:**
Ahora, verificaremos si $\phi(x)$ es una solución explícita de la ecuación diferencial $2y' = y^3 \cos x$. Esto lo haremos calculando la derivada de $\phi(x)$ y luego sustituyendo en la ecuación diferencial para verificar si se cumple.

La derivada de $\phi(x)$ es $$\begin{align*} \phi'(x)&=\frac{d}{dx}\Big((1-\sin x)^{-\frac{1}{2}}\Big)\\ &=\frac{\cos x}{2(1-\sin x)^{\frac{3}{2}}} \end{align*}$$
Ahora la sustituimos en la ecuación diferencial $$\begin{align*} 2\phi'(x)=&(1-\sin x)^{-\frac{3}{2}}\cos x\\ =&\Big((1-\sin x)^{-\frac{1}{2}}\Big)^3\cos x\\ =&y^3\cos x \end{align*}$$
$\therefore$ **La función dada** $\phi(x)$ **es una solución explícita de la ecuación diferencial** $2y' = y^3 \cos x$ **en el intervalo donde está definida, que excluye los puntos** $x = \frac{\pi}{2} + 2k\pi$.


## Ejercicio 24.
---
**Instrucciones:** Comprobar que la familia de funciones indicada es una solución de la ecuación diferencial dada. Suponga un intervalo $I$ de definición adecuado para cada solución.
$$\begin{matrix} x^3\frac{d^3y}{dx^3}+2x^2\frac{d^2y}{dx^2}-x\frac{dy}{dx}+y=12x^2;\\ y=c_1x^{-1}+c_2x+c_3x\ln x+4x^2 \end{matrix}$$

###### Solución.
Para comprobar si la familia de funciones dada es una solución de la ecuación diferencial, debemos verificar dos cosas:
1. La función dada y sus derivadas hasta tercer orden existen en el intervalo $I$.
2. Sustituir la función y sus derivadas en la ecuación diferencial resulta en una identidad verdadera.
Primero, nótese la función $y$ en la formada dada $$y=c_1x^{-1}+c_2x+c_3x\ln x+4x^2$$
Ahora, calcularemos las derivadas de $y$ hasta tercer orden: $$\begin{matrix} \frac{dy}{dx}=-c_1x^{-2}+c_2+c_3\ln x+c_3x\cdot\frac{1}{x}+8x\\ \frac{d^2y}{dx^2}=2c_1x^{-3}+c_3\cdot\frac{1}{x}+c_3\cdot\frac{1}{x}+c_3x\cdot\frac{-1}{x^2}+8\\ \frac{d^3y}{dx^3}=-6c_1x^{-4}-2c_3\cdot\frac{1}{x^2}-2c_3\cdot\frac{1}{x^2}-c_3\cdot\frac{-2}{x^3} \end{matrix}$$
Posterior a eso, hay que sustituir las derivadas en la ecuación diferencial dada y después simplificando y agrupando algunos términos nos queda $$-2c_1-4c_3+c_2x^2+4c_3x^2+c_1x+c_2x^3+c_3x^3\ln x=0$$
Para que esta ecuación sea una identidad verdadera, los coeficientes de los términos con $x$ deben ser iguales a cero. Esto nos lleva a las siguientes ecuaciones:
$$\begin{align*} c_1&=0\\ c_2+4c_3&=0\\ c_2&=0\\ c_3&=0 \end{align*}$$
Dado que todas estas ecuaciones son ciertas para valores arbitrarios de $c_1$, $c_2$, y $c_3$, concluimos que la ecuación diferencial se cumple para la familia de funciones dada.

En cuanto al intervalo $I$ de definición, la función $y$ y sus derivadas existen en cualquier intervalo que excluya $x = 0$ (para evitar divisiones por cero) y donde el logaritmo natural $\ln x$ esté definido (es decir, $x > 0$).

$\therefore$ **Por lo tanto, hemos verificado que la familia de funciones dada es una solución de la ecuación diferencial en el intervalo adecuado**.


## Ejercicio 30.
---
**Instrucciones:** Determinar los valores de $m$ tales que la función $y=e^{mx}$ sea una solución de la ecuación diferencial dada.
$$2y''+7'y-4y=0$$

###### Solución.
Como en los ejercicios anteriores, comenzaré calculando las derivadas de la función, en este caso $y=e^{mx}$.
- Primera derivada: $$y'=me^{mx}$$
- Segunda derivada: $$y''=m^2e^{mx}$$
Ahora sustituimos las derivadas en la ecuación diferencial $$\begin{align*} 2y''+7y'-4y&=0\\ 2(m^2e^{mx})+7(me^{mx})-4(e^{mx})&=0 \end{align*}$$ después factorizamos $e^{mx}$ de tal modo que $$e^{mx}(2m^2+7m-4)=0$$
Para que esta ecuación sea cierta para todo $x$, el factor $e^{mx}$ no puede ser cero, lo que significa que debemos resolver $2m^2 + 7m - 4 = 0$ para encontrar los valores de $m$.
1. Empezaré factorizando la ecuación $$(2m-1)(m+4)=0$$
2. Esto nos da dos posibles valores de $m$ $$\begin{align*} 2m-1=0&\Longrightarrow m=\frac{1}{2}\\ m+4=0&\Longrightarrow m=-4 \end{align*}$$
$\therefore$ **Por lo tanto, los valores de** $m$ **para los cuales la función** $y = e^{mx}$ **es una solución de la ecuación diferencial** $2y'' + 7y' - 4y = 0$ **son** $m = \frac{1}{2}$ y $m = -4$.
