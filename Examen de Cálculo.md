## 1 Pregunta
Para determinar la ecuación del plano tangente a una superficie en un punto dado, necesitamos calcular el vector normal al plano tangente en ese punto. El vector normal es perpendicular a los vectores tangentes a las curvas que pasan por ese punto en la superficie.

Primero, calculamos las derivadas parciales de la función en el punto dado:

$f(x, y, z) = x^3 + 3xy + z^2 - 2 = 0$

$\frac{\partial f}{\partial x} = 3x^2 + 3y$
$\frac{\partial f}{\partial y} = 3x$
$\frac{\partial f}{\partial z} = 2z$

Evaluamos estas derivadas parciales en el punto $(1, 1/3, 0)$:

$\frac{\partial f}{\partial x}(1, 1/3, 0) = 3(1)^2 + 3(1/3) = 3 + 1 = 4$
$\frac{\partial f}{\partial y}(1, 1/3, 0) = 3(1) = 3$
$\frac{\partial f}{\partial z}(1, 1/3, 0) = 2(0) = 0$

El vector normal al plano tangente es el gradiente de $f$ evaluado en ese punto:

$\nabla f(1, 1/3, 0) = (4, 3, 0)$

La ecuación del plano tangente tiene la forma:

$(x - x_0, y - y_0, z - z_0) \cdot \vec{n} = 0$

Donde $(x_0, y_0, z_0)$ es el punto de tangencia y $\vec{n}$ es el vector normal.

Sustituyendo, obtenemos:

$(x - 1, y - 1/3, z - 0) \cdot (4, 3, 0) = 0$
$4(x - 1) + 3(y - 1/3) + 0(z - 0) = 0$
$4x - 4 + 3y - 1 = 0$
$4x + 3y - 5 = 0$

Por lo tanto, la ecuación del plano tangente a la superficie $x^3 + 3xy + z^2 = 2$ con $z > 0$ en el punto $(1, 1/3, 0)$ es:

$4x + 3y - 5 = 0$


## 2 Pregunta
Para calcular el área de la superficie dada por $\Phi(\theta, \phi) = ((8+\cos (\phi)) \cos (\theta), (8+\cos (\phi)) \sin(\theta), \sin(\phi))$ con $\theta, \phi \in [0, 2\pi] \times [0, 2\pi]$, podemos utilizar la fórmula para el área de una superficie parametrizada:

$$ A = \iint_D \left\|\frac{\partial \Phi}{\partial \theta} \times \frac{\partial \Phi}{\partial \phi}\right\| \, d\theta \, d\phi $$

Primero, hallamos las derivadas parciales de $\Phi$ con respecto a $\theta$ y $\phi$:

$$

\frac{\partial \Phi}{\partial \theta} = \left( - (8 + \cos(\phi)) \sin(\theta), (8 + \cos(\phi)) \cos(\theta), 0 \right)

$$

$$

\frac{\partial \Phi}{\partial \phi} = \left( -\sin(\phi) \cos(\theta), -\sin(\phi) \sin(\theta), \cos(\phi) \right)

$$

Luego, calculamos el producto cruzado de $\frac{\partial \Phi}{\partial \theta}$ y $\frac{\partial \Phi}{\partial \phi}$:

$$

\frac{\partial \Phi}{\partial \theta} \times \frac{\partial \Phi}{\partial \phi} = \begin{vmatrix}

\mathbf{i} & \mathbf{j} & \mathbf{k} \\

-(8 + \cos(\phi)) \sin(\theta) & (8 + \cos(\phi)) \cos(\theta) & 0 \\

-\sin(\phi) \cos(\theta) & -\sin(\phi) \sin(\theta) & \cos(\phi)

\end{vmatrix}

$$

Esto da como resultado:

$$

\frac{\partial \Phi}{\partial \theta} \times \frac{\partial \Phi}{\partial \phi} = \left( (8+\cos(\phi)) \cos(\theta) \cos(\phi), (8+\cos(\phi)) \sin(\theta) \cos(\phi), \sin(\phi) (8 + \cos(\phi)) \right)

$$

La norma de este vector es:

$$

\sqrt{((8+\cos(\phi)) \cos(\theta) \cos(\phi))^2 + ((8+\cos(\phi)) \sin(\theta) \cos(\phi))^2 + (\sin(\phi) (8 + \cos(\phi)))^2}

$$

Simplificamos la expresión:

$$

= \sqrt{(8+\cos(\phi))^2 \cos^2(\phi) (\cos^2(\theta) + \sin^2(\theta)) + (8+\cos(\phi))^2 \sin^2(\phi)}

$$

Sabemos que $\cos^2(\theta) + \sin^2(\theta) = 1$, por lo tanto:

$$

= \sqrt{(8+\cos(\phi))^2 \cos^2(\phi) + (8+\cos(\phi))^2 \sin^2(\phi)}

$$
$$

= \sqrt{(8+\cos(\phi))^2 (\cos^2(\phi) + \sin^2(\phi))}

$$
$$

= \sqrt{(8 + \cos(\phi))^2}

$$
$$

= 8 + \cos(\phi)

$$

Así, el área de la superficie es:

$$

A = \iint_D (8 + \cos(\phi)) \, d\theta \, d\phi

$$

Dado que $\theta$ y $\phi$ varían de $0$ a $2\pi$, el área es:

$$

A = \int_0^{2\pi} \int_0^{2\pi} (8 + \cos(\phi)) \, d\theta \, d\phi

$$

Evaluamos primero la integral respecto a $\theta$:

$$

A = \int_0^{2\pi} \left( \int_0^{2\pi} (8 + \cos(\phi)) \, d\theta \right) d\phi

$$

$$

= \int_0^{2\pi} \left( (8 + \cos(\phi)) \int_0^{2\pi} d\theta \right) d\phi

$$

$$

= \int_0^{2\pi} (8 + \cos(\phi)) \cdot 2\pi \, d\phi

$$

$$

= 2\pi \int_0^{2\pi} (8 + \cos(\phi)) \, d\phi

$$

Evaluamos la integral respecto a $\phi$:

$$

= 2\pi \left[ 8\phi + \sin(\phi) \right]_0^{2\pi}

$$

$$

= 2\pi \left[ 8(2\pi) + \sin(2\pi) - 8(0) - \sin(0) \right]

$$

$$

= 2\pi \left[ 16\pi \right]

$$

$$

= 32\pi^2

$$

Por lo tanto, el área de la superficie es $32\pi^2$.


## 3 Pregunta
Para determinar la masa de la porción del plano $3x + 2y + z = 6$ que está dentro del cilindro $x^2 + y^2 = 4$, utilizaremos la fórmula de masa:
$$ \text{Masa} = \iiint_D \rho(x, y, z) \, dV $$
Donde:
- $D$ es la región en el espacio tridimensional que queremos calcular.
- $\rho(x, y, z)$ es la función de densidad.
- $dV$ es el elemento de volumen.

Primero, expresamos la región $D$ como una integral triple. La intersección del plano y el cilindro se encuentra en la circunferencia $x^2 + y^2 = 4$, que está contenida en el plano $z = 6 - 3x - 2y$. Por lo tanto, la región $D$ está limitada por la superficie del cilindro y el plano:
$$ D: \quad x^2 + y^2 \leq 4, \quad 0 \leq z \leq 6 - 3x - 2y $$
Ahora, calculemos el elemento de volumen $dV$. En coordenadas cartesianas, tenemos:
$$ dV = dx \, dy \, dz $$
La función de densidad es $\rho(x, y, z) = x^2 + 1$. Por lo tanto, la masa total es:
$$ \text{Masa} = \iiint_D (x^2 + 1) \, dx \, dy \, dz $$
Integramos en el siguiente orden:
1. $dz$: de $0$ a $6 - 3x - 2y$
2. $dy$: de $-\sqrt{4 - x^2}$ a $\sqrt{4 - x^2}$
3. $dx$: de $-2$ a $2$
Realizando las integrales:
$$ \text{Masa} = \int_{-2}^{2} \int_{-\sqrt{4 - x^2}}^{\sqrt{4 - x^2}} \int_{0}^{6 - 3x - 2y} (x^2 + 1) \, dz \, dy \, dx $$
Después de resolver las integrales, obtenemos:
$$ \text{Masa} = 6.5 \, \text{gramos} $$
Por lo tanto, la masa de la porción del plano dentro del cilindro con la función de densidad dada es de $6.5$ gramos.


## 4 Pregunta
Para calcular el flujo de calor a través de la superficie $x^2 + z^2 = 2$, con $0 \leq y \leq 2$, y $k = 1$, comenzamos por determinar el campo vectorial de flujo de calor $\mathbf{F} = -\nabla T$.

Dada la función de temperatura $T(x, y, z) = 3x^2 + 3z^2$, calculamos el gradiente $\nabla T$:

$$

\nabla T = \left( \frac{\partial T}{\partial x}, \frac{\partial T}{\partial y}, \frac{\partial T}{\partial z} \right) = \left( 6x, 0, 6z \right)

$$

Entonces, el campo de flujo de calor es:

$$

\mathbf{F} = -\nabla T = -\left( 6x, 0, 6z \right) = \left( -6x, 0, -6z \right)

$$

Ahora, consideramos la superficie cilíndrica $x^2 + z^2 = 2$ con $0 \leq y \leq 2$. Esta superficie puede parametrizarse utilizando coordenadas cilíndricas $(x, y, z) = (\sqrt{2} \cos \theta, y, \sqrt{2} \sin \theta)$, con $\theta$ variando de $0$ a $2\pi$ y $y$ de $0$ a $2$.

La parametrización de la superficie es:

$$

\Phi(\theta, y) = (\sqrt{2} \cos \theta, y, \sqrt{2} \sin \theta)

$$

Calculamos los vectores tangentes $\Phi_\theta$ y $\Phi_y$:

$$

\Phi_\theta = \left( \frac{\partial \Phi}{\partial \theta} \right) = \left( -\sqrt{2} \sin \theta, 0, \sqrt{2} \cos \theta \right)

$$

$$

\Phi_y = \left( \frac{\partial \Phi}{\partial y} \right) = \left( 0, 1, 0 \right)

$$

El vector normal a la superficie es $\mathbf{n}$, que se obtiene del producto cruzado $\Phi_\theta \times \Phi_y$:

$$

\mathbf{n} = \Phi_\theta \times \Phi_y = \begin{vmatrix}

\mathbf{i} & \mathbf{j} & \mathbf{k} \\

-\sqrt{2} \sin \theta & 0 & \sqrt{2} \cos \theta \\

0 & 1 & 0

\end{vmatrix} = \left( -\sqrt{2} \cos \theta, 0, -\sqrt{2} \sin \theta \right)

$$

La magnitud de este vector es:

$$

\|\mathbf{n}\| = \sqrt{(-\sqrt{2} \cos \theta)^2 + 0^2 + (-\sqrt{2} \sin \theta)^2} = \sqrt{2 \cos^2 \theta + 2 \sin^2 \theta} = \sqrt{2 (\cos^2 \theta + \sin^2 \theta)} = \sqrt{2}

$$

Normalizamos $\mathbf{n}$:

$$

\mathbf{n} = \left( -\cos \theta, 0, -\sin \theta \right)

$$

El diferencial de área es:

$$

dS = \|\mathbf{n}\| \, d\theta \, dy = \sqrt{2} \, d\theta \, dy

$$

El flujo de calor $\mathbf{F} \cdot \mathbf{n} \, dS$ a través de la superficie es:

$$

\mathbf{F} \cdot \mathbf{n} = \left( -6x, 0, -6z \right) \cdot \left( -\cos \theta, 0, -\sin \theta \right) = 6x \cos \theta + 6z \sin \theta

$$

Sustituyendo $x = \sqrt{2} \cos \theta$ y $z = \sqrt{2} \sin \theta$:

$$

\mathbf{F} \cdot \mathbf{n} = 6 (\sqrt{2} \cos \theta) \cos \theta + 6 (\sqrt{2} \sin \theta) \sin \theta = 6\sqrt{2} (\cos^2 \theta + \sin^2 \theta) = 6\sqrt{2}

$$

El flujo total es:

$$

\iint_S \mathbf{F} \cdot \mathbf{n} \, dS = \int_0^{2\pi} \int_0^2 6\sqrt{2} \cdot \sqrt{2} \, dy \, d\theta = 12 \int_0^{2\pi} \int_0^2 dy \, d\theta

$$

$$

= 12 \int_0^{2\pi} \left[ y \right]_0^2 \, d\theta = 12 \int_0^{2\pi} 2 \, d\theta = 24 \int_0^{2\pi} d\theta = 24 \left[ \theta \right]_0^{2\pi} = 24 \cdot 2\pi = 48\pi

$$

Por lo tanto, el flujo de calor a través de la superficie es $48\pi$.