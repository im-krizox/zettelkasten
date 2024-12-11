Día: 11/08/2023

## Notación y definición.
---
$$\begin{align*} f:&\overbrace{A}^{\text{Dom}(f)}\longrightarrow\overbrace{B}^{\text{Cod}(f)}\\ &\ \ \ w\ \ \ \ \longmapsto f(w) \end{align*}$$

**Imagen:** Subconjunto del codominio.
	- $\text{Im}(f)$
	- $\text{Img}(f)$
	- $\text{I}(f)$
	- $f(A)$

Se define de las siguientes maneras: $$\begin{matrix} :=\bigg{\{}u\in B\Big{|}\exists w\in A:f(w)=u\bigg{\}}\\ :=\bigg{\{}f(w)\Big{|}w\in A\bigg{\}} \end{matrix}$$
Si $u\in B,\ f^{-1}\{u\}=\Big{\{}w\in A\big{|}f(w)=u\Big{\}}$ es la imagen inversa.
Si $D\subset B,\ f^{-1}(D):=\Big{\{}w\in A\big{|}f(w)\in D\Big{\}}$.


### Ejemplos.
---
$$\begin{align*} f\big{(}f^{-1}(D)\big{)}^{\text{¿?}}&=0\\ f^{-1}\big{(}f(D)\big{)}&\neq0 \end{align*}$$
#Ejercicio_para_1°_parcial_ 
$$\begin{align*} f:&\mathbb{Z}\longrightarrow2\mathbb{Z}\\ &u\longmapsto2|u| \end{align*}$$ 
#### Conjunción de funciones.
---
$$\begin{matrix} \begin{align*} f:&A\longrightarrow B\\ &x\longmapsto f(x) \end{align*}\\ A\overbrace{\longrightarrow}^{f}B \end{matrix}$$ $$\begin{matrix} \begin{align*} g:&C\longrightarrow D\\ &u\longmapsto g(u) \end{align*}\\ \\ C\overbrace{\longrightarrow}^{g}D \end{matrix}$$ para unirlas tenemos que *crear una escalera* $$\begin{align*} A&\overbrace{\longrightarrow}^{f}B\\ a&\longmapsto f(a)\\ \\ C&\overbrace{\longrightarrow}^{g}D\\ f(a)&\longmapsto g(f(a)) \end{align*}$$


### Notación de conjuntos.
---
- Semi-abierto $$(0,1]$$ *el conjunto es semi-abierto por la izquierda y cerrado por la derecha*.

- Semi-cerrado $$(0,1]$$ *el conjunto es semi-abierto por la izquierda y semi-cerrado por la derecha*.


### Topología.
---
Sea $A$ un conjunto, $\tau\subset P(A)$ donde
1. $\emptyset, A\in \tau$.
2. $\mathbf{A}\subset\tau\rightarrow{\bigcup}_{B\in\mathbf{A}}B\in\tau$ $(B_1,B_2\in\tau\Rightarrow B_1\cup B_2\in \tau)$.
3. $A_1,\ldots,A_n\in\tau\Rightarrow\bigcap_{i=1}^{n}A_i\in\tau$.
$\tau$ se denomina una topología para $A$ y $(A,\tau)$ espacio topológico.