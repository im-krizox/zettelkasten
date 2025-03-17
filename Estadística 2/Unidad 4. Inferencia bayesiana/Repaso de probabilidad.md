
## Probabilidad condicional

$$P(A|B)=\dfrac{P(A\cap B)}{P(B)}$$

## Probabilidad total

![[Imagen de WhatsApp 2024-05-08 a las 07.30.34_4cae3407.jpg|500]]

$$\begin{align*} P(A)&=P(A\cap B)+P(A\cap B^{c})\\ &=P(A|B)P(B)+P(A|B^{c})P(B^{c}) \end{align*}$$

## Regla de Bayes

Si $\beta_{n}$ es una partición del espacio muestral y para todo $n$ tenemos que $\beta_{n}\in F$ y $P(\beta_{n})>0$
$$P(\beta_{k}|A)=\dfrac{P(A|\beta_{k})P(\beta_{k})}{\sum\limits_{n}P(A|\beta_{n})P(\beta_{n})}$$

- $P(A|B)\neq P(B|A)$
- $P(E|F)=p\ \neq\ P(F|E)=p$

Supongamos que se tiene una muestra observada $(X_{1},\ldots,X_{n})$ proveniente de una familia paramétrica $f(X|\theta)$ con parámetro desconocido $\theta$. La distribución a posteriori se define como
$$p(\theta|X)=\dfrac{p(X|\theta)p(\theta)}{\int_{\circ{H}}p(X|\theta)p(\theta)\ d\theta}$$
donde $p(X|\theta)$ es la función de máxima verosimilitud y $p(\theta)$ es la función de distribución a priori.


## Estimación puntual

$$\hat{\theta}=\mathbb{E}(\theta|X)=\int_{\circ{H}}\theta p(\theta|X)\ d\theta$$
Cualquier medida de tendencia central se puede emplear como estimación puntual.


## Intervalos de probabilidad

$$P(\theta\in A)=\int_{A}P(\theta|X)\ d\theta=1-\alpha$$

![[Imagen de WhatsApp 2024-05-08 a las 07.51.37_097f48fc.jpg|500]]

![[Imagen de WhatsApp 2024-05-08 a las 07.52.17_fe8d97b8.jpg|500]]

$$\begin{align*} A&=[a_{1},a_{2}]\\ &=\Big[q_{p(\theta|X)}^{(\frac{\alpha}{2})},q_{p(\theta|X)}^{(1-\frac{\alpha}{2})}\Big] \end{align*}$$


## Contraste de hipótesis

$$H_{j}:\theta\in\circ{H}_{j}$$
$$P(H_{j})=\int_{\circ{H}_{j}}p(\theta|X)\ d\theta$$


## Familia exponencial

Una familia de funciones de densidad o masa de probabilidades se denomina familia exponencial si se puede expresar de la siguiente forma:
$$f(X|\theta)=h(X)c(\theta)\exp\Big{(} \sum\limits_{i=1}^{k}W_{i}(\theta)t_{i}(X) \Big{)}$$


##### Ejemplo 1

Muestra que la distribución Poisson es familia exponencial.

$$\begin{align*} f(X|\theta)&=\dfrac{\theta^{x}e^{-\theta}}{x!}\\ &=\dfrac{1}{x!}e^{-\theta}\theta^{x}\\ &=\dfrac{1}{x!}e^{-\theta}e^{\ln\theta^{x}}\\ &=\dfrac{1}{x!}e^{-\theta}e^{\ln\theta} \end{align*}$$

- $h(X)=\dfrac{1}{x!}$
- $c(\theta)=e^{-\theta}$
- $W_{i}(\theta)=\ln\theta$
- $t_{i}(X)=x$


##### Ejemplo 2

Muestra que la distribución binomial $(n,\theta)$ con $n$ desconocido y $\theta$ desconocido es familia exponencial.

$$\begin{align*} f(X|n,\theta)&=\begin{pmatrix} n\\ x \end{pmatrix}\theta^{x}(1-\theta)^{n-x}\\ &=\begin{pmatrix} n\\ x \end{pmatrix}(1-\theta)^{n}\Big{(} \dfrac{\theta}{1-\theta} \Big{)}^{x}\\ &=\begin{pmatrix} n\\ x \end{pmatrix}(1-\theta)^{n}e^{x\ln\Big{(}\dfrac{\theta}{1-\theta}\Big{)}} \end{align*}$$

- $h(X)=\begin{pmatrix} n\\ x \end{pmatrix}$
- $c(\theta)=(1-\theta)^{n}$
- $W_{i}(\theta)=\ln\Big{(}\dfrac{\theta}{1-\theta}\Big{)}$
- $t_{i}(X)=x$


## Familias conjugadas

Sea $P=\{p(X|\theta):\theta\in\circ{H}\}$ una familia paramétrica. Una clase de distribuciones de probabilidad $\mathcal{F}$ es una familia conjugada para $P$ si para todo $p(X|\theta)\in P$ y $P(\theta)\in\mathcal{F}$ se cumple que $p(\theta|X)\in\mathcal{F}$.


## Distribuciones a priori conjugadas

Si $f(X|\theta)$ es familia exponencial podemos definir a la función a priori como
$$p(\theta)\ \ \ \alpha\ \ \ c(\theta)^{\alpha}\ \ \ \exp\Big{(}W_{i}(\theta)\beta\Big{)}$$
Además, la función de distribución a posteriori es
$$p(\theta|X)\ \ \ \alpha\ \ \ c(\theta)^{\alpha+n}\ \ \ \exp\Big{(}\sum\limits_{i=1}^{k}W_{i}(\theta)\big{[}\beta+\sum\limits_{j=1}^{n}t_{i}(X_{j})\big{]}\Big{)}$$


##### Ejemplo 3

