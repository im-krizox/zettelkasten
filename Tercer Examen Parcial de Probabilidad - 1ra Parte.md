
- Kristoffer Van Steemberghe Luján
- 319206463
- 21-05-2024

### Ejercicio 1.
Los partidos de voleibol en la temporada pasada, tuvieron una duración uniforme entre $60$ minutos y $135$ minutos, ambas inclusive.

#### a) Describa la variable aleatoria, la función de densidad y distribución acumulada.

**Variable aleatoria:** Sea $X$ la variable aleatoria que representa el tiempo que dure un partido de voleibol en minutos, donde $X$ se distribuye uniformemente en el intervalo de $[60,135]$.

**Función de densidad:** Dado que la distribución de los partidos está uniformemente distribuida entre $60$ y $135$ minutos, la función de densidad $f(x)$ es constante dentro de este intervalo y es igual a
$$f(x)=\begin{cases} \dfrac{1}{135-60}=\dfrac{1}{75}&\text{para }a\leq x\leq b\\ 0&\text{c. o. c.} \end{cases}$$
Así mismo la función de distribución acumulada es
$$F(x)=\begin{cases} 0&\text{para }x\leq a\\ \dfrac{x-60}{75}&\text{para }a\leq x <b\\ 1&\text{para }x\geq b \end{cases}$$

#### b) Calcule la media y la desviación típica.

**Media:**
$$\mu=\dfrac{a+b}{2}=\dfrac{60+135}{2}=\dfrac{195}{2}=97.5$$

**Desviación estándar:**
$$\sigma=\dfrac{b-a}{\sqrt{12}}=\dfrac{135-60}{\sqrt{12}}=\dfrac{75}{\sqrt{12}}=\dfrac{25\sqrt{3}}{\sqrt{12}}=21.6506$$

#### c) ¿Cuál es la probabilidad de que la duración de los partidos de un equipo en esta temporada, duré entre 75 y 105 minutos?

$$\begin{align*} P(75\leq X\leq105)&=F(105)-F(75)\\ &=\dfrac{105-60}{75}-\dfrac{75-60}{75}\\ &=\dfrac{45}{75}-\dfrac{15}{75}\\ &=\dfrac{2}{5} \end{align*}$$


### Ejercicio 2.
Un servicio de asistencia técnica en carretera ha comprobado que en las mañanas de los fines de semana el número de llamadas que recibe, por término medio, es de $3$ llamadas cada hora. Un operario comienza su jornada de sábado a las $8$ de la mañana. Suponiendo que las llamadas se realizan de forma independiente y con tasa constante:.

#### a) Defina la variable aleatoria.

**Variable aleatoria:** Sea $X$ la variable aleatoria que representa el número de llamadas que recibe cada hora un servicio de asistencia técnica los fines de semana por la mañana.

#### b) ¿Cuál es la probabilidad de que reciba la primera llamada antes de las 8:15?

Sabemos que $X$ se distribuye exponencialmente con $X\sim\text{Exp}(3)$.

Además, la media ($\mu$) es
$$\mu=\dfrac{1}{3}$$
Tomando en cuenta la falta de memoria en el modelo Exponencial, $X$ se puede interpretar como el tiempo en horas que transcurre desde el momento actual hasta que llega la primera llamada. Entonces, recapitulando, la probabilidad sería
$$\begin{align*} P(X<15\text{ minutos})=P(X<0.25\text{ horas})&=\int_{0}^{0.25}3e^{-3x}\ dx\\ &=3\int_{0}^{0.25}e^{-3x}\ dx\\ &=-\int_{-0.75}^{0}e^{u}\ du\\ &=\int_{-0.75}^{0}e^{u}\ du\\ &=e^{u}\Bigg{|}_{-0.75}^{0}\\ &=0.527633 \end{align*}$$

#### c) ¿Cuál es la probabilidad de que reciba $4$ llamadas en las dos primeras horas de su jornada de trabajo?

Propongamos una nueva variable aleatoria $Y$ que cuenta el número de llamadas recibidas en $2$ horas. Si en $1$ hora por término medio se reciben $3$ llamadas, ahora en un intervalo de tiempo del doble de tamaño se espera que también se duplique, es decir $6$. De esta forma, podemos decir que $Y$ se distribuye mediante una Poisson con parámetro $\mathbb{E}[Y]=6$.

La probabilidad que se solicita encontrar es $P(Y=4)$. Utilizando la función de probabilidad de Poisson obtenemos que
$$P(Y=4)=\dfrac{e^{-\lambda}\lambda^{y}}{y!}=\dfrac{e^{-6}6^{4}}{4!}=\dfrac{e^{-6}1296}{24}=\dfrac{\dfrac{1296}{e^{-6}}}{24}=\dfrac{54}{e^{6}}\approx0.133852$$

#### d) Si lleva 10 minutos sin recibir ninguna llamada, ¿cuál es la probabilidad de que reciba una nueva llamada en menos de 15 minutos?

La probabilidad buscada es $P(X<25\text{ minutos};X>10\text{ minutos})$. Aun que sabemos que la distribución exponencial no tiene memoria, entonces tenemos que calcular $P(X<15\text{ minutos})$.

A lo cual se tiene que realizar lo siguiente:
$$\begin{align*} P(X<15\text{ minutos})&=\dfrac{P(10\text{ minutos}<X<25\text{ minutos})}{P(X>10\text{ minutos})}\\ &=\dfrac{P(\dfrac{1}{6}<X<\dfrac{5}{12})}{P(X>\dfrac{1}{6})}\\ &=\dfrac{\int_{\frac{1}{6}}^{\frac{5}{12}}3e^{-3x}\ dx}{\int_{\frac{1}{6}}^{\infty}3e^{-3x}\ dx}\\ &=\dfrac{-e^{-3x}\Bigg{|}_{\frac{1}{6}}^{\frac{5}{12}}}{-e^{-3x}\Bigg{|}_{\frac{1}{6}}^{\infty}}\\ &=\dfrac{-e^{-\frac{1}{2}}-e^{-\frac{75}{60}}}{-e^{-\frac{1}{2}}}\\ &=\dfrac{-e^{-\frac{1}{2}}\Big{(}1-e^{-\frac{3}{4}}\Big{)}}{-e^{-\frac{1}{2}}}\\ &=1-e^{-0.75}\\ &=0.527633 \end{align*}$$


### Ejercicio 3.
Todas las semanas una panadería hace reportes de sus ventas, los registros de éstas indican que cada semana se venden de un mínimo de $300$ panes a un máximo de $700$ panes, y la mayoría de las semanas se venden $500$ panes.

#### a) Defina la variable aleatoria y a la distribución que la distribuye.

**Variable aleatoria:** Sea $X$ la variable aleatoria que representa el número de panes vendidos en una semana.

**Distribución que distribuye los datos:** Los datos están distribuidos triangularmente, ya que tenemos un mínimo ($a=300$), un máximo ($b=700$) y una moda ($c=500$).
$$X\sim T(300,700,500)$$

#### b) Encuentre la media y la varianza.

**Media:**
$$\mu=\dfrac{a+b+c}{3}=\dfrac{300+700+500}{3}=\dfrac{1500}{3}=500$$

**Varianza:**
$$\begin{align*} \sigma^{2}&=\dfrac{a^{2}+b^{2}+c^{2}-ab-ac-bc}{18}\\ &=\dfrac{300^{2}+700^{2}+500^{2}-(300\cdot700)-(300\cdot500)-(700\cdot500)}{18}\\ &=\dfrac{9000+490000+250000-210000-150000-350000}{18}\\ &=\dfrac{120000}{18}\\ &=\dfrac{20000}{3}\\ &\approx6666.\overline{6} \end{align*}$$

#### c) Calcule la probabilidad de que en una semana se tenga una venta entre $400$ y $600$ panes.

La probabilidad solicita es $P(400<X<600)$.

Para $P(X>400)$:
$$\begin{align*} \dfrac{(x-a)^{2}}{(b-a)(c-a)}&=\dfrac{(400-300)^{2}}{(700-300)(500-300)}\\ &=\dfrac{(100)^{2}}{(400)(200)}\\ &=\dfrac{10000}{80000}\\ &=\dfrac{1}{8}\\ &=0.125 \end{align*}$$


Para $P(X<600)$:
$$\begin{align*} 1-\dfrac{(b-x)^{2}}{(b-a)(b-c)}&=1-\dfrac{(700-600)^{2}}{(700-300)(700-500)}\\ &=1-\dfrac{(100)^{2}}{(400)(200)}\\ &=1-\dfrac{10000}{80000}\\ &=1-\dfrac{1}{8}\\ &=\dfrac{7}{8}\\ &=0.875 \end{align*}$$


### Ejercicio 4.
En una industria, la vida útil de una máquina (en horas) tiene la distribución Gamma. Si se declara como inservible al $4$ fallo y tiene un promedio de vida de $100$ horas.

#### a) Defina la variable aleatoria.

**Variable aleatoria:** Sea $X$ la variable aleatoria que representa el tiempo de vida útil en horas de una máquina.

#### b) Encuentra la probabilidad de que el dispositivo dure más de $300$ horas.

La probabilidad buscada es $P(X>300)=1-P(X\leq300)$.

Entonces
$$P(X>300)=1-P(X\leq300)=1-\dfrac{1}{\Gamma(4)}\int_{0}^{300}\dfrac{x^{4-1}e^{-\frac{x}{100}}}{100^{4}}\ dx$$
Debido al complejo calculo, utilizaremos una herramienta para resolverlo y obtenemos que
$$P(X>300)\approx0.6472$$

#### c) Encuentra la media y desviación estándar de la vida útil de la máquina.

**Media:**
En la descripción del ejercicio mencionan que en promedio ($\mu$) el tiempo de vida de la máquina es de $100$ horas, por lo cual no es necesario calcularla.

Lo que podemos hacer es encontrar $\beta$. Para ello sabemos que
$$\mu=\alpha\beta$$
En este caso
$$100=(4)(\beta)$$
Por lo que
$$\begin{align*} \beta&=\dfrac{100}{4}\\ &=25 \end{align*}$$

**Desviación estándar:**
$$\begin{align*} \sigma&=\beta\sqrt{\alpha}\\ &=25\sqrt{2}\\ &\approx35.355339 \end{align*}$$


### Ejercicio 5.
La proporción de pólizas de hogar que durante el año tienen algún siniestro sigue una distribución Beta ($X\rightarrow (\alpha,\beta)$) con $\beta=(0.3;0.5)$.

#### a) Defina la variable aleatoria y halle la media y varianza de la proporción de siniestros.

**Variable aleatoria:** Sea $X$ la variable aleatoria que representa la proporción de pólizas de hogar que durante el año han tenido un siniestro.

**Media:**
$$\mu=\dfrac{a}{a+b}=\dfrac{0.3}{0.3+0.5}=\dfrac{0.3}{0.8}=0.375$$

**Varianza:**
$$\sigma^{2}=\dfrac{ab}{(a+b)^{2}(a+b+1)}=\dfrac{(0.3\cdot0.5)}{(0.3+0.5)^{2}(0.3+0.5+1)}=\dfrac{0.15}{(0.64)(1.8)}=\dfrac{0.15}{1.152}=0.1302$$

#### b) ¿Cuál es la probabilidad de que la proporción de hogares con algún siniestro sea como máximo del $45\%$?

Para calcular las probabilidades usaremos el software de Excel, a lo cual la probabilidad solicitada es $P(X<0.45)=F(0.45)$

$$F(X)=\int_{0}^{x}\dfrac{\Gamma(a+b)}{\Gamma(a)\ \Gamma(b)}x^{a-1}(1-x)^{b-1}\ dx$$
$$\begin{align*} F(0.45)&=\int_{0}^{0.45}\dfrac{\Gamma(0.3+0.5)}{\Gamma(0.3)\ \Gamma(0.5)}0.45^{0.3-1}(1-0.45)^{0.5-1}\ dx \end{align*}$$

Usando Excel obtenemos que
$$P(X<0.45)=F(0.45)=0.613762$$
![[Pasted image 20240521172035.png|300]]

#### c) Con una probabilidad de $0.8$ ¿qué porcentaje como máximo de hogares tendrán algún siniestro?

Igualmente vamos a usar Excel para encontrar el porcentaje pero dejamos planteado lo siguiente:

$$\begin{align*} F(z)&=\int_{0}^{z}\dfrac{\Gamma(0.3+0.5)}{\Gamma(0.3)\ \Gamma(0.5)}z^{0.3-1}(1-z)^{0.5-1}\ dz=0.8 \end{align*}$$

Usando Excel obtenemos que
$$P(X<z)=(0.8)=0.811433$$
![[Pasted image 20240521172511.png|300]]

Lo que significa que un $81.143338\%$ de los hogares tendrán algún siniestro con una probabilidad del $80\%$. 