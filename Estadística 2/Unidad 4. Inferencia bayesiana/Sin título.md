
##### Ejemplo 4

Encuentra la función de distribución a posteriori para el modelo Poisson.


###### Función de distribución a priori

$$\begin{align*} f(\lambda)&\alpha\big{(}(\lambda)^{\alpha}\exp\big{[}W_{i}(\lambda)\beta\big{]}\\ &=(e^{-\lambda})^{\alpha}\exp\big{[}\ln(\lambda)\beta\big{]}\\ &=e^{-\lambda\alpha}\lambda ^{\beta} \end{align*}$$

>[!faq] ¿Quién es la familia conjugada del modelo *Poisson*?
>La distribución *Gamma*.

Si $\lambda\sim\text{Gamma}(\alpha,\beta)$
$$f\big{(}\lambda|\alpha,\beta\big{)}=\dfrac{\beta^{\alpha}}{\gamma(\alpha)}\lambda^{\alpha-1}e^{-\beta\lambda}$$ donde
- $\lambda$ es la variable aleatoria.
- $\alpha,\beta\in\mathbb{R}$.

Así que
$$f(\lambda)\sim\text{Gamma}(\beta+1,\alpha)$$


###### Función de distribución a posteriori

Por otro lado,
$$f\big{(}\lambda|x)\alpha c(\lambda)^{\alpha+n}\exp\Big{[}W_{i}(\lambda)\big{(}\beta+\sum\limits_{j=1}^{n}t_{i}(x_{ij})\big{)}\Big{]}$$
Finalmente, obtenemos que
$$\begin{align*} f\big{(}\lambda|x\big{)}\sim&\text{ Gamma }(\beta+\sum\limits_{i=1}^{n}x_{i}+1,\alpha+n)\\ &\text{Gamma }(\alpha+\sum\limits_{i=1}^{n}x_{i},\beta+n) \end{align*}$$
$$\hat{\lambda}=\mathbb{E}\big{(}\lambda|x\big{)}=\dfrac{\alpha+\sum\limits x_{i}}{\beta+n}$$


##### Ejemplo 5

Encuentra la función de distribución a posteriori para el modelo Exponencial
$$f\big{(}X|\lambda\big{)}=\lambda e^{-\lambda X}\ I_{(0,\infty)}^{(X)}$$
a) Mostrar que es familia exponencial.
b) Identificar la familia conjugada del modelo exponencial.
c) Encontrar la función de distribución a priori.
d) Encontrar la función de distribución a posteriori.

**a)** Si $f\big{(}X|\theta\big{)}$ es familia exponencial entonces
$$f\big{(}X|\theta\big{)}=c(\theta)h(X)\exp\big{[}\sum\limits_{i=1}^{n}W_{i}(\theta)+t_{i}(X)\big{]}$$
Luego, si $X\sim\text{Exp}(\lambda)$
$$\begin{align*} f\big{(}X|\lambda\big{)}&=\lambda e^{-\lambda X}\ I_{(0,\infty)}^{(X)}\\ &=\lambda\ I_{(0,\infty)}^{(X)}\exp[-\lambda X] \end{align*}$$
- $c(\lambda)=\lambda$
- $h(X)=I_{(0,\infty)}^{(X)}$
- $W_{i}(\lambda)=-\lambda$
- $t_{i}(X)=X$

**b)** La distribución *Gamma*.

**c)** Función de distribución a priori
$$\begin{align*} f(\lambda)&\alpha\ c(\lambda)^{\alpha}\exp\big{[}W_{i}(\lambda)\beta\big{]}\\ &=\lambda^{\alpha}\exp[-\lambda\beta]\\ &=\lambda^{\alpha+1-1}\exp[-\beta\lambda] \end{align*}$$
$$f(\lambda)\sim\text{Gamma }(\alpha+1,\beta)$$

**d)** Función de distribución a posteriori
$$f\big{(}\lambda|X\big{)}\sim\text{Gamma }(\alpha+n+1,\beta+\sum\limits_{i=1}^{n}X_{i}),\ \ \ \text{Gamma }(\alpha,\beta)$$
Si $\alpha=\alpha+n$ y $\beta=\beta+\sum\limits_{j=1}^{n}t_{i}(X_{j})$
$$\text{Gamma }(\alpha+n,\beta+\sum\limits_{i=1}^{n}X_{i})$$
Si $\lambda\sim\text{Gamma }(\alpha,\beta)$, entonces
$$f\big{(}\lambda|\alpha,\beta\big{)}=\dfrac{\beta^{\alpha}}{\gamma(\alpha)}\lambda^{\alpha-1}e^{-\beta\lambda}$$


##### Ejemplo 6

Encuentra la función de distribución a posteriori para el modelo normal donde $\mu$ es desconocida y $\sigma^{2}$ es conocida.

Si $f\big{(}X|\theta\big{)}$ es familia exponencial, entonces
$$f\big{(}X|\theta\big{)}=c(\theta)\ h(x)\ \exp\big{[}\sum\limits_{i=1}^{n}W_{i}(\theta)t_{i}(X)\big{]}$$
Luego, si $X\sim\mathcal{N}(\mu,\sigma^{2})$
$$\begin{align*} f\big{(}X|\mu,\sigma^{2}\big{)}&=\dfrac{1}{\sqrt{2\pi\sigma^{2}}}e \end{align*}$$