Metadata:
Fecha: 30-08-2023
Hora: 07:54
Título: Topología producto y topología caja.

## Topología producto.
Si $X$ y $Y$ son espacios topológicos la **topología producto** en $X\times Y$ es la que tiene por base a los productos de abiertos de $X$ con abiertos de $Y$.

#### Ejemplos.
- La topología producto en $\mathbb{R}\times\mathbb{R}$ tiene por base a los rectángulos abiertos $(a,b)\times(c,d)$ y es la misma que la topología usual en $\mathbb{R}^2$.
- Un anillo es el producto de un circulo y un intervalo.
- El toro es homeomorfo al producto $S^{1\times}S^1$, el toro sólido es homeomorfo a $D^{2\times}S^1$.
- $\mathbb{N}\times\mathbb{N}\cong\mathbb{N}$.

### Observaciones.
- La topología producto en $X\times Y$ hace a las proyecciones $p_{1}:X\times Y\rightarrow X$ y $p_{2}:X\times Y\rightarrow Y$ continuas y es la topología mas gruesa en $X\times Y$ con esta propiedad.
- Una función $f:X\rightarrow Y\times Z$ es continua si y solo si las funciones coordenadas $f_1:X\rightarrow Y$ y $f_2:X\rightarrow Z$ son continuas, ya que si $A\times B$ es un abierto básico de $Y\times Z$, entonces $f^{-1}(A\times B)=(f_1^{-1}(A)\cap(f_2^{-1}(B)))$.


## Topología caja (box).
En la topología caja, la base viene dada por los productos cartesianos de los conjuntos abiertos de los espacios componentes.

Aunque la topología caja tiene una definición algo más intuitiva que la topología producto, satisface menos propiedades deseables. En particular, si todos los espacios componentes son compactos, la topología de caja sobre su producto cartesiano no será necesariamente compacta, aunque la topología producto sobre su producto cartesiano siempre será compacta. En general, la topología caja es más fina que la topología producto, aunque ambas coinciden en el caso de productos directos o finitos (o cuando todos los factores son triviales, pero no todos).

>[!info] Definición.
>Sea $X$ tal que $$X:=\prod_{i\in I}X_i,$$ o el producto cartesiano (posiblemente infinito) de los espacios topológicos $X_i$, indexado por $i\in I$, la topología caja en $X$ es generado por la base $$\mathcal{B}=\Bigg\{ \prod_{i\in I}U_{i}\big| U_{i}\text{ abierto en }X_{i} \Bigg\}$$


### Propiedades.
La topología caja en $\mathbb{R}^{\omega}$:
- La topología caja es completamente regular.
- La topología caja no es compacta ni conexa.
- La topología caja no es contable en primer lugar (por tanto, no es metrizable).
- La topología caja no es separable.
- La topología caja es paracompacta (y, por tanto, normal y completamente regular) si se cumple la hipótesis del continuo.

