Metadata:
Fecha: 28-08-2023
Hora: 09:14
Título: Método gráfico.

*¡Feliz inicio de semana!*

**Objetivo del día de hoy:** Solucionar problemas de Programación Lineal por el Método Gráfico.

$$\text{(PPL)}\begin{cases} \text{Max }Z=&3x_1+2x_2\\\text{s. a.}&-2x_1+x_2&\leq1&\text{--- 1}\\ &x_1&\leq 2&\text{--- 2}\\ &x_1+x_2&\leq 3&\text{--- 3}\\ &x_1,x_2&\geq0 \end{cases}$$

$$\begin{matrix} -2x_1+x_2\leq1\\ x_2\leq1+2x_1 \end{matrix}$$
| $x_1$ | $x_2$ | Punto |
| --- | --- | --- |
| $0$ | $x_2\leq 1$ | $(0,1)$ |
| $1$ | $x_2\leq 3$ | $(1,3)$ |

En este caso la recta tiene dirección hacía abajo por el $\leq$.


$$x_1+x_2\leq3\Longrightarrow x_2\leq 3-x_1$$

| $x_1$ | $x_2$ | Punto |
| --- | --- | --- |
| $0$ | $x_2\leq 3$ | $(0,3)$ |
| $1$ | $x_2\leq 0$ | $(3,0)$ |

![[Pasted image 20230828092821.png|450]]


$$z=3x_1+2x_2$$ Si $z=0\Rightarrow 0=3x_1+2x_2\Rightarrow 2x_2=-3x_1\Rightarrow x_2=-\frac{3}{2}x_1$

| $x_1$ | $x_2$ | Punto |
| --- | --- | --- |
| $0$ | $0$ | $(0,0)$ |
| $2$ | $-3$ | $(2,-3)$ |


## Problema 2.
Problema 2 de los [[Problemas 4, 5, 6 y 7 como (PPL).]], [[Problemas 8, 9, 10 y 11 como (PPL).]] y [[Problemas 11, 12 y 13 como (PPL).]].

$$\text{(P)}\begin{cases} \text{Max }Z=&24x_1+15x_2\\ \text{s. a.}&3x_1+x_2&\leq1500\\ &x_1&\leq450\\ &x_2&\leq 750\\ &x_1,x_2&\geq0  \end{cases}$$ $$\text{(P)}\begin{cases} \text{Max }Z=&24x_1+15x_2\\ \text{s.a }&3x_1&=x_2\\ &x_1+x_2&\leq1500\\ &x_1&\leq450\\ &x_2&\leq 750\\ &x_1,x_2&\geq0 \end{cases}$$
![[Pasted image 20230828102746.png|400]]



## Otro ejemplo.
$$\text{(P)}\begin{cases} \text{Max }Z=&3x_1+2x_2\\ \text{s. a.}&x_1-x_2&\leq 1&\text{--- 1}\\ &x_1+x_2&\geq3&\text{--- 2}\\ &x_1,x_2&\geq 0 \end{cases}$$ $$\text{(P)}\begin{cases} \text{Min }Z=&x_1+2x_2\\ \text{s. a.}&x_1-3x_2&\leq6\\ &2x_1+4x_2&\geq8\\ &x_1-3x_2&\geq-6\\ &x_1,x_2&\geq0 \end{cases}$$
1. $$\begin{matrix} x_1-x_2\leq 1\\ x_1\leq 1+x_2 \end{matrix}$$

| $x_1$ | $x_2$ | Punto |
| --- | --- | --- |
| $x_1\leq 1$ | $0$ | $(1,0)$ |
| $x_1\leq 2$ | $1$ | $(2,1)$ |

2. $$\begin{matrix} x_1+x_2\geq3\\ x_2\geq3-x_1 \end{matrix}$$

| $x_1$ | $x_2$ |
| --- | --- |
| $0$ | $x_2\geq3$ |
| $1$ | $x_2\geq0$ |


