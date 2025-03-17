Metadata:
18-08-2023
09:11
Modelos de Programación Lineal.

## Apunte.
---
>[!info] Definición. 
>Una función $f:\mathbb{R}^n\rightarrow\mathbb{R}$ es lineal sí y sólo si existen constantes $c_1,c_2,\ldots,c_n$ tal que $$f(x_1,x_2,\ldots,x_n)=c_1x_1+c_2x_2+\ldots+c_nx_n$$

>[!info] Definición.
>Una expresión de la forma $$a_1x_1+\ldots+a_nx_n\leq b$$ o $$a_1x_1+\ldots+a_nx_n\geq b$$ se llaman desigualdades lineales.

>[!info] Definición. *Problema de Programación Lineal (PPL)*.
>Un Problema de Programación Lineal (PPL) consiste en la búsqueda del óptimo (maximizar o minimizar) una función lineal de $n$ variables $f:\mathbb{R}^n\rightarrow\mathbb{R}$ llamada función objetivo sujeta a ciertas condiciones llamadas restricciones lineales.

![[Pasted image 20230818092758.png]]


#### Modelo de PL en forma matricial.
---
$$\begin{cases} \text{Optimizar}&Z=CX\\ \text{s. a }&AX\leq b\\ &X\geq0 \end{cases}$$
$$C=[c_1,\ldots,c_n]_{1\times n}\rightarrow\text{vector de costos}$$ $$X=\begin{bmatrix} x_1\\ \vdots\\ x_n \end{bmatrix}_{n\times 1}\rightarrow\text{vector de las variables de decisión}$$ 
$$A=\begin{bmatrix} a_{11}&a_{12}&\ldots&a_{1n}\\ \vdots&\vdots& &\\ a_{m1}&a_{m2}&\ldots&a_{mn} \end{bmatrix}_{m\times n}\rightarrow\text{matriz de coeficientes tecnológicos ó matriz de insumos}$$ $$b=\begin{bmatrix} b_1\\ \vdots\\ b_m \end{bmatrix}_{m\times 1}\rightarrow\text{vector de recursos ó vector disponibilidad}$$


#### Propiedades de los (PPL).
---
1. Linealidad de la función objetivo y de las restricciones.
2. No negatividad de las variables.
3. Divisibilidad: los valores de las variables pueden ser fraccionarios.
4. Homogeneidad.

$$\text{(PPL)}\begin{cases} \text{Optimizar}&Z=\sum_{j=1}^{n}c_jx_j\\ \text{s. a}&\sum_{j=1}^na_{ij}x_j\leq b_i&i\in\overline{1,m}\\ &x_j\geq0&i\in1,\ldots,m\\&&i\in[1,\ldots,m] \end{cases}$$


###### Tareas.
---

