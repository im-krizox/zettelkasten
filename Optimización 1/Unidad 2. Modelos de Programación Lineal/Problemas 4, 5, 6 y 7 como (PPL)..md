Metadata:
Fecha: 21-08-2023
Hora: 09:14
Título: Problemas 4, 5, 6 y 7 como (PPL).

## Apunte.
---
### Problema 4.
---
Cuatro productos son procesados sucesivamente sobre 2 máquinas. El tiempo de manufactura en horas por unidad de cada producto es dado en la tabla siguiente:

| Máquinas | Producto 1 | Producto 2 | Producto 3 | Producto 4 |
| --- | --- | --- | --- | --- |
| 1 | 2 | 3 | 4 | 2 |
| 2 | 3 | 2 | 1 | 2 |
|  | Tiempo por unidad (horas) |

El costo total de producir una unidad de cada uno de los productos está basado directamente sobre el tiempo de la máquina. Supongamos que el costo por hora de la máquina 1 y 2 son $10.00 y $15.00 respectivamente. El total de horas presupuestadas para todos los productos sobre la máquina 1 y 2 son 500 y 380. Si el precio de venta por unidad por los productos 1, 2, 3 y 4 son $65.00, $70.00, $55.00 y $45.00. Formule el problema como un modelo de Programación Lineal para maximizar su utilidad total.

##### Solución.
---
$x_1=$ Número de productos a producir del producto 1.
$x_2=$ Número de productos a producir del producto 2.
$x_3=$ Número de productos a producir del producto 3.
$x_4=$ Número de productos a producir del producto 4.
**Objetivo:** Maximizar $Z=\$65x_1+\$70x_2+\$55x_3+\$45x_4$.

|  | $x_1$ | $x_2$ | $x_3$ | $x_4$ | Costo total por máquina |
| --- | --- | --- | --- | --- | --- |
| Máquina 1 | 2 $\times$ 10 $=$ $20.00 | 3 $\times$ 10 $=$ $30.00 | 4 $\times$ 10 $=$ $40.00 | 2 $\times$ 10 $=$ $20.00 | $110.00 |
| Máquina 2 | 3 $\times$ 15 $=$ $45.00 | 2 $\times$ 15 $=$ $30.00 | 1 $\times$ 15 $=$ $15.00 | 2 $\times$ 15 $=$ $30.00 | $120.00 |
| Costo total por producto | $65.00 | $60.00 | $55.00 | $50.00 |  |

$$\begin{align*} \text{Max }Z&=\$65x_1+\$70x_2+\$55x_3+\$45x_4\\ &=-\$65x_1-\$60x_2-\$55x_3-\$50x_4 \end{align*}$$
$$(\text{PPL})\begin{cases} \text{Max }Z&=\$0x_1+\$10x_2+\$0x_3-\$5x_4&=\$10x_2-\$5x_4\\ \text{s. a. }&2x_1+3x_2+4x_3+2x_4\leq500&\text{horas de la máquina 1}\\ &3x_1+2x_2+x_3+2x_4\leq380&\text{horas de la máquina 2}\\ &x_1,x_2,x_3,x_4\geq0 \end{cases}$$

### Problema 5.
---
Una compañia produce dos tipos de materiales para la construcción de casas. Cada material del primer tipo requiere tres veces más del tiempo para elaborarlo que el material del segundo tipo. La compañia puede producir un total de 1500 materiales en un día. El mercado limita las ventas diarias de 450 materiales del primer tipo y 750 del segundo tipo. Suponiendo que la utilidad por material es de $24 por tipo 1 y $15 por tipo 2. Plantear el problema como un problema de Programación Lineal en términos de obtener la máxima ganancia.

##### Solución.
---
**Objetivo:** Maximizar $Z=\$24x_1+\$15x_2$.

$$\text{(PPL)}\begin{cases} \text{Max }Z=&\$24x_1+\$15x_2\\ \text{s. a.}&x_1+x_2\leq1500&\text{materiales por día producidos}\\ &x_1\leq 450&\text{materiales por día vendidos}\\ &x_2\leq 750&\text{materiales por día vendidos}\\ &x_1,x_2\geq0 \end{cases}$$
otro planteamiento puede ser $$\text{(PPL)}\begin{cases} \text{Max }Z=&24x_1+15x_2\\ \text{s. a.}&450x_1+750x_2\leq1500\\ &x_1=3x_2\\ &x_1,x_2\geq0  \end{cases}$$


### Problema 6.
---
Escriba la formulación completa con Programación Lineal del siguiente problema de transporte e intente determinar la solución óptima por el método de tanteos.
Un fabricante tiene centros de distribución localizados en Atlanta, Chicago y la ciudad de New York. En estos centros tiene disponibilidad de 40, 20 y 40 unidades de su producto, respectivamente.
Sus detallistas requieren los siguientes números de unidades: Cleveland 25; Louisville 10; Memphis 20; Pittsburg 30; y Richmond 15. El costo de transporte por unidad, en dólares, entre cada centro y las localidades de los detallistas está dado en la siguiente tabla

|  | Cleveland | Louisvill | Memphis | Pittsburg | Richmond | 
| --- | --- | --- | --- | --- | --- |
| Atlanta | 55 | 30 | 40 | 50 | 40 |
| Chicago | 35 | 30 | 100 | 45 | 60 |
| New York | 40 | 60 | 95 | 35 | 30 |

##### Solución.
---
$x_{ij}=$ Cantidad de artículos a enviar del origen $i$ al destino $j$, $i\in\overline{1,3}$ y $j\in\overline{1,5}$.
**Objetivo:** Minimizar $Z=55x_{11}+30x_{12}+40x_{13}+50x_{14}+40x_{15}+35x_{21}+30x_{22}+100x_{23}+45x_{24}+60x_{25}+\ldots+30x_{35}$

$$\text{(PPL)}\begin{cases} \text{Min }Z=&55x_{11}+30x_{12}+40x_{13}+50x_{14}+40x_{15}+\ldots+30x_{35}\\ \text{s. a.}&x_{11}+x_{12}+x_{13}+x_{14}+x_{15}&\leq 40\\ &x_{21}+x_{22}+x_{23}+x_{24}+x_{25}&\leq 20\\ &x_{31}+x_{32}+x_{33}+x_{34}+x_{35}&\leq 40\\ &x_{11}+x_{21}+x_{31}&\geq25\\ &x_{12}+x_{22}+x_{32}&\geq 10\\ &x_{13}+x_{23}+x_{33}&\geq20\\ &x_{14}+x_{24}+x_{34}&\geq30\\ &x_{15}+x_{25}+x_{35}&\geq 15\\ &x_{ik}\geq0&i\in\overline{1,3}\ \ j\in\overline{1,5} \end{cases}$$

**Nota:** En Optimización 2 este problema se resolverá con igualdades utilizando el algoritmo de transporte y se añade la restricción de que la $\sum a_i=\sum b_j$.


### Problema 7.
---
La fábrica nacional de cerveza tiene plantas ubicadas en la CDMX, Guadalajara y Monterrey. La fábrica nacional de las latas, una subsidiaria de la fábrica nacional de cervezas tiene plantas en Puebla y Torreón. La demanda mensual de latas de cerveza se pronostica en:

| Planta de cerveza | Demanda mensual en latas |
| --- | --- |
| CDMX | 2,000,000 |
| Guadalajara | 500,000 |
| Monterrey | 400,000 |

Las latas de cerveza se retornan a la Fundidora Nacional de Aluminio, en donde se vierten en aluminio y de ahí se manden a la fábrica de latas. La producción máxima mensual de latas es

| Planta de latas | Capacidad mensual |
| --- | --- |
| Puebla | 1,000,000 |
| Torreón | 1,500,000 |

Los fletes están en función de la distancia entre las fábricas. Estos son

|  | Puebla | Torreón |
| --- | --- | --- |
| CDMX | 5 | 20 |
| Guadalajara | 20 | 15 |
| Monterrey | 25 | 2 |

Establecer el problema de Programación Lineal si se desean minimizar los costos de fletes.

##### Solución.
---
$$\text{(PPL)}\begin{cases} \text{Min }Z=&5x_{\text{P-DF}}+20x_{\text{P-G}}+25x_{\text{P-M}}+20x_{\text{T-DF}}+15x_{\text{T-G}}+2x_{\text{T-M}} \end{cases}$$



###### Tareas.
---

