Metadata:
Fecha: 04-09-2023
Hora: 09:22
Título: Más ejercicios.

**Objetivo del día de hoy:**
- Plantear los problemas como *(PPL)* de la práctica #2.
- Resolver los problemas de *PL* por el método gráfico.

## Planteamiento de los problemas de la práctica #2.


## PL por el método gráfico.
### Problema 1.
$$\text{(PPL)}\begin{cases} \text{Max }Z=&4x_{1}+6x_{2}\\ \text{sujeto a}&2x_{1}+3x_{2}&\leq 6\\ &6x_{1}+4x_{2}&\leq 12\\ &-2x_{1}+2x_{2}&\leq 2\\ &x_{1},x_{2}&\geq0 \end{cases}$$
#### Solución.
- Despeje $1$: $$\begin{align*} 2x_{1}+3x_{2}&\leq 6\\ 3x_{2}&\leq6-2x_{1}\\ x_{2}&\leq\frac{6-2x_{1}}{3} \end{align*}$$

| $x_{1}$ | $x_{2}$ | Punto |
| --- | --- | --- |
| $1$ | $\frac{4}{3}$ | $(1,\frac{4}{3})$ |
| $2$ | $\frac{2}{3}$ | $(2,\frac{2}{3})$ |

- Despeje $2$: $$\begin{align*} 6x_{1}+4x_{2}&\leq12\\ 4x_{2}&\leq12-6x_{1}\\ x_{2}&\leq\frac{12-6x_{1}}{4} \end{align*}$$

| $x_{1}$ | $x_{2}$ | Punto |
| --- | --- | --- |
| $1$ | $1.5$ | $(1,1.5)$ |
| $0$ | $3$ | $(0,3)$ |

- Despeje $3$: $$\begin{align*} -2x_{1}+2x_{2}&\leq 2\\ 2x_{2}&\leq 2+2x_{1}\\ x_{2}&\leq\frac{2+2x_{1}}{2}\\ x_{2}&\leq1+x_{1} \end{align*}$$

| $x_{1}$ | $x_{2}$ | Punto |
| --- | --- | --- |
| $1$ | $2$ | $(1,2)$ |
| $2$ | $3$ | $(2,3)$ |

- Supongamos $Z=0$ entonces $$\begin{align*} Z=0\Rightarrow&0=4x_{1}+6x_{2}\\ 4x_{1}+6x_{2}&=0\\ 6x_{2}&=-4x_{1}\\ x_{2}&=\frac{-4x_{1}}{6} \end{align*}$$

| $x_{1}$ | $x_{2}$ | Punto |
| --- | --- | --- |
| $1$ | $\frac{-4}{6}$ | $(1,\frac{-4}{6})$ |
| $-4$ | $\frac{16}{6}$ | $(-4,\frac{16}{6})$ |

- Elaboramos la gráfica: ![[Pasted image 20230904095230.png]]
[Enlace](https://www.geogebra.org/calculator/zuqpbjqx).

$\therefore$ 


### Problema 2.
$$\text{(PPL)}\begin{cases} \text{Max }Z=&2x_{1}+x_{2}\\ \text{sujeto a}&4x_{1}+3x_{2}&\leq 20\\ &-x_{1}+2x_{2}&\leq 6\\ &4x_{1}-3x_{2}&\leq 8\\ &x_{1},x_{2}&\geq0 \end{cases}$$
#### Solución.
- Despeje $1$: $$\begin{align*} 4x_{1}+3x_{2}&\leq 20\\ 3x_{2}&\leq 20-4x_{1}\\ x_{2}&\leq \frac{20-4x_{1}}{3} \end{align*}$$
- 