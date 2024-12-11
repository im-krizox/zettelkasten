Metadata:
Fecha: 31-08-2023
Hora: 18:23
Título: Tarea 2.

## Ejercicio 4.
**Instrucciones:** $y=\frac{1}{(x^{2}+c)}$ es una familia uniparamétrica de soluciones de la ED de primer orden $y'+2xy^{2}=0$. Determine una solución del PVI de primer orden que consiste en esta ecuación diferencial y la condición inicial dada. Dé el intervalo $I$ más largo en el cual está definida la solución.
$$y(-2)=\frac{1}{2}$$
###### Solución.
Tenemos la ecuación diferencial $y' + 2xy^2 = 0$ y se nos dice que la solución es de la forma $y = \frac{1}{x^2 + c}$, donde $c$ es una constante que aún no conocemos. Queremos encontrar una solución que también cumpla con la condición inicial $y(-2) = \frac{1}{2}$.

Comenzamos sustituyendo $y$ en la ecuación diferencial para verificar si realmente es una solución. La derivada de $y$ con respecto a $x$ es: $$y'=\frac{-2x}{(x^{2}+c)^{2}}$$
Ahora reemplazamos $y$ y $y'$ en la ecuación diferencial: $$\frac{-2x}{(x^{2}+c)^{2}}+2x\bigg( \frac{1}{x^{2}+c} \bigg)^{2}=0$$
Simplificamos esta expresión:
$$\frac{-2x}{(x^{2}+c)^{2}}+\frac{2x}{(x^{2}+c)^{2}}=0$$
Vemos que las dos partes se cancelan, lo que significa que la solución propuesta satisface la ecuación diferencial.

Ahora, necesitamos encontrar el valor de $c$ que cumple con la condición inicial $y(-2) = \frac{1}{2}$. Sustituimos $x = -2$ y $y = \frac{1}{2}$ en la solución propuesta: $$\frac{1}{2}=\frac{1}{(-2)^{2}+c}=\frac{1}{4+c}$$
Resolvemos esta ecuación para $c$:
$$\frac{1}{2}=\frac{1}{4+c}\Rightarrow4+c=2\Rightarrow c=-2$$
Con el valor de $c$ encontrado, la solución de la ecuación diferencial es: $$y=\frac{1}{x^{2}-2}$$
Esta solución está definida siempre que el denominador $x^2 - 2$ no sea cero, lo que significa que $x^2 \neq 2$. Esto nos lleva al intervalo de definición $(-\infty, -\sqrt{2})$.

$\therefore$ En resumen, la solución de la ecuación diferencial $y' + 2xy^2 = 0$ que cumple con la condición inicial $y(-2) = \frac{1}{2}$ es $y = \frac{1}{x^2 - 2}$, y esta solución está definida en el intervalo $(-\infty, -\sqrt{2})$.


## Ejercicio 10.
**Instrucciones:** $x=c_{1}\cos t+c_{2}\sin t$ es una familia de soluciones de dos parámetros de la ED de segundo orden $x''+x=0$. Determine una solución del PVI de segundo orden que consiste en esta ecuación diferencial y las condiciones iniciales dadas.
$$x\bigg(\frac{\pi}{4}\bigg)=\sqrt{2},\ \ \ \ \ x'\bigg( \frac{\pi}{4} \bigg)=2\sqrt{2}$$
###### Solución.
Tenemos la ecuación diferencial $x'' + x = 0$ y la familia de soluciones dada por $x = c_1 \cos t + c_2 \sin t$. Queremos encontrar una solución que también cumpla con las condiciones iniciales $x\left(\frac{\pi}{4}\right) = \sqrt{2}$ y $x'\left(\frac{\pi}{4}\right) = 2\sqrt{2}$.

Dado que $x = c_1 \cos t + c_2 \sin t$, calculamos las derivadas de $x$ con respecto a $t$: $$\begin{align*} x'&=-c_{1}\sin t+c_{2}\cos t\\ x''&=-c_{1}\cos t-c_{2}\sin t \end{align*}$$
Sustituimos las derivadas de $x$ en la ecuación diferencial $x'' + x = 0$: $$-c_{1}\cos t-c_{2}\sin t+c_{1}\cos t+c_{2}\sin t=0$$
Vemos que las dos partes se cancelan, lo que significa que la solución propuesta satisface la ecuación diferencial.

Ahora necesitamos usar las condiciones iniciales para determinar los valores de $c_1$ y $c_2$.

Dado que $x\left(\frac{\pi}{4}\right) = \sqrt{2}$, sustituimos $\frac{\pi}{4}$ en la expresión de $x$: $$c_{1}\cos \bigg( \frac{\pi}{4} \bigg)+c_{2}\sin\bigg(\frac{\pi}{4}\bigg)=\sqrt{2}$$
Simplificamos: $$\frac{\sqrt{2}}{2}c_{1}+\frac{\sqrt{2}}{2}c_{2}=\sqrt{2}$$
Dado que $x'\left(\frac{\pi}{4}\right) = 2\sqrt{2}$, sustituimos $\frac{\pi}{4}$ en la expresión de $x'$: $$-c_{1}\sin\bigg(\frac{\pi}{4}\bigg)+c_{2}\cos\bigg(\frac{\pi}{4}\bigg)=2\sqrt{2}$$
Simplificamos: $$-\frac{\sqrt{2}}{2}c_{1}+\frac{\sqrt{2}}{2}c_{2}=2\sqrt{2}$$
Resolvemos este sistema de ecuaciones para $c_1$ y $c_2$. Podemos hacerlo de diversas maneras, por ejemplo, multiplicando la segunda ecuación por $\frac{\sqrt{2}}{2}$ y sumándola a la primera ecuación: $$\frac{\sqrt{2}}{2}c_{1}+\frac{\sqrt{2}}{2}c_{2}-\frac{\sqrt{2}}{2}c_{1}+\frac{\sqrt{2}}{2}c_{2}=\sqrt{2}+2\sqrt{2}$$
Esto se simplifica a: $$\sqrt{2}c_{2}=3\sqrt{2}\Rightarrow c_{2}=3$$
Luego, podemos sustituir el valor de $c_2$ en la primera ecuación para encontrar el valor de $c_1$: $$\frac{\sqrt{2}}{2}c_{1}+\frac{\sqrt{2}}{2}\cdot3=\sqrt{2}\Rightarrow\frac{\sqrt{2}}{2}c_{1}+\frac{3\sqrt{2}}{2}=\sqrt{2}\Rightarrow\frac{\sqrt{2}}{2}c_{1}=\frac{\sqrt{2}}{2}\Rightarrow c_{1}=1$$
Con los valores de $c_1$ y $c_2$ determinados, la solución de la ecuación diferencial con las condiciones iniciales dadas es: $$x=c_{1}\cos t+c_{2}\sin t=\cos t+3\sin t$$
$\therefore$ En resumen, la solución del problema de valor inicial es $x = \cos t + 3 \sin t$.


## Ejercicio 14.
**Instrucciones:** $y=c_{1}e^{x}+c_{2}e^{-x}$ es una familia de dos parámetros de soluciones de segundo orden ED $y''-y=0$. Encuentre una solución del PVI de segundo orden que consiste en esta ecuación diferencial y las condiciones iniciales dadas.
$$y(0)=0,\ \ \ \ \ y'(0)=0$$
###### Solución.
Tenemos la ecuación diferencial $y'' - y = 0$ y la familia de soluciones dada por $y = c_1 e^x + c_2 e^{-x}$. Queremos encontrar una solución que también cumpla con las condiciones iniciales $y(0) = 0$ y $y'(0) = 0$.

Dado que $y = c_1 e^x + c_2 e^{-x}$, calculamos las derivadas de $y$ con respecto a $x$: $$\begin{align*} y'&=c_{1}e^{x}-c_{2}e^{-x}\\ y''&=c_{1}e^{x}+c_{2}e^{-x} \end{align*}$$
Sustituimos las derivadas de $y$ en la ecuación diferencial $y'' - y = 0$: $$(c_{1}e^{x}+c_{2}e^{-x})-(c_{1}e^{x}+c_{2}e^{-x})=0$$
Vemos que las dos partes se cancelan, lo que significa que la solución propuesta satisface la ecuación diferencial.

Ahora necesitamos usar las condiciones iniciales para determinar los valores de $c_1$ y $c_2$.

Dado que $y(0) = 0$, sustituimos $x = 0$ en la expresión de $y$: $$c_{1}e^{0}+c_{2}e^{0}=0\Rightarrow c_{1}+c_{2}=0$$
Dado que $y'(0) = 0$, sustituimos $x = 0$ en la expresión de $y'$: $$c_{1}e^{0}-c_{2}e^{0}=0\Rightarrow c_{1}-c_{2}=0$$
Entonces, tenemos el siguiente sistema de ecuaciones: $$\begin{align*} c_1 + c_2 &= 0 \\ c_1 - c_2 &= 0 \end{align*}$$
Esencialmente, estas ecuaciones nos dicen que $c_1$ y $c_2$ son iguales, pero con signos opuestos. Resolvemos este sistema y encontramos que $c_1 = c_2 = 0$.

Con los valores de $c_1$ y $c_2$ determinados, la solución de la ecuación diferencial con las condiciones iniciales dadas es: $$y=c_{1}e^{x}+c_{2}e^{-x}=0$$
$\therefore$ En resumen, la solución del problema de valor inicial es $y = 0$. Esto significa que la función constante cero es la única solución que satisface las condiciones iniciales proporcionadas.


## Ejercicio 20.
**Instrucciones:** Determine una región del plano $xy$ donde la ecuación diferencial dada tendría una solución única cuya gráfica pase por un punto $(x_{0},y_{0})$ en la región.
$$\frac{dy}{dx}-y=x$$
###### Solución.
Dada la ecuación diferencial $\frac{dy}{dx} - y = x$, queremos determinar una región en el plano $xy$ donde esta ecuación tenga una solución única que pase por un punto $(x_0, y_0)$ en esa región.

Vamos a reorganizar la ecuación diferencial para que esté en su forma estándar: $$\frac{dy}{dx}=y+x$$
Ahora definimos la función $f(x, y) = y + x$. Calculamos su derivada parcial con respecto a $y$ $$\frac{\partial f}{\partial y}=1$$
El Teorema de Existencia y Unicidad garantiza la existencia y unicidad de soluciones para ecuaciones diferenciales de primer orden de la forma $\frac{dy}{dx} = f(x, y)$. La condición necesaria para la existencia y unicidad es que $\frac{\partial f}{\partial y}$ sea continua en la región de interés. En este caso, $\frac{\partial f}{\partial y}$ es constante y, por lo tanto, es continua en todo el plano.

Dado que $\frac{\partial f}{\partial y} = 1$ es constante y continua en todo el plano $xy$, podemos aplicar el Teorema de Existencia y Unicidad para afirmar que la ecuación diferencial $\frac{dy}{dx} = y + x$ tiene una solución única en todo el plano. Por lo tanto, no hay ninguna restricción en la región donde esta ecuación tenga una solución única que pase por el punto $(x_0, y_0)$.

$\therefore$ En resumen, la solución es que la ecuación diferencial tiene una solución única en todo el plano $xy$, sin importar la región, debido a la naturaleza constante y continua de la derivada parcial $\frac{\partial f}{\partial y}$.


## Ejercicio 24.
**Instrucciones:** Determine una región del plano $xy$ donde la ecuación diferencial dada tendría una solución única cuya gráfica pase por un punto $(x_{0},y_{0})$ en la región.
$$(y-x)y'=y+x$$
###### Solución.
Dada la ecuación diferencial $(y - x)y' = y + x$, queremos determinar una región en el plano $xy$ donde esta ecuación tenga una solución única que pase por un punto $(x_0, y_0)$ en esa región.

Vamos a reorganizar la ecuación diferencial para que esté en su forma estándar: $$y'=\frac{y+x}{y-x}$$
Definimos la función $f(x, y) = \frac{y + x}{y - x}$. Calculamos su derivada parcial con respecto a $y$: $$\frac{\partial f}{\partial y}=\frac{-2x}{(y-x)^{2}}$$
La derivada parcial $\frac{\partial f}{\partial y}$ está definida en todo el plano excepto donde el denominador $(y - x)^2$ sea igual a cero, es decir, donde $y = x$. En otras palabras, $\frac{\partial f}{\partial y}$ está indefinida en la línea $y = x$.

Dado que $\frac{\partial f}{\partial y}$ está definida en todas partes excepto en la línea $y = x$, podemos aplicar el Teorema de Existencia y Unicidad para afirmar que la ecuación diferencial $(y - x)y' = y + x$ tiene una solución única en cualquier región del plano $xy$ donde $y \neq x$.

La región donde $y \neq x$ es cualquier región del plano excepto la línea $y = x$. Por lo tanto, la ecuación diferencial tendrá una solución única en cualquier región del plano donde $y < x$ o donde $y > x$.

$\therefore$ En resumen, la solución es que la ecuación diferencial tiene una solución única en cualquier región donde $y < x$ o donde $y > x$, debido a la naturaleza de la derivada parcial $\frac{\partial f}{\partial y}$ y a las condiciones de existencia del Teorema de Existencia y Unicidad.


## Ejercicio 30.
**Instrucciones:**
1. Compruebe que $y=\tan(x+c)$ es una familia uniparamétrica de soluciones de la ecuación diferencial $y'=1+y^{2}$.
2. Puesto que $f(x,y)=1+y^{2}$ y $\frac{\partial f}{\partial y}=2y$ son continuas en donde quiera, la región $R$ en el teorema 1.2.1 se puede considerar como todo el plano $xy$. Utilice la familia de soluciones del inciso 1. para determinar una solución explícita del problema con valores iniciales de primer orden $y'=1+y^{2}$, $y(0)=0$. Aun cuando $x_0=0$ esté en el intervalo $(-2,2)$, explique por qué la solución no está definida sobre este intervalo.
3. Determine el intervalo $I$ de definición más largo para la solución del problema con valores iniciales del inciso 2..

###### Solución.
Dada la ecuación diferencial $y' = 1 + y^2$, se nos pide verificar si $y = \tan(x + c)$ es una familia de soluciones. Calculamos la derivada de $y$ con respecto a $x$: $$\frac{d}{dx}\big( \tan(x+c) \big)=\sec^{2}(x+c)=1+\tan^{2}(x+c)$$
Vemos que $\frac{d}{dx}(\tan(x + c))$ coincide con la expresión $1 + y^2$, por lo tanto, la función $y = \tan(x + c)$ satisface la ecuación diferencial.

Dado que $y = \tan(x + c)$ satisface la ecuación diferencial, vamos a utilizarla para resolver el problema con valores iniciales $y' = 1 + y^2$ y $y(0) = 0$. Si sustituimos $x = 0$ y $y = 0$ en $y = \tan(x + c)$, obtenemos: $$0=\tan(0+c)=\tan c$$
Esto significa que $c = 0$, y por lo tanto, la solución es $y = \tan x$.

La solución $y = \tan x$ es discontinua en $x = \pm \frac{\pi}{2}$ debido a la singularidad de la función tangente en esos puntos. Dado que la solución debe pasar por el punto $(0, 0)$ y la ecuación no es válida en $x = \pm \frac{\pi}{2}$, la solución no puede estar definida en el intervalo $(-2, 2)$, ya que contiene los puntos problemáticos $\pm \frac{\pi}{2}$.

El intervalo más grande en el cual la solución puede estar definida es el intervalo donde no hay singularidades, es decir, el intervalo $\left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$.

$\therefore$ En resumen:
1. La solución propuesta $y = \tan(x + c)$ satisface la ecuación diferencial.
2. La solución con valores iniciales $y' = 1 + y^2$, $y(0) = 0$ es $y = \tan x$, pero no está definida en el intervalo $(-2, 2)$ debido a las singularidades en $x = \pm \frac{\pi}{2}$.
3. El intervalo de definición más largo para la solución es $\left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$.

