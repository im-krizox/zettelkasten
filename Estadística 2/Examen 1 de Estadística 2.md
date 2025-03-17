
- Kristoffer Van Steemberghe Luján
- 319206463
- 20/03/2024


## Ejercicio 1.
#Prueba-de-Kruskal-Wallis

En un estudio de calidad se realizaron pruebas a tres tipos de cronómetros. La siguiente tabla muestra miles de ciclos (encendido-apagado-reinicio) sobrevividos hasta que alguna parte del mecanismo falló (Natrella 1963).

Prueba si hay una diferencia significativa entre los tipos y, si la hay, determina cuáles tipos son significativamente diferentes. Utiliza técnica no paramétricas.

| Tipo 1          | Tipo 2          | Tipo 3          |
| --------------- | --------------- | --------------- |
| $1.7$ *(1)*     | $13.6$ *(6)*    | $13.4$ *(5)*    |
| $1.9$ *(2)*     | $19.8$ *(8)*    | $20.9$ *(9)*    |
| $6.1$ *(3)*     | $25.2$ *(12)*   | $25.1$ *(10.5)* |
| $12.5$ *(4)*    | $46.2$ *(16.5)* | $29.7$ *(13)*   |
| $16.5$ *(7)*    | $46.2$ *(16.5)* | $46.9$ *(18)*   |
| $25.1$ *(10.5)* | $61.1$ *(19)*   |                 |
| $30.5$ *(14)*   |                 |                 |
| $42.1$ *(15)*   |                 |                 |
| $82.5$ *(20)*   |                 |                 |
|                 |                 |                 |
| $n_1=9$         | $n_2=6$         | $n_3=5$         |
| $R_1=76.5$      | $R_2=78$        | $R_3=55.5$      |

![[Pasted image 20240320075335.png]]


Obtenemos los siguientes datos:
- $n=20$
- $k=3$
- $R=210$


$$\begin{align*} H&=\frac{12}{n(n+1)}\Bigg{(} \sum\limits_{i=1}^{k}\frac{R_{i}^{2}}{n_{i}} \Bigg{)}-3(n+1)\\ H&=\frac{12}{20(20+1)}\Bigg{(} \frac{(76.5)^{2}}{9}+\frac{(78)^{2}}{6}+\frac{(55.5^{2})}{5} \Bigg{)}-3(20+1) \end{align*}$$
$$H=\frac{753}{350}=2.1514285714$$

- Se rechaza $H_{0}$ con un nivel de significancia $\alpha$ si $H>qx_{k-1}^{2}(1-\alpha)$
$$\begin{align*} 2.1514285714&>x_{2}^{2}(0.95)\\ 2.1514285714&\ngtr5.991 \end{align*}$$
Como se observa anteriormente, $H$ es menor que el valor crítico, por lo que no rechazamos la hipótesis nula.
$\therefore$ No hay suficiente evidencia para afirmar que haya un nivel significativo que diferencie a los tres tipos de cronómetros, por lo que se acepta $H_{0}$.

- Se rechaza $H_{0}$ si $\text{p-valor}<\alpha$, $\text{p-valor}=\mathbb{P}(x_{k-1}^{2}>H)$
$$\begin{align*} \mathbb{P}(x_{2}^{2}>2.1514285714)&=0.3403 \end{align*}$$
$$\begin{align*} 0.3403&<0.05\\ 0.3403&\nless0.05 \end{align*}$$
$\therefore$ Se acepta $H_{0}$.



## Ejercicio 2.


Los datos en la siguiente tabla fueron tomados de un artículo en el New York Times (20 de abril 2001), "La raza de la víctima afecta la sentencia del asesino". Los datos provienen de un estudio de todos los casos de homicidio en Carolina del Norte durante el período 1993-1997 en los que era posible que una condena por asesinato resultará en la pena de muerte. Tales datos han desempeñado un papel importante en el debate sobre la pena de muerte en los Estados Unidos, el único país occidental rico que la impone.

Prueba que la raza de la víctima y la raza del acusado eran independientes de si el acusado recibió la pena de muerte por homicidios en Carolina del Norte durante los años 1993-1997 y da tus conclusiones al respecto.

| Raza del acusado | Raza de la víctima | Penas de muertes | No penas de muerte |
| ---------------- | ------------------ | ---------------- | ------------------ |
| No blanco        | Blanco             | $33$             | $251$              |
| Blanco           | Blanco             | $33$             | $508$              |
| No blanco        | No blanco          | $29$             | $587$              |
| Blanco           | No blanco          | $4$              | $76$               |
