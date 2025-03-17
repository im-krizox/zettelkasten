
$$\text{Cambios de variable }\begin{cases} SS_{\text{Total}}=SSE_{r}\\ SS_{\text{Errores}}=SSE_{c} \end{cases}$$
$$\begin{align*} SS_{\text{Total}}&=SS_{\text{Tratamientos}}+SS_{\text{Errores}}\\ \sum\limits_{i=1}^{t}\sum\limits_{j=1}^{r}(Y_{ij}-\overline{Y})^{2}&=\sum\limits_{i=1}^{t}\sum\limits_{j=1}^{r}(\overline{Y_{i}}-\overline{Y})^{2}+\sum\limits_{i=1}^{t}\sum\limits_{j=1}^{r}(Y_{ij}-\overline{Y_{i}})^{2} \end{align*}$$

#### Tabla ANOVA

| Factor de variabilidad | Grados de libertad | Suma de cuadrados          | Cuadrados medios                       | Estadístico de la prueba                                                                               |
| ---------------------- | ------------------ | -------------------------- | -------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| Tratamiento            | $t-1$              | $SS_{\text{Tratamientos}}$ | $\frac{SS_{\text{Tratamientos}}}{t-1}$ | $F_{0}=\frac{\frac{SS_\text{Tratamientos}}{t-1}}{\frac{SS_{\text{Errores}}}{tr-t}}\sim F_{t-1,\ tr-t}$ |
| Errores                | $tr-t$             | $SS_{\text{Errores}}$      | $\frac{SS_\text{Errores}}{tr-t}$       |                                                                                                        |
| Total:                 | $tr-1$             | $SS_\text{Total}$          |                                        |                                                                                                        |

Se rechaza $H_{0}$ si $F_{0}>q_{F_{t-1,n-1}}{(1-\alpha)}$ 
- $H_{0}:\mu_{1}=\ldots=\mu_{k}$
- $H_{1}:\mu_{i}\neq\mu_{j},\ i\neq j$

##### Ejemplo 2

Un ingeniero de desarrollo de productos tiene interés en investigar la resistencia a la tensión de una fibra que usará para hacer playeras. El ingeniero sabe por experiencia previa que la resistencia a la tensión se afecta por el peso porcentual de algodón utilizado en la mezcla de materiales de fibra.

Además, sospecha que al aumentar el contenido de algodón se incrementará la resistencia, al menos en un principio. El ingeniero decide probar ejemplares en cinco niveles del peso porcentual del algodón: 15%, 20%, 25%, 30% y 35%. También decide probar cinco ejemplares en cada nivel del contenido de algodón. Los resultados que obtuvo, se muestran en la siguiente tabla:

| 15% | 20% | 25% | 30% | 35% |
| --- | --- | --- | --- | --- |
| 7   | 12  | 14  | 19  | 7   |
| 7   | 17  | 18  | 25  | 10  |
| 15  | 12  | 18  | 22  | 11  |
| 11  | 18  | 19  | 19  | 15  |
| 9   | 18  | 19  | 23  | 11  |
Con estos datos, ¿podemos afirmar la resistencia de las playeras es similar para cada nivel de contenido de algodón?
- $H_{0}:\mu_{1}=\ldots=\mu_{k}$
- $H_{1}:\mu_{i}\neq\mu_{j},\ i\neq j$

- $\overline{Y_{1}}=9.8$
- $\overline{Y_{2}}=15.4$
- $\overline{Y_{3}}=17.6$
- $\overline{Y_{4}}=21.6$
- $\overline{Y_{5}}=10.8$
- $\overline{Y}=15.04$

$$\begin{align*} SS_{\text{Tratamientos}}&=\sum\limits_{i=1}^{t}\sum\limits_{j=1}^{r}(\overline{Y_{i}}-\overline{Y})^{2}\\ &=r\sum\limits_{i=1}^{t}(\overline{Y_{i}}-\overline{Y})^{2}\\ &=5\Big{[}(9.8-15.04)^{2}+(15.04-15.04)^{2}+(17.6-15.04)^{2}+(21.6-15.04)^{2}+(10.08-15.04)^{2}\Big{]}\\ &=475.76 \end{align*}$$

$$\sum\limits_{i=1}^{t}\sum\limits_{j=1}^{r_{i}}(\overline{Y_{i}}-\overline{Y})^{2}=r_{1}(\overline{Y_{1}}-\overline{Y})^{2}+\ldots+r_{t}(\overline{Y_{t}}-\overline{Y})^{2}$$

$$\begin{align*} SS_{\text{Total}}&=\sum\limits_{i=1}^{t}\sum\limits_{j=1}^{r}(Y_{ij}-\overline{Y})^{2}\\ &=636.96 \end{align*}$$

$$SS_{\text{Errores}}=161.20$$

Grados de libertad de los tratamientos:
- $t-1$
- $5-1=4$

Grados de libertad de los errores:
- $tr-t$
- $25-5=20$

$H_{0}:\mu_{1}=\ldots=\mu_{5}=\mu$ ✖
$H_{1}:\mu_{i}\neq\mu_{j},\ i\neq j$ ✔

