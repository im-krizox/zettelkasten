Metadata:
Fecha: 18-08-2023
Hora: 11:29
Título: Espacios métricos.

## Apunte.
---
$$V,W,U\ \ \ \mathbb{K}-\text{espacio vectorial}$$ $$V\times W\longrightarrow\mathbb{R}$$

>[!info] Definición. *Bola abierta*.
>Si $(X,d)$ es un espacio métrico, $r\in\mathbb{R}_+\cup\{0\}$ y $x_0\in X$, el conjunto $$B_r(x_0):=\Big\{x\in X:d(x_0,x)<r\Big\}$$ se llama **bola abierta** con centro en $x_0$ y radio $r$.

En $\mathbb{R}^2$:
- $d(u,v)=\sqrt{\sum_{i=1}^2(u_i-v_i)^2}$ usual
	- *Imagen*
	- $(x_1-y_1)^2+(x_2-y_2)^2<r^2$
- $d(u,v)=\sum_{i=1}^{2}\big|v_i-u_i\big|$ taxista
	- *Imagen*
	- $|x_1-y_1|+|x_2-y_2|<r$
	- $$\begin{matrix} |x_1-y_1|+|x_2-y_2|=r\\ x_1=\theta\land r=1\\ |y_1|+|y_2|=1 \end{matrix}$$
	- $$\begin{matrix} y_1+y_2=1&x+y=1&y=1-x&m=-1\\ y_1-y_2=1&x-y=1&y=x-1&m=1\\ -y_1+y_2=1&-x+y=1&y=1+x&m=1\\ -y_1-y_2=1&x+y=-1&y=-x-1&m=-1 \end{matrix}$$

>[!info] Definición.
>Si $(X,d)$ es un espacio métrico, y $\mathcal{B}=\Big\{B_r(x_0)|r\in\mathbb{R}_+\cup\{0\}\land x_0\in X\Big\}$ es una base para una topología $\tau$ en $X$.
>La cual se denomina topología generada por la métrica $d$. $(X,\tau)$ se dice metrizable si existe $d$ métrica en $X$ tal que $\tau$ es la generada por $d$.
>

Un conjunto $A\subset X$ con $(X,d)$ espacio métrico es abierto sí y sólo si para cada $a\in A$, existe $r\in\mathbb{R}_+$ tal que $B_r(a)\subset A$.

>[!help] Observación.
>$\emptyset$ es abierto.
>>[!check] Demostración.
>>Por vacuidad.

>[!faq] Observación.
>$X$ es abierto.
>>[!check] Demostración.

>[!help] Proposición.
>


>[!info] Definición.
>Sean $(X,d_1)$ y $(Y,d_2)$ espacio métrico y $f:X\rightarrow Y$ una función es continua si $\forall a_0\in X$, $\forall \epsilon\in\mathbb{R}_+$, $\exists r\in\mathbb{R}_+$ tal que $x_0\in X$ si $x_0\in B_r(a_0)\backslash\{a_r\}$ entonces $$f(x_0)\in B_r\big(f(a_0)\big)=\Big\{y\in Y|d_2(y,a_0)<\epsilon\Big\}$$


###### Tareas.
---
- Para espacios métricos, definir:
	- Producto interno.
	- Norma.
	- Distancia (métrica).
- Métrica del supremo.