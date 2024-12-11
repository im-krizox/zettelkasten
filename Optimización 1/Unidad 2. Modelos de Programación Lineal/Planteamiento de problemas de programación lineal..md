Metadata:
Fecha: 18-08-2023
Hora: 09:47
Título: Planteamiento de problemas de programación lineal.

## Apunte.
---
### Problema 1.
---
Formule el siguiente problema de preparación de dieta. Una madre desea que sus niños obtengan ciertas cantidades de elementos nutritivos de sus cereales de desayuno. Los niños pueden escoger entre comer tronados o dorados o una mezcla de las dos. De su desayuno deben obtener, cuando menos 1 mg de tiamina, 5 mg de niacina y 400 calorías. Una onza de tronados contiene 0.10 mg de tiamina, 1 mg de niacina y 110 calorías; 1 onza de dorados contiene 0.25 mg de tiamina, 0.25 mg de niacina y 120 calorías. Una onza de tronados cuesta 3.8 centavos y una onza de dorados 4.2 centavos.

#### Planteamiento del problema.
---
$x_1=$ Cantidad de onzas de tronados a comprar.
$x_2=$ Cantidad de onzas de dorados a comprar.
**Objetivo:** Minimizar $Z=\$3.8x_1+\$4.2x_2$

|  | $x_1$ | $x_2$ | **Objetivo** $\geq$ |
| --- | --- | --- | --- |
| **Niacina** | 1 | 0.25 | 5 mg |
| **Tiamina** | 0.10 | 0.25 | 1 mg |
| **Calorías** | 110 | 120 | 400 cal |
| | $3.80 | $4.20 | |

$$\text{(PPL)}\begin{cases} \min Z&=\$3.80x_1+\$4.20x_2\\ \text{s. a.}&x_1+0.25x_2&\geq 5\\ &0.10x_1+0.25x_2&\geq 1\\ &110x_1+120x_2&\geq400\\ &x_1,x_2&=0 \end{cases}$$


### Problema 3.
---
Un fabricante de muebles desea determinar cuantas mesas, si

#### Planteamiento del problema.
---
$x_1=$ Número de mesas a producir
$x_2=$ Número de sillas a producir
$x_3=$ Número de escritorios a producir
$x_4=$ Número de libreros a producir
**Objetivo:** Maximizar $Z=\$12x_1+\$5x_2+\$15x_3+\$10x_4$

|  | $x_1$ | $x_2$ | $x_3$ | $x_4$ |  |
| --- | --- | --- | --- | --- | --- |
| **Madera tipo 1** | 5 | 1 | 9 | 12 | 1500 pies |
| **Madera tipo 2** | 2 | 3 | 4 | 1 | 1000 pies |
| **Horas hombre** | 3 | 2 | 5 | 10 | 800 horas |
| **Mesas** | 1 | 0 | 0 | 0 | $\geq$ 40 |
| **Sillas** | 0 | 1 | 0 | 0 | $\geq$ 130 | 
| **Escritorios** | 0 | 0 | 1 | 0 | $\geq$ 30 |
| **Libreros** | 0 | 0 | 0 | 1 | $\leq$ 10 |
|  | $12 | $5 | $15 | $10 |  |

$$\text{(PPL)}\begin{cases} \max Z=&\$12x_1+\$5x_2+\$15x_3+\$10x_4\\ \text{s. a.}& \end{cases}$$



###### Tareas.
---

