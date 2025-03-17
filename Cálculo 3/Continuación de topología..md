Metadata:
Fecha: 25-08-2023
Hora: 11:15
Título: Continuación de topología.

## Apunte.
---
En $\mathbb{R}$ la topología usual es la que tiene como base $$\mathcal{B}=\Big\{ (a,b)\big|a,b\in\mathbb{R} \Big\}$$ también llamada topología del orden.

>[!faq] Proposición.
>Si $X$ es un conjunto con un orden $\prec$, entonces $$\mathcal{B}=\Big\{ (a,b)\big|a,b\in X \Big\}$$ es una base para una topología.
>Esta se llama topología del orden en $X$.
>>[!check] Demostración.
>>Ejercicio para examen.

##### Ejercicios para estudiar para el examen.
---
1. Si $<$ es el orden usual de $\mathbb{R}$ defínase en $\mathbb{R}^2$ la relación $\prec$ como: Para $u,v\in\mathbb{R}^2$ diremos que $$u\prec v$$ sí y sólo si $$u_2-u_1^2<v_2-v_1^2\ \lor\ u_2-u_1^2=v_2-v_1^2\ \land\ u_1<v_1$$ ¿$\prec$ es un orden en $\mathbb{R}^2$?.

2. Nuevamente $<$ es el orden usual de $\mathbb{R}$. Definamos para $a,b\in\mathbb{R}:a\prec b$ sí y sólo si $$a^2<b^2\ \lor\ a^2=b^2\ \land\ a<b$$
![[Pasted image 20230825114529.png|300]] ![[Pasted image 20230825114551.png|500]] ![[Pasted image 20230825114608.png|600]]


$$\mathbf{S}^1$$ $$D^2=\big\{ (a,b)\in\mathbb{R}^2:a^2+b^2<1 \big\}$$
>[!info] Definición.
>Sean $(X_1,\tau_1)$ y $(X_2,\tau_2)$ espacios topológicos y $f:X_1\longrightarrow X_2$ función. $f$ es continua sí y sólo si $$\forall v\in\tau_2:f^{-1}(v)\in\tau_1$$

>[!faq] Proposición.
>Si $\mathcal{B}_2$ es una base para la topología $\tau_2$ de $X_2$ $f:X_1\longrightarrow X_2$ es continua sí y sólo si $\forall {B}\in{B}_2:f^{-1}(B)$ es abierto en $X_1$.
>

$$\begin{align*} f:\overbrace{\mathbb{R}}^{X_1}&\longrightarrow\overbrace{\mathbb{R}}^{X_2}\\ x&\longmapsto f(x)=\begin{cases} 1,&\text{si }x\neq1\\ 0,&\text{si }x=1 \end{cases} \end{align*}$$
Si $X_1$ y $X_2$ tienen las topologías usuales sabemos que no es continua.
$$\begin{align*} f^{-1}\Big( \frac{1}{2},2 \Big)&=\Big\{ x\in\mathbb{R}\big|f(x)\in\big( \frac{1}{2},2 \big) \Big\}\\ &=\mathbb{R}\backslash\{1\}=(-\infty,1)\cup(1,\infty)\\ f^{-1}\Big( -\frac{1}{4},\frac{1}{4} \Big)&=\{1\}\ \text{No es abierto} \end{align*}$$
Por otro lado si $\tau_1=P(\mathbb{R})=\tau_2$, $f$ es continua.
 
 


###### Tareas.
---

