### Ejercicio 1.
---
1. La probabilidad de que sea hombre y fume. $P(H\cap F)$.
	Solución:
	$$\begin{align*} P(A|B)&=\frac{P(A\cap B)}{P(B)}\\ P(A\cap B)&=P(A|B)P(B)\\ \text{sustituimos}\\ P(H\cap F)&=P(F\cap H)\\ &=P(F|H)P(H)\\ &=0.30(0.60)\\ &=0.18 \end{align*}$$
2. La probabilidad de que sea hombre y no fume. $P(H\cap NF)$.
	Solución:
	$$\begin{align*} P(H\cap NF)&=P(NF\cap H)\\ &=P(NF|H)P(H)\\ &=0.7(0.6)\\ &=0.42 \end{align*}$$
3. La probabilidad de que sea mujer y fume. $P(M\cap F)$.
	Solución:
	$$\begin{align*} P(M\cap F)&=P(F\cap M)\\ &=P(F|M)P(M)\\ &=0.2(0.4)\\ &=0.08 \end{align*}$$
4. La probabilidad de que sea mujer y no fume. $P(M\cap NF)$.
	Solución:
	$$\begin{align*} P(M\cap NF)&=P(NF\cap M)\\ &=P(NF\cap M)\\ &=0.4(0.8)\\ &=0.32 \end{align*}$$
5. La probabilidad de que sea hombre dado que se sabe que fuma.
	Solución:
	$$\begin{align*} P(H|F)&=\frac{P(H\cap F)}{P(F)}\\ &=\frac{P(F|H)P(H)}{P(F|H)P(H)+P(F|M)P(F)}\\ &=\frac{0.18}{0.18+0.08}\\ &=\frac{0.18}{0.26}\\ &=\frac{9}{13}\\ &\approx0.6923 \end{align*}$$
6. La probabilidad de que sea mujer dado que se sabe que no fuma.
	Solución:
	$$\begin{align*} P(M|NF)&=\frac{P(M\cap NF)}{P(NF)}\\ &=\frac{P(NF|M)P(M)}{P(NF|M)P(M)+P(NF|H)+P(NF)}\\ &=\frac{0.32}{0.32+0.42}\\ &=\frac{0.32}{0.74}\\ &=\frac{0.16}{0.37}\\ &\approx 0.4324\end{align*}$$

### Ejercicio 2.
---
Si $$\begin{matrix} f(x)=\begin{cases} x^2+\frac{4x}{3}&\text{ si }0\leq x\leq 1;\\ 0&\text{en otros casos} \end{cases}\\ \begin{align*} E(x)&=\int_{-\infty}^{\infty}xf(x)dx\\ &=\int_0^1x(x^2+\frac{4x}{3})dx\\ &=\int_0^1x^3+\frac{4x^2}{3}dx\\ &=\frac{x^4}{4}+\frac{4}{3}\frac{x^3}{3}\bigg{|}_0^1\\ &=\frac{x^4}{4}+\frac{4}{9}x^3\bigg{|}_0^1\\ &=\frac{1}{4}+\frac{4}{9}\\ &=\frac{9+16}{36}\\ &=\frac{25}{36} \end{align*} \end{matrix}$$

### Ejercicio 3.
---
Si $$f(x)=\begin{cases} e^{-x}&\text{si }x>0\\ 0&\text{en otros casos} \end{cases}$$ calcular lo siguiente: $$\begin{align*} M_x(t)&=E(e^{tx})\\ &=\int_{0}^{\infty}e^{tx}e^{-x}dx\\ E(x^2)&=\int_{-\infty}^{\infty}x^2f(x)dx\\ &=\int_{0}^{\infty}e^{x(t-1)}dx\\ \int e^{kx}dx&=\frac{1}{k}e^{kx}\\ e^{kx}&=\frac{1}{k}e^{kx}d(kx)\\ &=\frac{1}{k}e^{kx}k\\ &=e^{kx} \end{align*}$$

### Ejercicio 4.
---
Si $$f(x,y)=\begin{cases} 2ye^{-x}&\text{si }0<y<1,\ x>0\\ 0&\text{en otros casos} \end{cases}$$
Encuentra $F(x,y)$.
	Solución:
	Caso cuando $0<y<1,\ x>0$ $$\begin{align*} F(x,y)&=\int_{-\infty}^x\int_{-\infty}^{y}f(u,v)dv\ du\\ &=\int_{-\infty}^{x}\int_{-\infty}^{y}2ve^{-u}dv\ du\\ &=\Bigg{[}\int_0^x\bigg{[}\int_0^y2ve^{-u}dv\bigg{]}du\Bigg{]}\\ &=\int_0^x\bigg{[}\frac{2v^2}{2}e^{-u}\Big{|}_0^{y}\bigg{]}du\\ &=\int_0^xy^2e^{-u}du\\ &=y^2\int_0^xe^{-u}du\\ &=y^2\Big{[}-1\cdot e^{-u}\Big{]}\bigg{|}_0^x\\ &=y^2\Big{[}-e^{-x}-(-e^{-0})\Big{]}\\ &=y^2[-e^{-x}+1]\\ &=y^2(1-e^{-x}) \end{align*}$$
	Caso cuando $y\geq 1$ $$\begin{matrix} \lim_{y\to\infty}F(x,y)=F(x)\\ F(x)=\frac{d}{dx}f(x)\\ f(x)=\int F(x)\ dx\\ \\ \begin{align*} f(x)&=\int_0^12ye^{-x}\ dy\\ &=e^{-x}\\ \\ F(x)&=\int_{-\infty}^{x}f(u)\ du\\ &=\int_0^xe^{-u}\ du\\ &=1-e^{-x} \end{align*}\\ \\ F(x,y)=\begin{cases} 0&\text{si }x\leq 0,\ y\leq 0\\ y^2(1-e^{-x})&\text{si }x>0,\ 0<y<1\\ 1-e^{-x}&\text{si }x>0,\ y\geq 1 \end{cases} \end{matrix}$$
