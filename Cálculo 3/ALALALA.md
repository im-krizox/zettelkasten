Metadata:
14-08-2023
11:20
ALALALA

## Apunte.
---
>[!info] Definición.
>Sea $J$ un conjunto (índices) y $\mathcal{A}$ una colección de conjuntos.
>Diremos que $\mathcal{A}$ es una familia indexada por $J$ si existe $$\beta:J\rightarrow\mathcal{A}$$ función (inyectiva o sobre).
>Denotaremos por $A\alpha$ a la imagen de $\alpha\in J$ bajo $\beta$.

Si $\mathcal{X}=\mathbb{R}$ y $\tau$ como la colección de subconjuntos de $\mathbb{R}$ tal que si $A\in\tau$ y $a\in A$ existe $b,c\in\mathbb{R}$ con $a\in(b,c)\subset A$.
0. $\tau\subset P(\mathbb{R})$.
	1. Por definición de $\tau$.
1. $\emptyset,\mathbb{R}\in\tau$.
	1. Sean $e\in\mathbb{R}$, así $e\in(e^{-1},e^{+1})\subset\mathbb{R}$.
2. $\forall\{A_\alpha\}_{\alpha\in J}\subset \tau: \bigcup_{\alpha\in J}A_\alpha\in\tau$.
	1. Tarea para examen.
3. $\forall J$ conjunto finito de índices y $\forall\{A_{\alpha}\}_{\alpha\in J}\subset\tau:\bigcap A_\alpha\in\tau$. 

Par $(X,\tau)$ espacio topológico. Si $\mathcal{B}\subset\tau$ tal que $\forall A\in \tau$ existe $\mathcal{A}\subset \mathcal{B}$ tal que $A=\bigcup \mathcal{A}=\bigcup_{\mathcal{C}\in\mathcal{A}}c$ entonces $\mathcal{B}$ es base para la topología $\tau$. $$\mathcal{B}=\big\{(a,b)|a,b\in\mathbb{R}\big\}$$ si $(a,b)\in\mathcal{B}$ y $c\in(a,b)$, tomando $x_0,y_0\in\mathbb{R}:a=x_0\text{ y }b=y_0\Rightarrow c\in(x_0,y_0)\subset(a,b)$ así $(a,b)$ es un abierto en la topología usual de $\mathbb{R}$.

Si $A$ es un elemento de la topología usual de $\mathbb{R}$, entonces existe una colección $$\mathcal{B}_A\subset\mathcal{B}\text{ tal que }A=\bigcup_{c\in\mathcal{B}_A}$$
$$f:A\subset\mathbb{R}\rightarrow\mathbb{R}$$ continua, si y sólo sí $\forall x_0\in A, \forall \epsilon\in\mathbb{R}_+,\exists\delta\in\mathbb{R}_+:\forall x\in A:0<|x-x_0|<\delta\rightarrow x\in(x_0-\delta,x_0+\delta)\Rightarrow |f(x)-f(x_0)|<\epsilon$ $f(x)\in(f(x_0)-\epsilon,f(x_0)+\epsilon)$.



>[!info] Definición.
>Sea $(X,\tau)$ un espacio topológico y $x_0\in X$. Una vecindad (abierta) de $x_0$, es un conjunto $B\subset X$ tal que $x_0\in B(B\in \tau)$.


###### Tareas.
---







