
$$SS_{E}=Y'Y-2\beta'X'Y+\beta'X'X\beta$$
Al derivar respecto a $\beta$, se obtiene que $$\frac{\partial SS_{E}}{\partial\beta}=-2X'Y+2X'X\beta$$
Después, al igualar a $0$ la expresión anterior $$\begin{align*} X'X\hat{\beta}&=X'Y\\ (X'X)^{-1}X'X\hat{\beta}&=(X'X)^{-1}X'Y\\ I\hat{\beta}&=(X'X)^{-1}X'Y\\ \hat{\beta}&=(X'X)^{-1}X'Y \end{align*}$$
$$\hat{\beta} = \begin{bmatrix} \hat{\beta_{0}}\\ \hat{\beta_{1}}\\ \vdots\\ \hat{\beta_{n}} \end{bmatrix}\ \ \ \ \ \ \ \ \ \ \beta=\begin{bmatrix} \beta_{0}\\ \beta_{1}\\ \vdots\\ \beta_{n} \end{bmatrix}$$

### Propiedades de los estimadores

$$\begin{align*} \mathbb{E}(\hat{\beta}|X)&=\mathbb{E}\big{(}(X'X)^{-1}X'Y\big{)}\\ &=(X'X)^{-1}X'\mathbb{E}(Y)\\ &=(X'X)^{-1}X'X\beta\\ &=\beta \end{align*}$$
$$Y=X\beta+\epsilon$$
$$\begin{align*} \mathbb{E}(Y)&=\mathbb{E}(X\beta)+\mathbb{E}(\epsilon)\\ &=X\beta+0_{n\times1} \end{align*}$$
Por lo tanto, $\hat{\beta}$ es un estimador insesgado para $\beta$.

$$\begin{align*} \text{Var}(\hat{\beta}|X)&=\text{Var}\Big{(}(X'X)^{-1}X'Y\Big{)}\\ &=\Big{[}(X'X)^{-1}X'\Big{]}\Big{[}(X'X)^{-1}X'\Big{]}\text{Var}(Y)\\ &=\Big{[}(X'X)^{-1}X'\Big{]}\Big{[}(X'X)^{-1}X'\Big{]}\sigma^{2}\\ &=(X'X)^{-1}X'X(X'X)^{-1}\sigma^{2}\\ &=(X'X)^{-1}\sigma^{2}\\ &=\sigma^{2}(X'X)^{-1} \end{align*}$$
