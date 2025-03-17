Metadata:
Fecha: 30-08-2023
Hora: 09:26
Título: (PPL) en forma gráfica.

*¡Buenos días!*
**Objetivos del día de hoy:**
- Resolver PPL en forma gráfica.
- Dudas de planteamiento.
- Asuntos generales.

>[!note] Nota.
>Propiedades de los (PPL): $$\text{(PPL)}\begin{cases} \text{1) Solución única}\\ \text{2) Solución óptima no finita }Z\rightarrow +\infty\\ \text{3) Solución multiple}\\\text{4) Sin solución} \end{cases}$$


## Ejercicio.
Solucionar en forma gráfica los siguientes (PPL).

#### Ejercicio 1.
$$\text{(PPL)}\begin{cases} \text{Max }Z=&2x_1+4x_{2}\\ \text{s. a.}&x_1+2x_{2}&\leq5\\ &x_{1}+x_{2}&\leq4\\ &x_{1},x_{2}&\geq0 \end{cases}$$

$$\begin{align*} x_{1}+x_{2}&\leq5\\ 2x_{2}&=5-x_{1}\\ x_{2}&\leq\frac{5-x_{1}}{2} \end{align*}$$
| $x_1$ | $x_2$ | Punto |
| --- | --- | --- |
| $0$ | $x_{2}\leq\frac{5}{2}$ | $(0,\frac{5}{2})$ |
| $1$ | $x_{2}\leq2$ | $(1,2)$ |

$$\begin{align*} x_{1}+x_{2}&\leq4\\x_{2}&\leq4-x_{1} \end{align*}$$

| $x_{1}$ | $x_{2}$ | Punto |
| --- | --- | --- |
| $0$ | $x_{2}\leq4$ | $(0,4)$ |
| $1$ | $x_{2}\leq 3$ | $(1,3)$ |

Ahora, con $Z$ $$\begin{align*} Z&=2x_{1}+4x_{2}\\ \text{si }Z=0&\Rightarrow0=2x_{1}+4x_{2}\\ x_{2}&=\frac{-2x_{1}}{4} \end{align*}$$

| $x_1$ | $x_{2}$ | Punto |
| --- | --- | --- |
| $1$ | $x_{2}\leq \frac{-1}{2}$ | $(1,\frac{-1}{2})$ |
| $2$ | $x_{2}\leq-1$ | $(2,-1)$ |
![[Pasted image 20230830095513.png|650]]


#### Ejercicio 2.
$$\text{(PPL)}\begin{cases} \text{min }Z=&-3x_{1}-2x_{2}\\ \text{s. a.}&x_{1}+x_{2}&=10\\ &x_{1}&\geq4\\ &x_{1},x_{2}&\geq0 \end{cases}$$
$$\begin{align*} x_{1}+x_{2}&=10\\ x_{2}&=10-x_{1} \end{align*}$$

| $x_1$ | $x_{2}$ | Punto |
| --- | --- | --- |
| $0$ | $x_{2}=10$ | $(0,10)$ |
| $1$ | $x_{2}=9$ | $(1,9)$ |

Ahora, con $Z$ $$\begin{align*} Z&=-3x_{1}-2x_{2}\\ \text{si }Z=0&\Rightarrow0=-3x_{1}-2x_{2}\\ 2x_{2}&=-3x_{1}\\ x_{2}&=\frac{-3x_{1}}{2} \end{align*}$$

| $x_1$ | $x_2$ | Punto |
| --- | --- | --- |
| $1$ | $x_{2}=\frac{-3}{2}$ | $(1,\frac{-3}{2})$ |
| $2$ | $x_{2}=-3$ | $(2,-3)$ |

#### Ejercicio 3.
$$\text{(PPL)}\begin{cases} \text{Min }Z=&x_1+2x_{2}\\ \text{s. a.}&x_1-3x_{2}&\leq6\\ &2x_{1}+4x_{2}&\geq8\\ &x_{1}-3x_{2}&\geq-6\\ &x_{1},x_{2}&\geq0 \end{cases}$$
$$\begin{align*} x_{1}-3x_{2}&\leq6\\ 3x_{2}&\leq6-x_{1}\\ x_{2}&\leq\frac{6-x_{1}}{3} \end{align*}$$

| $x_{1}$ | $x_{2}$ | Punto |
| --- | --- | --- |
| $0$ | $x_{2}\leq3$ | $(0,3)$ |
| $2$ | $x_{2}\leq\frac{4}{3}$ | $(2,\frac{4}{3})$ |
$$\begin{align*} 2x_{1}+4x_{2}&\geq8\\ 4x_{2}&\geq8-2x_{1}\\ x_{2}&\geq\frac{8-2x_{1}}{4} \end{align*}$$

| $x_{1}$ | $x_{2}$ | Punto |
| --- | --- | --- |
| $0$ | $2$ | $(0,8)$ |
| $4$ | $1$ | $(4,1)$ |
$$\begin{align*} x_{1}+6&\geq3x_{2}\\ x_{2}&\leq\frac{x_{1}+6}{3}  \end{align*}$$

| $x_{1}$ | $x_{2}$ | Punto |
| --- | --- | --- |
| $3$ | $3$ | $(3,3)$ |
| $6$ | $4$ | $(6,4)$ |
Ahora con $Z$ $$\begin{align*} Z&=x_{1}+2x_{2}\\ \text{si }Z=0&\Rightarrow0=x_{1}+2x_{2}\\ 2x_{2}&=-x_{1}\\ x_{2}&=\frac{-x_{1}}{2} \end{align*}$$

| $x_{1}$ | $x_{2}$ | Punto |
| --- | --- | --- |
| $-2$ | $1$ | $(-2,1)$ |
| $1$ | $\frac{-1}{2}$ | $(1,\frac{-1}{2})$ |
![[Pasted image 20230830113734.png|650]]

