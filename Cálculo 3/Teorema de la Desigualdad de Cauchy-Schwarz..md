Metadata:
Fecha: 30-08-2023
Hora: 11:22
Título: Teorema de la Desigualdad de Cauchy-Schwarz.

## Teorema de la Desigualdad de Cauchy-Schwarz.
Si $a_1,\ldots,a_n,b_1,\ldots,b_n\in\mathbb{R}$, entonces $$\Bigg( \sum\limits_{k=1}^{n}a_{k}b_{k} \Bigg)^{2}\leq \Bigg( \sum\limits_{j=1}^{n}a_{j}^{2} \Bigg)\sum\limits_{i=1}^{n}b_{i}^{2}$$
Más aún, si para algún $i\in\{ 1,\ldots,n \}$ se tiene que $a_{i}\neq0$, se tendrá la igualdad si y solo si un real $t\in\mathbb{R}$ tal que $t(a_1,\ldots,a_n)=(b_1,\ldots,b_n)$.

### Demostración.
Sabemos que la suma de números no negativos siempre es no negativo. Entonces $$\sum\limits_{i=1}^{n}(a_{i}x+b_{i})^{2}\geq0\ldots\ldots(\text{I})$$ para cualquier $x\in\mathbb{R}$. Esto será $0$ si y solo si $\forall i\in\{ 1,\ldots,n \}:(a_{i}x+b_{i})^{2}=0$ si y solo si $\forall i\in\{1,\ldots,n\}:a_{i}x+b_{i}=0$.
Tome $A=\sum\limits a_{i}^{2}$, $B=\sum\limits a_{i}b_{i}$ y $C=\sum\limits b_{i}^{2}$, así $(\text{I})$ se transforma en $$Ax^{2}+2Bx+C\geq0\ldots\ldots(\text{II})$$
Si $A>0$, tomemos $x=\frac{-B}{A}$. Así tendremos que $B^{2}-AC\leq0$ por lo cual $$\bigg(\sum\limits a_{i}b_{i}\bigg)^{2}\leq\bigg( \sum\limits a_{i}^{2} \bigg)\sum\limits b_{i}^{2}$$
Si $A=0$, implica que $a_{i}^{2}=0\ \forall i\in\{1,\ldots,n\}$.
Entonces $A=0$ y $B=0$.
Concluyendo que $$\bigg(\sum\limits a_{i}b_{i}\bigg)^{2}\leq\bigg( \sum\limits a_{i}^{2} \bigg)\bigg( \sum\limits b_{i}^{2} \bigg)$$


Como vimos el producto interno en $\mathbb{R}^4$ se define como $u\cdot v=u\text{ I }v^{\top}$, donde $\text{I}\in\mathcal{M}_{n}(\mathbb{R})$ y $v^{\top}$ es el vector columna asociado a $v$.

¿Se puede cambiar $\text{I}$ por otra matriz?
La respuesta es afirmativa. Bastará tomar $A\in\mathcal{M}_{n}(\mathbb{R})$ con $T_{A}$ sea **bilineal simétrica**; es decir, $A$ es simétrica y positiva definida.


#### Propiedades del producto interno en $\mathbb{R}^{n}$.
Sea $\theta$ el origen:
1. $\theta\cdot v=0$ $\forall v\in\mathbb{R}^n$.
2. $v\cdot v\geq0\land (v\cdot v=0\text{ si y solo si }v=\theta)$ $\forall v\in\mathbb{R}^n$.
3. $u\cdot v=v\cdot u$ $\forall u,v\in\mathbb{R}^n$.
4. Si $\alpha,\beta\in\mathbb{R}$ y $u,v,w\in\mathbb{R}^n$ $$\begin{align*} u\cdot(\alpha v+\beta w)&=\alpha u\cdot v+\beta u\cdot w\\ (\alpha u+\beta v)\cdot w&=\alpha u\cdot w+\beta v\cdot w \end{align*}$$
5. $(u+v)\cdot(u+v)=u^{2}+v^{2}+2u\cdot v$ $\forall u,v\in\mathbb{R}^n$.

$T:\mathbb{R}^n\longrightarrow\mathbb{R}^n$ lineal si y solo si $\forall \alpha,\beta\in\mathbb{R}$, $\forall u,v\in\mathbb{R}^n$ $$T(\alpha u+\beta v)=\alpha\ T(u)+\beta\ T(v)$$ $$\begin{align*} B:\mathbb{R}^{n}\times\mathbb{R}^{n}&\longrightarrow\mathbb{R}^{n}\\ (u,v)&\longmapsto B(u,v)=(u_{0},v_{0}) \end{align*}$$

##### Demostración.
1. Es claro que $\theta\text{ I }v=\theta\begin{pmatrix} v_{1}\\ \vdots\\ v_{n} \end{pmatrix}=0$.
2. Hay dos pasos:
	1. Para $v\in\mathbb{R}^{n}$, tenemos que $$v\cdot v=v\text{ I }v^{\top}=\sum\limits v_{i}^{2}\geq0$$ puesto la suma de números no negativos es no negativa.
	2. Si $v\in\mathbb{R}$ con $v^{2}=0$. Entonces $\sum\limits v_{i}^{2}=0$. Pero sabemos que la suma de no negativos es cero si son cero todos los sumandos. Esto implica $\forall i\in\{1,\ldots,n\}a_{i}=0$. Y si $v\in\mathbb{R}^n$ es $v=\theta$, se tiene que $\theta\cdot\theta=0$, así $v^{2}=0$. 
3. Use la propiedad de bilinealidad.
4. Use la propiedad de bilinealidad.
5. Sean $u,v\in\mathbb{R}^{n}$, entonces $$(u+v)\cdot(u+v)=u\cdot(u+v)+v\cdot(u+v)$$ por *4.*, más aún $$u\cdot(u+v)=u^{2}+u\cdot v\land v\cdot(u+v)=u\cdot v+v^{2}$$ por *4.*. Entonces $$(u+v)\cdot(u+v)=u^{2}+v^{2}+2u\cdot v$$


#### Propiedades de la norma.
La norma en $\mathbb{R}^{n}$ la definimos como $$\forall v\in\mathbb{R}^{n}:\ ||v||=(v\cdot v)^{\frac{1}{2}}$$
Esta tiene las siguientes propiedades:
$\forall u,v\in\mathbb{R}^{n}$, $\forall \alpha,\beta\in\mathbb{R}$ 
1. $||u||\geq0\ \land\ \big(||u||=0 \text{ si y solo si }u=\theta \big)$.
2. $||\alpha u||=|\alpha|\ ||u||$.
3. $||u-v||=||v-u||$.
4. $|u\cdot v|\leq||u||\ \ ||v||$.
5. $||u+v||\leq||u||+||v||$.

##### Demostración.
1. Como $||u||=(u\cdot u)^{\frac{1}{2}}\geq0$ y $||u||=0$ si y solo si $u\cdot u=0$ si y solo si $u=\theta$.
2. $||\alpha u||=\big( \sum\limits a^{2}u_{i}^{2} \big)^{\frac{1}{2}}=\big( \alpha^{2}\sum\limits u_{i}^{2} \big)^{\frac{1}{2}}=(\alpha^{2})^{\frac{1}{2}}\big( \sum\limits u_{i}^{2} \big)^{\frac{1}{2}}=|a|\ \ ||u||$.
3. Note que $$\begin{align*} (u-v)\cdot(u-v)&=u^{2}+v^{2}-2u\cdot v\\ (v-u)\cdot(v-u)&=u^{2}+v^{2}-2v\cdot u\\ &=u^{2}+v^{2}-2u\cdot v \end{align*}$$
4. Desigualdad de  *Cauchy-Schwarz*.
5. Desigualdad del triángulo ![[Pasted image 20230830121759.png|350]] como $$\begin{align*} ||u+v||^{2}&=(u+v)\cdot(u+v)&=||u||^{2}+||v||^{2}+2u\cdot v\\ &\leq||u||^{2}+||v||^{2}+2||u||\ ||v||&=\Big( ||u||+||v|| \Big)^{2} \end{align*}$$ y $||u||+||v||\geq0$, $||u+v||\geq0$ se tiene que $$||u+v||\leq||u||+||v||$$


Sabemos que $A\subset\mathbb{R}^{n}$ es abierto en $\mathbb{R}^{n}$ en la topología usual, si $\forall a\in A,\exists r\in\mathbb{R}_{+}$ tal que $B_{r}(a)\subset A$.
![[Pasted image 20230830123358.png|350]]


>[!info] Definición. Sea $A\subset\mathbb{R}^n$ y $a\in \mathbb{R}^{n}$, diremos que
>1. $a$ es un punto inferior de $A$ si existe $r\in\mathbb{R}_{+}$ tal que $B_{r}(a)\subset A$. El conjunto de puntos inferiores de $A$ se denota por $A^{\circ}$, $\text{Inf}(A)$.
>2. $a$ es un punto frontera de $A$ si para todo $r\in\mathbb{R}_{+}$ $B_{r}^{*}(a)\cap A\neq \emptyset$ y $B_{r}^{*}(a)\cap(\mathbb{R}^{n}\backslash A)\neq\emptyset$, donde $B_{r}^{*}(a)=B_{r}(a)\backslash\{a\}$. El conjunto de puntos frontera de $A$ se denota por $\partial A$, $\text{fr}\ A$.
>3. $a$ es un punto exterior de $A$ si existe $r\in\mathbb{R}_{+}$ tal que $B_{r}(a)\subset\mathbb{R}^{n}\backslash A$.


Para $A=[0,1]\times(0,1)$, tenemos que $A^{\circ}=(0,1)\times(0,1)$. En efecto, si tomamos $u\in A^{\circ}$, cumplirá que $0<u_{1}<1$ y $0<u_{2}<1$.

Tomando $l_{1}$ el segmento de recta que une $\theta$ con $e_{1}$.
Tomando $l_{2}$ el segmento de recta que une
Tomando $l_{3}$ el segmento de recta que une
Tomando $l_{4}$ el segmento de recta que une
*Imagen*

Sea $r_{i}$



 
 

