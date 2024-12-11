Metadata:
Fecha: 24-08-2023
Hora: 13:15
Título: Solución de una ecuación diferencial.

## Apunte.
---
>[!info] Definición. *Solución de una ecuación diferencial*.
>Una solución de una ecuación diferencial es una función $\phi(t)$ definida en un intervalo $I$ y que tiene al menos $n$ derivadas continuas en $I$, las cuales cuando se sustituyen en la ecuación diferencial reducen la ecuación a una igualdad.

>[!info] Definición. *Coma integral*.
>Una coma integral de una E. D. O. es la gráfica de una solución.

>[!info] Definición. *Familia uniparámetrica*.
>Una familia uniparámetrica de soluciones de una E. D. O.  es una solución de la E. D. que contiene un parámetro y es representada por un conjunto de la forma $G(t,y,c)=0$.

Una familia a $n$-parámetros de soluciones de una E. D. O. es una familia de soluciones $G(t,y,c_1,c_2,\ldots,c_n)=0$ de una E. D. O. de orden $n$ con la cual se puede obtener todas las soluciones de la E. D. en un intervalo $I$.

Una solución singular de una E. D. O. es una solución que no puede obtenerse de una familia paramétrica de soluciones.


### Problema de valores iniciales.
---
$$\begin{matrix} F(t,y,y',\ldots,y^{(n)})=0;\\ y(t_0)=y_0,\ y'(t_0)=y_1,\ldots,y^{n-1}(t_0)=y_{n+1} \end{matrix}$$
Una solución a un P. V. I. es una solución particular de la E. D. que cumple las condiciones iniciales.

>[!info] Definición.
>Una solución de una ecuación diferencial se llama implícita si se escribe en la forma $G(x,y)=0$, para alguna función $G$ que depende de dos variables y que este definida en un solo conjunto de la forma $I\times J$ donde $I$ es un intervalo de solución de $G$ para la E. D.

#### Ejemplo.
---
Considere la E. D. $y'=-\frac{x}{y}$.
$x^2+y^2=25$ es una solución implícita de la E. D.
**Demostración:**
La función $G(x,y)=x^2+y^2-25$ cumple con $G(x,y)=0\Longleftrightarrow x^2+y^2=25$.
Ya que si despejamos la variable dependiente $y=\pm\sqrt{25-x^2}$ y así nos quedan dos soluciones $$\begin{matrix} \phi_1(x)=y=\sqrt{25-x^2}\\ \phi_2(x)=y=-\sqrt{25-x^2} \end{matrix}$$

##### Ejercicio.
---
Verifica que la ecuación $t^2+y^2-4=0$ es una solución implícita de la E. D. $t+yy'=0$, en el Intervalo $-2<t<2$.
**Demostración:**
La función $G(t,y)=t^2+y^2-4$ cumple con $G(t,y)=0\Longleftrightarrow t^2+y^2=4$.
Si despejamos la variable dependiente $y=\pm\sqrt{4-t^2}$ y así nos quedan dos soluciones $$\begin{matrix} \phi_1(x)=y=\sqrt{4-t^2}\\ \phi_2(x)=y=-\sqrt{4-t^2} \end{matrix}$$


>[!info] Teorema de existencia y unicidad de soluciones.
>Sea $R$ una región rectangular en $\mathbb{R}^2$ definida por las desigualdades $a\leq x\leq b$ y $c\leq y\leq d$ que contiene al punto $(x_0,y_0)$ en su interior. Si tanto $f(x,y)$ como $\frac{\partial f}{dy}$ son continuas en $\mathbb{R}$, entonces existe un intervalo $I_0=(x_0-h,x_0+h),h>0$ contenido en el intervalo $[a,b]$ y una función única $y(x)$ que es solución al problema de valores iniciales $\frac{df}{dx}=f(x,y);y(x_0)=y_0$.


>



###### Tareas.
---

