Metadata:
15-08-2023
13:13
Definición de ecuación diferencial.

## Apunte.
---
Sea la siguiente ecuación $$\frac{dx(t)}{dt}=k\big{(}x(t)-f(t)\big{)}$$ donde
	- $t$ se le llama *variable independiente*.
	- $x$ *variable dependiente*.

>[!info] Definición. *Ecuación Diferencial (ED)*.
>Una Ecuación Diferencial (ED) es una ecuación que contiene derivadas de una o más variables (*dependientes*) con respecto a una o más variables *independientes*.

#### Ejemplos.
---
1. $\frac{dx(t)}{dt}=kx(t)$ es una ecuación diferencial, con $k\in\mathbb{R}$.
2. $x(t)+y(t)=x'(t)+y''(t)$.
3. $y(s,t)=\frac{\partial y(s,t)}{\partial s}-\frac{\partial y(s,t)}{\partial t}$ es una ecuación diferencial parcial, donde, $y$ es variable dependiente y $s,t$ variables independientes.
4. $\frac{x(t)}{y(t)}=x'(t)\cdot y'(t)$ es una ecuación diferencial.

>[!info] Definición. *Ecuación diferencial parcial (EDP)*.
>Una ecuación diferencial parcial es una ecuación diferencial (EDP) que involucra derivadas parciales de una ó más variables dependientes con respecto de dos ó mas variables independientes.

5. $y(s,t)=\frac{\partial y(s,t)}{\partial t}$ es una EDP.

>[!info] Definición. *Ecuación diferencial ordinaria (EDO)*.
>Una ecuación diferencial ordinaria (EDO) es una ecuación diferencial de la forma $$F(x,y,y',\ldots,y^{(n)})=0$$ donde $F$ es una función de $n+1$ variables, $y$ es una función de la variable $x$ y $$y'=\frac{dy}{dx},\ldots y^{(n)}=\frac{dy^n}{dx^n}$$ son las derivadas de $y$.

En otras palabras, una EDO es una ecuación diferencial en la que sólo aparecen derivadas de una ó más variables dependientes con respecto a una sola variables independiente.

##### Retomando los ejemplos anteriores con EDO.
---
1. $x(t)+y(t)=x'(t)+y''(t)$. Ahora si fuera una EDO sería $$F(t,x,y,x',y',x'',y'')=x(t)+y(t)-x'(t)-y''(t)=0$$ si hacemos una sustitución quedaría $$F(x_1,x_2,x_3,x_4,x_5,x_6,x_7)=x_2+x_3-x_4-x_7$$
2. $\frac{dx(t)}{dt}=kx(t)$, si la convertimos a una EDO quedaría $$\begin{align*} F(t,x,x')&=\frac{dx(t)}{dt}-kx(t)\\ &=x'-kx(t)&=0 \end{align*}$$


### Clasificación por orden.
---
>[!info] Definición. *Clasificación por orden*.
>El orden de una ecuación diferencial ordinaria es el orden de la derivada mayor que aparece en la ecuación diferencial.

#### Ejemplos.
---
1. $y'(t)=5y(t)$ es una ecuación diferencial de primer orden.
2. $y'''(t)=y(t)$ es una ecuación diferencial ordinaria de tercer orden.
3. $z^{(4)}(t)+3z'''(t)+4z''(t)+z'(t)-25t=0$ es una EDO de cuarto orden.
4. $\big{(}z^{(4)}\big{)}^4+3z'''(t)+\big{(}4z''(t)\big{)}^2+z'(t)-25t=0$ es una ecuación diferencial ordinaria donde $t$ es la variable independiente, $z$ la variable dependiente.

>[!tip] Tip de derivadas y potencias.
>Las potencias no afectan a las derivadas. $$\big(z^n\big)^m$$ es una ecuación diferencial de grado $n$ elevada a la $m$ potencia.

5. $\big(z^4\big)^4+3z''(t)+(4z'')^2-25t=0$ es una EDO de 2° orden.
6. $\cos(t)z^{(5)}(t)-e^tz''(t)+4=0$ es una EDO de quinto orden.


### Clasificación por linealidad.
---
>[!info] Definición.
>Una ecuación diferencial ordinaria $F(x,y,y',\ldots,y^{(n)})=0$ de orden $n$ es lineal, si $F$ es lineal con respecto a las variables $y,y',\ldots,y^{(n)}$.
>Es decir, la ecuación diferencial admite una expresión de la forma: $$a_n(t)y^{(n)}+a_{n-1}(t)y^{(n-1)}+\ldots+a_2(t)y''(t)+a_1(t)y'+a_0(t)y+g(t)=0$$


>[!tip] Tip para identificar ecuaciones diferenciales no lineales.
>Si la variable dependiente está elevada a una $n+1$ potencia, o dentro de una función, la ecuación diferencial no es lineal.
>


#### Ejemplos de ecuaciones diferenciales lineales.
---
1. $\cos(t)z^{(5)}(t)-e^tz''(t)+4=0$ es una EDO de 5° orden lineal.
2. $e^{y(t)}=y'(t)$ es una EDO de primer orden no lineal.
3. $\cos\big(y(t)\big)=y'(t)$ es una EDO de 1° orden no lineal.
4. $y(t)=\sqrt{y''(t)}$ es una EDO de 2° orden no lineal.

#### Ejemplos usando todas las clasificaciones.
1. $\Big(\frac{dr}{dt}\Big)^3=\sqrt{\frac{d^2r}{ds^2}+1}$ es una EDP de segundo orden no lineal.
2. $y''+y\sin(t)=0$ es una EDO de segundo orden lineal.
3. $\frac{dy}{dt}+3\Big(\frac{d^2y}{dt^2}\Big)^5+5y=0$ es una EDO de 2° orden no lineal.
4. $\frac{\partial^2\rho}{\partial t^2}+\frac{\partial^2\theta}{\partial t^2}=\sqrt{\rho+\Big(}$ 

###### Tareas.
---







