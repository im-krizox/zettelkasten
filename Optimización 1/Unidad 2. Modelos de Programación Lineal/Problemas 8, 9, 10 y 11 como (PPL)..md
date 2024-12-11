Metadata:
Fecha: 23-08-2023
Hora: 09:16
Título: Problemas 8, 9, 10 y 11 como (PPL).

## Apunte.
---
**Objetivo del día de hoy:** Plantear los problemas 8, 9, 10 y 11.


### Problema 8.
---
Una casa de inversiones dispone de $600,000 para colocarlos en un conjunto de alternativas de inversión. La inversión tipo 1 está disponible en cada uno de los próximos seis año y se espera que produzca un rendimiento del 28% por cada peso invertido, al momento de su vencimiento al final de 3 años. La inversión tipo 2 también está disponible en cada uno de los próximos 6 años. Está inversión rendirá 16% por cada peso invertido y vence al final de dos años. La inversión tipo 3 está disponible solo al principio del segundo año y rinde 50% al final del cuarto año por cada peso invertido. La inversión tipo 4 está disponible en cualquier momento después del tercer año y produce un rendimiento del 40% al final de dos años. La oportunidad final de inversión es el tipo 5, está disponible solo una vez al principio del año.

Cuando las inversiones vencen, están disponibles para reinversión. A la casa le gustaría determinar la cartera de inversiones que maximice el rendimiento de la inversión total por un periodo de seis años, es decir, al final del sexto año.

#### Solución.
---
**Datos:**
$600,000 a 6 años.

| Tipo | Inicia | Rendimiento | Termina |
| --- | --- | --- | --- |
| Tipo 1 | Cualquier año | 28% | 3 años |
| Tipo 2 | Cualquier año | 16% | 2 años |
| Tipo 3 | Al principio del segundo año | 50% | A finales del 4° año |
| Tipo 4 | Cualquier momento después del 3° año | 40% | 2 años |
| Tipo 5 | A principios del año 1 | 45% | 4 años |
| Tipo 6 | Cada año | 0% | 1 año |

| Año | Inversión | Año 1 | Año 2 | Año 3 | Año 4 | Año 5 | Año 6 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Año 1 | Tipo 1 |  |  | $\longrightarrow$ 28% |  |  |  |
| Año 1 | Tipo 2 |  | $\longrightarrow$ 16% |  |  |  |  |
| Año 1 | Tipo 5 |  |  |  | $\longrightarrow$ 45% |  |  |
| Año 1 | Tipo 6 | $\longrightarrow$ 0% |  |  |  |  |  |
| Año 2 | Tipo 1 |  |  |  | $\longrightarrow$ 28% |  |  |
| Año 2 | Tipo 2 |  |  | $\longrightarrow$ 16% |  |  |  |
| Año 2 | Tipo 3 |  |  |  | $\longrightarrow$ 50% |  |  |
| Año 2 | Tipo 6 |  | $\longrightarrow$ 0% |  |  |  |  |
| Año 3 | Tipo 1 |  |  |  |  | $\longrightarrow$ 28% |  |
| Año 3 | Tipo 2 |  |  |  | $\longrightarrow$ 16% |  |  |
| Año 3 | Tipo 6 |  |  | $\longrightarrow$ 0% |  |  |  |
| Año 4 | Tipo 1 |  |  |  |  |  | $\longrightarrow$ 28% |
| Año 4 | Tipo 2 |  |  |  |  | $\longrightarrow$ 16% |  |
| Año 4 | Tipo 4 |  |  |  |  | $\longrightarrow$ 40% |  |
| Año 4 | Tipo 6 |  |  |  | $\longrightarrow$ 0% |  |  |
| Año 5 | Tipo 2 |  |  |  |  |  | $\longrightarrow$ 16% |
| Año 5 | Tipo 4 |  |  |  |  |  | $\longrightarrow$ 40% |
| Año 5 | Tipo 6 |  |  |  |  | $\longrightarrow$ 0% |  |
| Año 6 | Tipo 6 |  |  |  |  |  | $\longrightarrow$ 0% |

![[Pasted image 20230823122950.png]]

$x_{ij}=$ cantidad a invertir en el tipo $i$ en el año $j$, $i\in\overline{1,6}$ $j\in\overline{1,6}$.

$$\begin{align*} \text{Max }Z=\ \ \ \ \ \ \ &&\\ \text{s. a.}\ \ \ \ \ \ \ &x_{11}+x_{21}+x_{51}+x_{61}&=&\$600,000\\ &x_{12}+x_{22}+x_{32}+x_{62}&=&x_{61}\\ &x_{13}+x_{23}+x_{63}&=&x_{62}+1.16x_{21}\\ &x_{14}+x_{24}+x_{44}+x_{64}&=&x_{63}+1.16x_{22}+1.28x_{11}\\ &x_{25}+x_{45}+x_{65}&=&x_{64}+1.16x_{23}+1.5x_{32}+1.28x_{12}+1.45x_{51}\\ &x_{66}&=&1.28x_{13}+1.16x_{24}+1.40x_{44}+x_{65} \end{align*}$$ $$x_{ij}\geq0\ \ \ \ \ \ i\in\overline{1,6},\ \ \ j\in\overline{1,6}$$


### Problema 9.
---
Un granjero desea determinar cuáles la mejor selección de animales para su granja con el objeto de maximizar sus utilidades por la venta de los animales al final del verano. Puede elegir entre comprar borregos, reses o cabras. Cada borrego requiere un acre de pastura y $15 de alimentación y tratamiento. Un borrego cuesta $25 y puede venderse en $60. Para las reses esos valores son de 4 acres $30, $40 y $100; y para las cabras los valores son $\frac{1}{2}$ acre, $5, $10 y $20. La granja tiene 300 acres y el granjero dispone de $2500 para invertirlos en la compra y mantenimiento del rebaño. Por último, el granjero no desea que más del 40% de sus animales sean cabras, o que los borregos sean menos del 30%. Plantee este problema en forma de (PPL) para maximizar las utilidades al final del periodo.

#### Solución.
---

| Animales | Acres | Alimentos y Tratamiento | Costo | Venta |
| --- | --- | --- | --- | --- |
| Borregos | 1 | $15 | $25 | $60 |
| Reses | 4 | $30 | $40 | $100 |
| Cabras | $\frac{1}{2}$ | $5 | $10 | $20 |

|  | $x_1^{\text{Borregos}}$ | $x_2^{\text{Reses}}$ | $x_3^{\text{Cabras}}$ |
| --- | --- | --- | --- |
| Acres | 1 | 4 | $\frac{1}{2}$ |
| Alimento, tratamiento y costo | $40 | $70 | $15 |
| Precio de venta | $60 | $100 | $20 |
| **Utilidad** | $20 | $30 | $5 |

$$\text{(PPL)}\begin{cases} \text{Max }Z=&20x_1+30x_2+5x_3\\ \text{s. a.}&x_1+4x_2+\frac{1}{2}x_3&\leq300\text{ acres}\\ &\$40x_1+\$70x_2+\$15x_3&\leq\$2500\text{ inversión}\\ &x_1&\geq0.30(x_1+x_2+x_3)\\ &x_3&\leq0.40(x_1+x_2+x_3) \end{cases}$$


### Problema 10.
---
El gerente de mercadotecnia de una compañia que vende productos alimenticios dietéticos está considerando la promoción de un nuevo producto. El presupuesto de publicidad de la compañia incluye $60,000 para este fin. La compañia puede hacer publicidad al nuevo producto a través de comerciales en T. V. y/o anuncios en revistas. Cada comercial de T. V. cuesta $8 pero se ha estimado que esos comerciales lo ven 50,000 personas. Cada anuncio de revista cuesta $4,500 y se estima que 25,000 personas ven esos anuncios. Debido a que la compañia controlara de la empresa que vende alimentos dietéticos también tiene inversiones en diversas imprentas, los administradores de primer nivel han dado instrucciones al gerente de que coloque cuando menos tres anuncios en revistas. El gerente ha decidido que la compañia debería tener cuando menos tantos comerciales como anuncios de revistas. Para auxiliarse en su proceso de toma de decisiones el gerente ha planteado el problema como sigue.

#### Solución.
---
$x_1=$ Cantidad de comerciales en T. V.
$x_2=$ Cantidad de anuncios en revistas.
**Función objetivo:** $\text{Max }Z=50,000x_1+25,000x_2$.

$$\text{(PPL)}=\begin{cases} \text{Max }Z&50,000x_1+25,000x_2\\ \text{s. a.}&\$8x_1+\$4,500x_2&\leq\$60,000\\ &x_2&\geq3\\ &x_1&\geq x_2\\ &x_1,x_2&\geq0  \end{cases}$$


###### Tareas.
---
