Metadata:
Fecha: 04-09-2023
Hora: 11:41
Título: Untitled 3

###### Puntos extras.
Si $C$ es una circunferencia en $\mathbb{R}^2$ con centro $(h,k)$ y radio $r\in\mathbb{R}_{+}$, además si $u\in\mathbb{R}^{2}\backslash C$. Demuestra que $$d(u,C)=d(u,p)$$ donde $p\in C\cap l_{u}$ donde $l_{u}$ es la recta que pasa por $u$ y $(h,k)$ y $p$ es el punto que cumple la menor de las distancias con los dos puntos en $C\cap l_{u}$.

- Punto extra para el segundo parcial:
	- $1$ punto si lo hace con Geometría Analítica.
	- $1$ punto al curso si lo hace con regla y compás.


## Retomando lo de la clase pasada.
$$\begin{align*} A=&[0,1]\times(0,1)\\ A^{\circ}=&(0,1)\times(0,1) \end{align*}$$
Vemos que $\partial A=l_{1}\cup l_{2}\cup l_{3}\cup l_{4}=:l$.
$\Rightarrow]$ Tome $u\in l_{1}\cup l_{2}\cup l_{3}\cup l_{4}$ entonces, dado $r\in\mathbb{R}_{+}$
- Si $u\in l_{1}$ tomemos $w=(u_{1},u_{2}-\frac{r}{2})$, así $w\in\mathbb{R}^{2}\backslash A$ y $w\in B_{r}(u)$.
- Si $u\in l_2$ tomemos $w=(u_{1}+\frac{r}{2},u_{2})$, así $w\in\mathbb{R}^{2}\backslash A$ y $w\in B_{r}(u)$.
- Si $u\in l_{3}$ tomemos $w=(u_{1},u_{2}+\frac{r}{2})$, así $w\in\mathbb{R}^{2}\backslash A$ y $w\in B_{r}(u)$.
- Si $u\in l_{4}$ tomemos $w=(u_{1}-\frac{r}{2},u_{2})$, así $w\in\mathbb{R}^{2}\backslash A$ y $w\in B_{r}(u)$.

>[!note] Nota.
>Demostrar porque $w\in\mathbb{R}^{2}\backslash A$.

![[Pasted image 20230904120535.png|350]]

Así $B_{r}(u)\cap A^{c}\neq\emptyset$.
Recordando que
- $r_{1}=d(u,l_{1})$
- $r_{2}=d(u,l_{2})$
- $r_{3}=d(u,l_{3})$
- $r_{4}=d(u,l_{4})$

Primero supongamos que $u\in\{\theta,l_{1},l_{2},(1,1)\}$.
Ahora bien si $t_{i}=\frac{1}{2}\min\{r,r_{i}\}$ con $i\in\{1,2,3,4\}$:
- Si $u\in l_{1}$ tomemos el punto $w=(u_{1},u_{2}+t_{3})$ así $w\in B_{r}(u)\cap A$.
- Si $u\in l_{2}$ tomemos el punto $w=(u_{1}-t_{4},u_{2})$ así $w\in B_{r}(u)\cap A$.
- Si $u\in l_{3}$ tomemos el punto $w=(u_{1},u_{2}-t_{1})$ así $w\in B_{r}(u)\cap A$.
- Si $u\in l_{4}$ tomemos el punto $w=(u_{1}+t_{2},u_{2})$ así $w\in B_{r}(u)\cap A$.

Ahora si $r\geq 1$ y
- Si $u=e_{2}$, tome $w=(\frac{1}{4},\frac{3}{4})$.
- Si $u=\theta$, tome $w=(\frac{1}{4},\frac{1}{4})$.
- Si $u=e_{1}$, tome $w=(\frac{3}{4},\frac{1}{4})$.
- Si $u=e_{1}+e_{2}$, tome $w=(\frac{3}{4},\frac{3}{4})$.
así $w\in B_{r}(u)\cap A$.

Si $r<1$ y si
- $u=\theta$ tome $w=(\frac{r}{2},\frac{r}{2})$.
- $u=e_{1}$ tome $w=(1-\frac{1}{r},\frac{r}{2})$.
- $u=e_{1}+e_{2}$ tome $w=(1-\frac{r}{2},1-\frac{r}{2})$.
- $u=e_{2}$ tome $w=(0,\frac{r}{2})$.
Por lo que $w\in B_{r}(u)\cap A$.
Así $B_{r}(u)\cap A\neq\emptyset$.
$\therefore$ $\partial A\supset l$.

Si $u\notin l\cup A$, entonces $B_{r}(u)\subset A^{c}$ donde $r=\frac{1}{10}d(u,A)$, por lo que $B_{r}(u)\cap A=\emptyset$.
Análogamente si $u\in A^{\circ}$, existe $r\in\mathbb{R}_{+}$ tal que $B_{r}(u)\subset A$, así $B_{r}(u)\cap A^{c}=\emptyset$.
Así $\partial A\subset l$.


>[!info] Definición.
>Un punto $u_{0}\in\mathbb{R}^{n}$ es un punto de acumulación de un conjunto $A\subset \mathbb{R}^{n}$ si y sólo si $\forall r\in\mathbb{R}_{+}$ $B_{r}^{*}(u)\cap A\neq\emptyset$.
>A los puntos de acumulación del conjunto $A$ se denotan por $A'$.

#### Ejemplos.
1. En $\mathbb{R}$, tomemos $A=\{\frac{1}{n}|n\in\mathbb{N} \}$ así $A'=\{0\}$.
   ![[Pasted image 20230904124035.png|450]]
2. En $\mathbb{R}$ tome $\mathbb{Z}$ 
   ![[Pasted image 20230904124151.png|450]] Así $A'=\emptyset$.

3. Si $A\subset \mathbb{R}^{n}$ un conjunto finito $A'\subset\emptyset\land A=\emptyset\land A\supset\emptyset$.

4. Tome $\mathbb{Q}\cap(0,1)$ en $\mathbb{R}$. Por densidad de $\mathbb{Q}$ en $\mathbb{R}$ tendremos $\big( \mathbb{Q}\cap (0,1) \big)'=[0,1]$.
