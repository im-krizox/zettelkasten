Metadata:
Fecha: 01-09-2023
Hora: 11:50
Título: Más cosas de cálculo.

$$A=[0,1]\times(0,1)$$
Si $u\in(0,1)\times(0,1)$ entonces $u\in A^{\circ}$.
$\therefore$ $(0,1)\times(0,1)\subset A^{\circ}$.

Supongamos $\exists u_{0}\in A^{\circ}:u_{0}\notin(0,1)\times(0,1)$, con $u_{0}=(u_{1},u_{2})$.

Entonces:
- **Caso 1)** $u_{0}\in l_{1}\cup l_{2}\cup l_{3}\cup l_{4}$.
	Dado $r\in\mathbb{R}_{+}$, tomar $w$ como
	- **Caso 1.1)** Si $u_{0}\in l_{1}$, $w=(u_{1},u_{2}-\frac{r}{2})$, es claro que $u_{2}-\frac{r}{2}<0$, puesto $0=u_{2}$; además $d(u_{0},w)=\frac{r}{2}<r$. 
	  $\therefore$ Por lo tanto $B_{r}(u_{0})\subsetneq A$.
	- **Caso 1.2)** Si $u_{0}\in l_{2}$, basta tomar $w=(u_{1}+\frac{r}{2},u_{2})$.
	- **Caso 1.3)** Si $u_{0}\in l_{3}$, basta tomar $w=(u_{1},u_{2}+\frac{r}{2})$.
	- **Caso 1.4)** Si $u_{0}\in l_{4}$, basta tomar $w=(u_{1}-\frac{r}{2},u_{2})$.
- **Caso 2)** $u_{0}\in[0,1]\times[0,1]$. Sean $L_{1},L_{2},L_{3}$ y $L_{4}$ las rectas que se generan por $l_{1},l_{2},l_{3}$ y $l_{4}$ respectivamente.
	- **Caso 2.1)** Si $w$ no esta del mismo lado que $(0,1)\times(0,1)$ con respecto a $L_{1}$.
	  Así $d(w,L_{1})=d>0$ con $r=\frac{1}{2}d$ tenemos que $B_{r}(w)\not\subset A$ puesto que el punto $w_{0}=(w_{1},w_{2}+\frac{r}{2})\in B_{r}(w)$ pero $w_{0}\notin A$.
	$\therefore$ $(0,1)\times(0,1)\supset A^{\circ}$.

$\therefore$ $(0,1)\times(0,1)=A^\circ$.


$$A=[0,1]\times(0,1)$$
Así la frontera de $A$ $\subset\land\supset$ $=l_{1}\cup l_{2}\cup l_{3}\cup l_{4}$.

Sea $u\in l_{1}$, así $r_{1}=0$ y al menos $r_{2}>0$.

Dado $r\in\mathbb{R}_{+}$:
- **Caso 1)** Si $u\notin\{e_{2},\theta\}$, es decir $r_{1}$ y $r_{3}$ no son $0$. Tome $w=(u_{1}-\frac{r}{2},u_{2})\in B_{r}(u)\cap A^{c}$, es decir $B_{r}(u)\cap A^c\neq\emptyset$.