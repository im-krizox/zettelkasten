Metadata:
Fecha: 22-08-2023
Hora: 13:18
Título: Solución de una Ecuación Diferencial.

## Apunte.
---
Sea una EDO $$F(x,y,y',\ldots,y^{(n)})=0$$
Una función $\phi:I\rightarrow\mathbb{R}$ y que sus derivadas sean continuas, es solución de la EDO si $$F\big(x,\phi(x),\phi'(x),\ldots,\phi^{(n)}(x)\big)=0$$

#### Ejemplos.
---
Para $y'(x)=0$.
Sea $$\begin{align*} \phi:&I\rightarrow\mathbb{R}\\ \phi(x)=&c,&c\in\mathbb{R},\text{ fijo} \end{align*}$$
entonces $\phi'(x)=0$, así que
$$\begin{matrix} y\longleftrightarrow\phi(x)=c\\ y'\longleftrightarrow\phi'(x)=0 \end{matrix}$$ de esta forma $\phi'(x)=0$.
Así, $\phi$ es solución de la ED en $I\in\mathbb{R}$.

---

Para $y''(x)=0$.
Sea $$\begin{matrix} \phi(x)=ax+b\\ \phi'(x)=a\\ \phi''(x)=0 \end{matrix}$$ entonces $\phi''(x)=0$, así que $$\begin{matrix} y\longleftrightarrow\phi(x)\\ y'\longleftrightarrow\phi'(x)\\ y''\longleftrightarrow\phi''(x) \end{matrix}$$ de esta forma $\phi''(x)=0$.
Así, $\phi$ es solución de la E. D.

---

Para $y'''(x)=0$.
Sea $$\begin{matrix} \phi(x)=ax^2+bx+c\\ \phi'(x)=2ax+b\\ \phi''(x)=2a\\ \phi'''(x)=0 \end{matrix}$$ entonces $\phi'''(x)=0$, así que $$\begin{matrix} y\longleftrightarrow\phi(x)\\ y'\longleftrightarrow\phi'(x)\\ y''\longleftrightarrow\phi''(x)\\ y'''\longleftrightarrow\phi'''(x) \end{matrix}$$
Así, $\phi$ es solución de la E. D.

---

Para $y''-4y=0$.
Sea $$\begin{align*} \phi(x)&=ce^{2x}\\ \phi'(x)&=2ce^{2x}\\ \phi''(x)&=4ce^{2x} \end{align*}$$ entonces $$\begin{align*} \phi''(x)-4\phi(x)&=0\\ 4ce^{2x}-4(ce^{2x})&=0\\ 4ce^{2x}-4ce^{2x}&=0\\ 0&=0 \end{align*}$$
Así, $\phi$ es solución para la E. D.
**Nota:** Otra solución es $\phi(x)=de^{-2x}$.

---

>[!info] Definición. *Familia Uniparámetrica*.
>Al conjunto de soluciones de una E. D. se le llama Familia Uniparámetrica.

#### Ejemplo.
---
$$\begin{align*} \varphi(x)&=ce^{2x}+de^{-2x}\\ \varphi'(x)&=2ce^{2x}-2de^{-2x}\\ \varphi''(x)&=4ce^{2x}-4de^{-2x} \end{align*}$$ de está forma $$\begin{align*} \varphi''(x)-4\varphi(x)&=0\\ 4ce^{2x}+4de^{-2x}-4(ce^{2x}+de^{-2x})&=0\\ 0&=0  \end{align*}$$
Así, $ce^{2x}+de^{-2x}$ es una familia biparámetrica de soluciones de la E. D o familia a dos parámetros de soluciones de la E. D.

---

>[!info] Definición.
>Al problema de encontrar una solución de una ecuación diferencial $$F(t,y,\ldots,y^{(n)})=0$$ que satisface las condiciones $$y(t_0)=y_0,\ y'(t_0)=y_1,\ldots,y^{(n-1)}(t_0)=y_{n-1}\in\mathbb{R}$$ se le llama **problema con valores iniciales de** $n$**-ésimo orden**.

#### Ejemplo.
---
Para $y'(x)=0,\  y(0)=3$.
$$\begin{matrix} \phi(x)=c\\ 3=\phi(0)=c\Rightarrow c=3 \end{matrix}$$ $y(x)=3$ es la solución al P. V. I.

---
Para $y'(x)-16y(x)=0,\ y(0)=3$.
$$\begin{matrix} \phi_c(x)=ce^{16x}\Rightarrow3=\phi_c(0)=ce^{16(0)}\\ \begin{align*} 3&=ce^{16(0)}\\ &=ce^{0}\\ &=c1\\ 3&=c \end{align*} \end{matrix}$$ $\phi_3(x)=3e^{16x}$ es la solución al P. V. I.

---

*Foto*

---

Para $y''-4y=0,\ y(1)=1,\ y'(1)=-2$.
$$\begin{matrix} \phi(1)=ce^{2(1)}+de^{2(-1)}=0\\ \phi'(1)=2ce^{2(1)}+2de^{2(-1)}=-2 \end{matrix}$$ nos genera lo siguiente $$\begin{align*} ce^2+de^{-2}&=1\\ 2ce^2+2de^{-2}&=-2 \end{align*}$$ 




###### Tareas.
---
