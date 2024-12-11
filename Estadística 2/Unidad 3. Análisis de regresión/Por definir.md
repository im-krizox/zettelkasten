
### Tabla ANOVA

| Factor de variabilidad | Grados de libertad | $SS$                              | $MS$                                          |
| ---------------------- | ------------------ | --------------------------------- | --------------------------------------------- |
| Regresión              | $1$                | $\hat{\beta_{1}}S_{xy}$           | $\hat{\beta_{1}}S_{xy}$                       |
| Residuos               | $n-2$              | $SS_{\tau}-\hat{\beta_{1}}S_{xy}$ | $\frac{SS_{\tau}-\hat{\beta_{1}}S_{xy}}{n-2}$ |
| Total                  | $n-1$              | $SS_{\tau}$                       |                                               |

### Estadístico de la prueba

$$F_{0}=\frac{MS_\text{Regresión}}{MS_\text{Residuos}}\sim F_{1,\ n-2}$$
$$SS_{\text{Regresión}}=\sum\limits\limits_{i=1}^{n}(\hat{Y_{i}}-\overline{Y})^{2}$$
$$SS_{\text{Total}}=\sum\limits_{i=1}^{n}(Y_{i}-\overline{Y})^{2}$$
- $H_{0}:\beta_{1}=0$
- $H_{1}:\beta_{1}\neq0$

### Región de rechazo

$$F_{0}>q_{F_{1,\ n-2}}^{(1-\alpha)}$$

