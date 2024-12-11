
- Kristoffer Van Steemberghe Luján
- 319206463
- 20/05/2024


## Ejercicio 1.

**Solución (a):**

Para estimar la relación entre el $GPA$ y el $ACT$, realizaremos un análisis de regresión lineal simple utilizando los datos proporcionados. Calcularemos las estimaciones para la pendiente ($\beta_{1}$) y el intercepto ($\beta_{0}$) en la ecuación $GPA=\beta_{0}+\beta_{1}\cdot ACT$.

Primero calcularemos las sumas necesarias:
$$\begin{align*} \sum\limits x_{i}&=21+24+26+27+29+25+25+30=207\\ \sum\limits y_{i}&=2.8+3.4+3.0+3.5+3.6+3.0+2.7+3.7=25.7\\ \sum\limits x_{i}y_{i}&=21(2.8)+24(3.4)+26(3.0)+27(3.5)+29(3.6)+25(3.0)+25(2.7)+30(3.7)=670.80\\ \sum\limits x_{i}^{2}&=21^{2}+24^{2}+26^{2}+27^{2}+29^{2}+25^{2}+25^{2}+30^{2}=5413\\ n&=8 \end{align*}$$
Ahora aplicamos la fórmula de mínimos cuadrados:
$$\begin{align*} \beta_{1}&=\dfrac{\big{(}n(\sum\limits x_{i}y_{i})-(\sum\limits x_{i})(\sum\limits y_{i})\big{)}}{\big{(}n(\sum\limits x_{i}^{2})-(\sum\limits x_{i})^{2}\big{)}}\\ &=\dfrac{\big{(}8(670.80)-(207)(25.7)\big{)}}{\big{(}8(5413)-(207)^{2}\big{)}}\\ &=\dfrac{46.5}{455}\\ &=0.102197 \end{align*}$$
$$\begin{align*} \beta_{0}&=\dfrac{\big{(}\sum\limits y_{i}-\beta_{1}(\sum\limits x_{i})\big{)}}{n}\\ &=\dfrac{\big{(}25.7-0.102197(207)\big{)}}{8}\\ &=\dfrac{4.545221}{8}\\ &=0.568152 \end{align*}$$
Por lo tanto, la ecuación de regresión estimada es:
$$GPA=0.568152+0.102197\cdot ACT$$
La pendiente positiva ($0.102197$) indica que existe una relación positiva entre el $GPA$ y el $ACT$, es decir, a medida que aumenta el puntaje $ACT$, también aumenta el $GPA$ predicho.
El intercepto $(0.568152)$ representa el $GPA$ predicho cuando el puntaje $ACT$ es cero.

Si el puntaje $ACT$ aumenta en $5$ puntos, el $GPA$ predicho aumentará en $0.102197\times 5=0.510985$ puntos.


**Solución (b):**

Vamos a usar la fórmula del intervalo de confianza para una predicción:
$$\hat{y}\pm t_{\dfrac{\alpha}{2},n-2}\cdot\sqrt{MSE\cdot\Big{(}1+\dfrac{1}{n}+\dfrac{(x_{0}-\overline{x})^{2}}{\sum\limits (x_{i}-\overline{x})^{2}}}$$
donde:
- $\hat{y}$ es la predicción.
- $t_{\dfrac{\alpha}{2},n-2}$ es el valor crítico de la distribución Student.
- $MSE$ es el error cuadrático medio.
- $x_{0}$ es el valor de $ACT(20)$.
- $\overline{x_{i}}$ es la media de los valores de $ACT$.

Vamos a encontrar cada uno de estos valores:
$$\begin{align*} \hat{y}&=0.568152+0.102197\cdot20\\ &\approx 2.612092 \end{align*}$$

La media es:
$$\begin{align*} \overline{x_{i}}&=\dfrac{\sum\limits x_{i}}{n}\\ &=\dfrac{207}{8}\\ &=25.875 \end{align*}$$

Ahora para facilitar el cálculo de los $\hat{y_{i}}$ lo haremos usando Excel donde la fórmula para encontrar los $\hat{y_{i}}$ es:
$$\hat{y_{i}}=0.568152+0.102197\cdot x_{i}$$
Los $\hat{y_{i}}$ nos quedan de la siguiente forma:
![[Pasted image 20240520081834.png]]

Ahora procedemos a encontrar el valor de $MSE$:
$$\begin{align*} MSE&=\dfrac{\sum\limits(y_{i}-\hat{y_{i}})^{2}}{n-2}\\ &=\dfrac{0.000000000025}{8-2}\\ &=\dfrac{0.000000000025}{6}\\ &=0.00000000000416669 \end{align*}$$

Finalmente, construimos el intervalo de confianza:
$$t_{0.025,6}=1.9432$$
$$\begin{align*} IC&=2.612092\pm1.9432\cdot\sqrt{0.00000000000416669\cdot\Big{(}1+\frac{1}{8}+\dfrac{(20-25.875)^{2}}{669.515625}}\\ &=2.612092\pm1.9432\cdot0.00000221412\\ &=2.612092\pm0.00000430248\\ &=2.612092-0.00000430248=2.61208\\ &=2.612092+0.00000430248=2.61209 \end{align*}$$
$$IC=(2.61208,2.61209)$$


**Solución (c):**

Estudiante $1$:
$ACT$: $21$
$GPA$ Observado: $2.8$
Calculamos el valor ajustado:
$$\hat{y}_1 = 0.5706 + 0.1021 \cdot 21 \approx 2.7147$$
Calculamos el residuo:
$$e_1 = 2.8 - 2.7147 \approx 0.0853$$

Estudiante $2$:
$ACT$: $24$
$GPA$ Observado: $3.4$
Calculamos el valor ajustado:
$$\hat{y}_2 = 0.5706 + 0.1021 \cdot 24 \approx 3.021$$
Calculamos el residuo:
$$e_2 = 3.4 - 3.021 \approx 0.379$$

Estudiante $3$:
$ACT$: $26$
$GPA$ Observado: $3.0$
Calculamos el valor ajustado:
$$\hat{y}_3 = 0.5706 + 0.1021 \cdot 26 \approx 3.2252$$
Calculamos el residuo:
$$e_3 = 3.0 - 3.2252 \approx -0.2252$$

Estudiante $4$:
$ACT$: $27$
$GPA$ Observado: $3.5$
Calculamos el valor ajustado:
$$\hat{y}_4 = 0.5706 + 0.1021 \cdot 27 \approx 3.3273$$
Calculamos el residuo:
$$e_4 = 3.5 - 3.3273 \approx 0.1727$$

Estudiante $5$:
$ACT$: $29$
$GPA$ Observado: $3.6$
Calculamos el valor ajustado:
$$\hat{y}_5 = 0.5706 + 0.1021 \cdot 29 \approx 3.5315$$
Calculamos el residuo:
$$e_5 = 3.6 - 3.5315 \approx 0.0685$$

Estudiante $6$:
$ACT$: $25$
$GPA$ Observado: $3.0$
Calculamos el valor ajustado:
$$\hat{y}_6 = 0.5706 + 0.1021 \cdot 25 \approx 3.1231$$
Calculamos el residuo:
$$e_6 = 3.0 - 3.1231 \approx -0.1231$$

Estudiante $7$:
$ACT$: $25$
$GPA$ Observado: $2.7$
Calculamos el valor ajustado:
$$\hat{y}_7 = 0.5706 + 0.1021 \cdot 25 \approx 3.1231$$
Calculamos el residuo:
$$e_7 = 2.7 - 3.1231 \approx -0.4231$$

Estudiante $8$:
$ACT$: $30$
$GPA$ Observado: $3.7$
Calculamos el valor ajustado:
$$\hat{y}_8 = 0.5706 + 0.1021 \cdot 30 \approx 3.6336$$
Calculamos el residuo:
$$e_8 = 3.7 - 3.6336 \approx 0.664$$

**Solución (d):**

El coeficiente de determinación ($R^2$) mide la proporción de la variación total en la variable dependiente que es explicada por el modelo de regresión.
$$R^2 = \frac{SSR}{SST}$$
Donde:
- ($SSR$) es la suma de los cuadrados de la regresión.
- ($SST$) es la suma total de los cuadrados.

Calculamos:
$$\bar{y} = \frac{25.7}{8} \approx 3.2125$$
$$SSR = \sum (\hat{y}_i - \bar{y})^2 \approx 0.43471$$
$$SST = \sum (y_i - \bar{y})^2 \approx 1.02875$$
$$R^2 = \frac{0.43471}{1.02875} \approx 0.42256$$
El coeficiente de determinación ($R^2 \approx 0.4225$) indica que aproximadamente el $42.25\%$ de la variabilidad en el $GPA$ puede ser explicada por el $ACT$. Esto sugiere que hay una relación moderada entre $ACT$ y $GPA$, y que el $ACT$ puede explicar un poco más del $42\%$ de la variabilidad en los $GPA$ de estos ocho estudiantes. El resto de la variabilidad (aproximadamente $57.75\%$) se debe a otros factores no incluidos en el modelo o a la variabilidad inherente en los datos.