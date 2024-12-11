Metadata:
Fecha: 06-09-2023
Hora: 11:35
Título: Puntos de adherencia.

>[!info] Definición.
>Un punto $u_{0}\in\mathbb{R}^{n}$ es un punto de adherencia de un conjunto $A\subset\mathbb{R}^{n}$ si y sólo si para cada $r\in\mathbb{R}_{+}$ $B_{r}(u_{0})\cap A\neq\emptyset$.
>El conjunto de puntos de adherencia se llama cerradura del conjunto $A$ y se denota por $\overline{A}$, $cl(A)$, $Cl(A)$.


#### Ejemplos .
1. En $\mathbb{R}_{1}$ tomar $A=[1,2]\cup[-1,0]\cup\{\frac{1}{2}\}$ así $\frac{1}{2}$ es punto de adherencia de $A$. Puesto que para $r\in\mathbb{R}_{+}$, $\frac{1}{2}\in B_{r}(\frac{1}{2})$ y $\frac{1}{2}\in A$.

>[!faq] Proposición.
>Si $A\subset\mathbb{R}^{n}$ entonces $A\subset\overline{A}$.
>>[!check] Demostración.
>>Ejercicio segundo parcial.

![[Pasted image 20230906114516.png|550]]
Si $u_{0}\in(0,1)\backslash\{\frac{1}{2}\}$, tome $r=\frac{1}{2}\min\{u_{0},1-u_{0},|\frac{1}{2}-u_{0}|\}$ $B_{r}(u_{0})\cap A=\emptyset$.
Si $u_{0}>2$, tomar $r=\frac{u_{0}-2}{2}$, así $B_{r}(u_{0})\cap A=\emptyset$.
Si $u_{0}<-1$, tome $r=\frac{-1-u_{0}}{2}$, así $B_{r}(u_{0})\cap A=\emptyset$.
$\therefore$ $\overline{A}=A$.

2. $\overline{\emptyset}=\emptyset$.

3. $\overline{\mathbb{R}^{n}}=\mathbb{R}^{n}$.

4. $\overline{\mathbb{Q}}=\mathbb{R}$ en $\mathbb{R}$.
>[!note] Nota.
>$X$ e. t. y $A\subset X$.
>$A$ es denso en $X$ si $\overline{A}=X$.

5. $\overline{\mathbb{N}}=\mathbb{N}$ en $\mathbb{R}$.

6. $\overline{\mathbb{Z}}=\mathbb{Z}$ en $\mathbb{R}$.

7. $\overline{\mathbb{R}\backslash \mathbb{Q}}=\mathbb{R}$.

8. En $\mathbb{R}^{2}$, tome $A=\mathbb{Q}\times\mathbb{N}$.
![[Pasted image 20230906115832.png|350]]


>[!faq] Pregunta.
>$$ ¿ \overline{A\times B}=\overline{A}\times\overline{B} ?$$

9. Tome $A=\mathbb{Q}\cap[0,1]$ y $B=[0,1]\backslash A$.
En $\mathbb{R}^{2}$, ¿quién es $\overline{A\times B}$?


>[!info] Teorema.
>Un conjunto $A\subset \mathbb{R}^{n}$ es cerrado si y solo si $\overline{A}=A$.

>[!info] Definición.
>Un conjunto $B\subset \mathbb{R}^{n}$ es cerrado siempre que $\mathbb{R}^{n}\backslash B$ sea abierto.

>[!info] Definición.
>Un punto $u_{0}\in\mathbb{R}^{n}$ es punto aislado de $A\subset \mathbb{R}^{n}$ si existe $r\in\mathbb{R}_{+}$ tal que $B_{r}(u_{0})\cap A=\{u_{0}\}$.

Una función con dominio de la forma $$\prod_{\alpha\in J}A_{\alpha}$$ se llama función de varias variables.

>[!info] Definición.
>Si $A\subset \mathbb{R}^{n}$, $f:A\longrightarrow\mathbb{R}^{n}$ una función. Para $x_{0}\in\mathbb{R}^{n}$, $f$ tiene como límite a $L\in\mathbb{R}^{n}$, cuando $x$ tiende a $x_{0}$ si y solo si $\forall \epsilon\in\mathbb{R}_{+}$, $\exists\delta\in\mathbb{R}_{+}:x\in A\land 0<||x-x_{0}||<\delta=>||f(x)-L||<\epsilon$.
>

>[!faq] Proposición.
>Si $f$ tiene límite cuando $x$ tiende a $u$ entonces es único.
>>[!check] Demostración.
>>Ejercicio segundo parcial.

Como el límite es único, podemos denotarlo como $$\lim_{x\to x_{0}}f(x)=L$$
Recuerda que $f:A\subset\mathbb{R}^{n}\rightarrow\mathbb{R}^{n}$ es continua si para todo abierto (bola abierta) en $\mathbb{R}^{n}$, $B$, su imagen inversa, $f^{-1}(B)$, es abierto en $\mathbb{R}^{n}$.

>[!info] Teorema.
>Sea $f:A\subset\mathbb{R}^{n}\longrightarrow\mathbb{R}^{n}$ una función entonces: $f$ es continua si y solo si $\forall a_{0}\in A$ $$\lim_{a\to a_{0}}f(a)=f(a_{0})$$

