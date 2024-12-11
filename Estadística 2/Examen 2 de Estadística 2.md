
- Kristoffer Van Steemberghe Luján
- 319206463
- 26/04/2024


## Ejercicio 1.

Se llevó a cabo un diseño completamente aleatorizado para comparar los efectos de cinco estímulos en los tiempos de reacción y se obtuvieron los siguientes resultados:

| A     | B     | C     | D     | E     |
| ----- | ----- | ----- | ----- | ----- |
| $0.8$ | $0.7$ | $1.2$ | $1.0$ | $0.6$ |
| $0.6$ | $0.8$ | $1.0$ | $0.9$ | $0.4$ |
| $0.6$ | $0.5$ | $0.9$ | $0.9$ | $0.4$ |
| $0.5$ | $0.5$ | $1.2$ | $1.1$ | $0.7$ |
| $0.6$ | $1.3$ | $0.7$ | $0.3$ |       |
| $0.9$ | $0.8$ |       |       |       |
| $0.7$ |       |       |       |       |
1. Realiza un análisis de varianza (ANOVA) y evalúa si existe una diferencia significativa en los tiempos medios de reacción entre los cinco estímulos.

2. Compara los estímulos $B$ y $C$ para determinar si hay una disparidad en los tiempos medios de reacción.

**Solución:**

Primero, vamos a calcular la media de los tiempos de reacción para cada estímulo.

| A          | B          | C         | D          | E      |
| ---------- | ---------- | --------- | ---------- | ------ |
| $0.8$      | $0.7$      | $1.2$     | $1.0$      | $0.6$  |
| $0.6$      | $0.8$      | $1.0$     | $0.9$      | $0.4$  |
| $0.6$      | $0.5$      | $0.9$     | $0.9$      | $0.4$  |
| $0.5$      | $0.5$      | $1.2$     | $1.1$      | $0.7$  |
| $0.6$      | $1.3$      | $0.7$     | $0.3$      |        |
| $0.9$      | $0.8$      |           |            |        |
| $0.7$      |            |           |            |        |
| $\mu=0.67$ | $\mu=0.76$ | $\mu=1.0$ | $\mu=0.84$ | $0.52$ |
con $\overline{X}=0.7629$

Después, calculamos primero la suma de cuadrados total:
$$\sum\limits(X_{ij}-\overline{X})^{2}=1.78296307$$

Luego la suma de cuadrados entre tratamientos:
$$\sum\limits n_{i}(\overline{X}_{i}-\overline{X})^{2}=0.60726907$$
Ahora calculamos la suma de cuadrados dentro de los tratamientos:
$$SCT-SCE=1.175694$$
Luego revisamos los grados de libertad entre tratamientos:
$$k-1=5-1=4$$
y también los grados de libertad dentro de los tratamientos:
$$N-k=27-5=22$$
Finalmente obtenemos las varianzas, primero la que es entre tratamientos:
$$\frac{SCE}{\text{g. l. entre tratamientos}}=\frac{0.60726907}{4}=0.15181727$$
y la varianza dentro de los tratamientos:
$$\frac{SCD}{\text{g. l. dentro de tratamientos}}=\frac{1.755694}{22}=0.05344064$$

Posteriormente definimos el estadístico de la prueba, el cual sería $F=\frac{\text{Varianza entre tratamientos}}{\text{Varianza dentro de tratamientos}}$ y compararemos con el valor crítico de $F$ para determinar la significancia:
$$F=\frac{0.15181727}{0.05344064}=2.84085815$$

Ahora, comparamos con la tabla de valores críticos para $F$ con $\alpha=0.5$ con $4$ y $22$ grados de libertad, vemos que $F_{\text{Crítico}}=2.98$. Como $F<F_{\text{Crítico}}$, no rechazamos la hipótesis nula.

Posteriormente, para comparar los estímulos $B$ y $C$, usaremos la prueba $t-\text{Student}$ para muestras independientes.

$$\begin{align*} \text{Estímulo }B&:\ \overline{X}_{B}=0.76,\ \ \ s_{B}=0.294392,\ \ \ n_{B}=6\\ \text{Estímulo }C&:\ \overline{X}_{C}=1.0,\ \ \ \ s_{C}=0.212132,\ \ \ n_{C}=5 \end{align*}$$
$$\begin{align*} t&=\frac{\overline{X}_{B}-\overline{X}_{C}}{\sqrt{\frac{s_{B}^{2}}{n_{B}}+\frac{s_{C}^{2}}{n_{C}}}}\\ &=\frac{0.76-1.0}{\sqrt{\frac{0.086666}{6}+\frac{0.044999}{5}}}\\ &=\frac{-0.24}{\sqrt{0.023444}}\\ &=\frac{-0.24}{0.153114}\\ t&=-1.567459 \end{align*}$$
Para $\alpha=0.5$ y $df=n_{B}+n_{C}-2=6+5-2=9$, el valor crítico de $t$ es aproximadamente es $\pm2.262$, por lo que $|t|<2.262$, no rechazamos la hipótesis nula.

$\therefore$ No hay una diferencia significativa entre los estímulos $B$ y $C$.


## Ejercicio 2.
Dado que es de esperar que el tiempo medio de reacción pueda variar entre las personas, se podría haber llevado a cabo el experimento del ejercicio anterior de manera más eficiente utilizando un diseño de bloques aleatorizados, con las personas como bloques. Por lo tanto, se llevó a cabo un nuevo experimento con la participación de cuatro personas, y cada una de ellas fue expuesta a los cinco estímulos en un orden aleatorio. Los tiempos de reacción (en segundos) se presentan en la siguiente tabla.

| Sujeto | A     | B     | C     | D     | E     |
| ------ | ----- | ----- | ----- | ----- | ----- |
| 1      | $0.7$ | $0.8$ | $1.0$ | $1.0$ | $0.5$ |
| 2      | $0.6$ | $0.6$ | $1.1$ | $1.0$ | $0.6$ |
| 3      | $0.9$ | $1.0$ | $1.2$ | $1.1$ | $0.6$ |
| 4      | $0.6$ | $0.8$ | $0.9$ | $1.0$ | $0.4$ |
Realiza un análisis de varianza (ANOVA) para evaluar las diferencias en los tiempos medios de reacción para los cuatro estímulos.

**Solución:**

Calculamos la media de los tiempos de reacción

| Sujeto | A                | B                | C                | D                | E                |
| ------ | ---------------- | ---------------- | ---------------- | ---------------- | ---------------- |
| 1      | $0.7$            | $0.8$            | $1.0$            | $1.0$            | $0.5$            |
| 2      | $0.6$            | $0.6$            | $1.1$            | $1.0$            | $0.6$            |
| 3      | $0.9$            | $1.0$            | $1.2$            | $1.1$            | $0.6$            |
| 4      | $0.6$            | $0.8$            | $0.9$            | $1.0$            | $0.4$            |
|        | $\overline{X}_A$ | $\overline{X}_B$ | $\overline{X}_C$ | $\overline{X}_D$ | $\overline{X}_E$ |

Planteamos nuestras hipótesis:
- $H_{0}:$ No hay diferencias significativas en los tiempos medios de reacción entre los estímulos.
- $H_{1}:$ Existen diferencias significativas en los tiempos medios de reacción entre los estímulos.

Calculamos la media general de los datos:
$$\overline{X}=\frac{\sum\limits X_{ij}}{N}=0.82$$
Luego hacemos la suma de cuadrados total:
$$=1.012$$
Hacemos la suma de cuadrados entre grupos:
$$=0.787$$
Calculamos la suma de cuadrados dentro de grupos:
$$=0.225$$
Cálculamos los grados de libertad y medias cuadráticas:
$$GLG=4,\ \ \ GLD=15$$
$$MCG=0.196,\ \ \ MCD=0.015$$
Usaremos el estadístico $F$:
$$F=\frac{MCG}{MCD}=\frac{0.196}{0.015}=13.0666$$
Comparando con el valor crítico de $F$ para un nivel de significancia de $\alpha=0.05$, rechazamos $H_{0}$ porque $F>F_\text{Crítico}$.

$\therefore$ Existen diferencias significativas en los tiempos medio de reacción entre los estímulos.