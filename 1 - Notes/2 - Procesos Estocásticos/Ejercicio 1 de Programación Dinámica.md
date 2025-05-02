El Consejo Mundial de Salud se dedica a desarrollar la atención médica en los países de desarrollo. Actualmente dispone de cinco brigadas médicas para asignarlas a tres de ellos con el fin de mejorar el cuidado de la salud, la educación para la salud y los programas de capacitación. El consejo debe determinar cuántas brigadas asignar (si lo hace) a cada uno de los países para maximizar la medida como están constituidas, es decir, el número asignado a cada país debe ser un entero.
La medida de desempeño se evalúa en términos de los años de vida adicionales por persona. En el caso de un país específico, esta medida es igual al incremento en el promedio de vida esperado en años, multiplicado por su población.

![[Pasted image 20250501181125.png]]

### Solución.

#### 1. Definición de la Función de Estado.
Denotemos
- $f_i(j)$: el valor máximo de "años-persona" que podemos obtener al asignar $j$ brigadas a los primeros $i$ países.
- $r_k(x)$: el rendimiento (en miles de años-persona) del país $k\in\{A,B,C\}$ cuando se le asignan $x$ brigadas.

Queremos finalmente $f_3(5)$.

#### 2. Etapa 1: Solo país $A$ ($i=1$).
Aquí no hay elección: si asignamos $j$ brigadas a $A$, obtenemos
$$f_1(j)=r_A(j)$$

| $j$ brigadas | 0   | 1    | 2    | 3    | 4     | 5     |
| ------------ | --- | ---- | ---- | ---- | ----- | ----- |
| $r_A(j)$     | $0$ | $45$ | $70$ | $90$ | $105$ | $120$ |

#### 3. Etapa 2: Países $A$ y $B$ ($i=2$).
Ahora tenemos $j$ brigadas para repartir entre $A$ (con $x$) y $B$ (con $j-x$).
$$f_2(j)=\max_{0\leq x\leq j}\{f_{1}(x)+r_{B}(j-x)\}$$
Hacemos este cálculo para $j=0,1,\dots,5$:


| $j$ | Candidatos $\big(x,f_1(x)+r_B(j-x)\big)$                                                          | $f_2(j)$ | $x^*$   |
| --- | ------------------------------------------------------------------------------------------------- | -------- | ------- |
| 0   | $(0,0+0)$                                                                                         | $0$      | $0$     |
| 1   | $(0,0+20)=20;\ (1,45+0)=45$                                                                       | $45$     | $1$     |
| 2   | $(0,0+45)=45;\ (1,45+20)=65;\ (2,70+0)=70$                                                        | $70$     | $2$     |
| 3   | $(0,0+75)=75;\ (1,45+45)=90;\ (2,70+20)=90;\ (3,90+0)=90$                                         | $90$     | $1,2,3$ |
| 4   | $(0,0+110)=110;\ (1,45+75)=120;\ (2,70+45)=115;\ (3,90+20)=110;\ (4,105+0)=105$                   | $120$    | $2$     |
| 5   | $(0,0+150)=150;\ (1,45+110)=155;\ (2,70+75)=145;\ (3,90+45)=135;\ (4,105+20)=125;\ (5,120+0)=120$ | $155$    | $2$     |
- $f_{2}$ queda como $[0,45,70,90,120,155]$.
- $x^{*}(j)$ es cuántas brigadas irían a $A$ en la solución óptima de esa subinstancia.

#### 4. Etapa 3: Países $A$, $B$ y $C$ ($i=3$).
Finalmente repartimos las 5 brigadas en dos bloques:
- $y$ brigadas a los dos primeros países (optimizados con $f_{2}(y)$)
- $5-y$ brigadas a $C$
