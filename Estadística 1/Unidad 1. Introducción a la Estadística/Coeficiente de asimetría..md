Metadata:
Fecha: 23-08-2023
Hora: 07:14
Título: Coeficiente de asimetría.

## Apunte.
---
### Coeficiente de asimetría.
---
$$sk(x)=\frac{1}{s^3}\Big[\frac{1}{n}\sum_{i=1}^{n}(x_i-\overline{x})^3\Big]$$ donde $s$ es la desviación estándar de $x$.
$$\begin{align*} sk(x)&=\frac{1}{s^3}[m_3]\\ &=\frac{m_3}{(m_2)^{\frac{3}{2}}} \end{align*}$$ donde $$s=\Big(\frac{1}{n}\sum_{i=1}^n(x_i-\overline{x})^2\Big)^{\frac{1}{2}}$$
![[Pasted image 20230823073450.png|500]]

#### Ejemplo 14.
---
Muestra que el coeficiente de asimetría es adimensional e invariante a cambios de escala y origen.
- $sk(ax+c)=sk(x)$.
**Demostración:**
Debido a que $m_3$ y $(m_2)^{\frac{3}{2}}$ tienen la misma unidad de medida, $sk(x)$ es adimensional.
Por otro lado, tenemos que $$sk(ax+c)=\frac{1}{\big[s(ax+c\big]^3}\Big[\frac{1}{n}\sum_{i=1}^n\big(ax_i+c-[a\overline{x}+c]\big)^3\Big]$$ $$\begin{align*} \text{Media}(ax+c)&=a\text{Media}(x)+c\\ s(ax+c)&=|a|s(x)\\ &=\frac{1}{\big[ |a|s(x) \big]^3}\Big[\frac{a^3}{n}\sum_{i=1}^n(x_i-\overline{x})^3\Big]\\ &=\frac{a^3}{|a|^3}\frac{1}{s^3}\Big[ \frac{1}{n}\sum_{i=1}^n(x_i-\overline{x})^3 \Big]\\ &=\frac{a^3}{|a|^3}sk(x) \end{align*}$$
Pero para las dos últimas expresiones tenemos dos casos $$\begin{cases} \text{si }a>0\text{,}&sk(ax+c)=sk(x)\\ \text{si }a<0\text{,}&sk(ax+c)=-sk(x) \end{cases}$$


###### Tareas.
---




