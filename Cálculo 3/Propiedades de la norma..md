Metadata:
Fecha: 28-08-2023
Hora: 11:56
Título: Propiedades de la norma.

Sea $$\mathbb{R}^2,\tau_{E}\subsetneq \tau_O$$
1. $$\begin{align*} \text{Id}:(\mathbb{R}^2,\tau_O)&\longrightarrow(\mathbb{R}^2,\tau_E)\\ u&\longmapsto u \end{align*}$$ Si $B_r(u_0)$ es un bola con centro $u_0\in\mathbb{R}$ y radio $r\in\mathbb{R}_+,B_r(u_0)\in\tau_E$, así $\text{Id}^{-1}\big( B_r(u_0) \big)=B_{r_0}(u)$ y sabemos que $B_r(u_0)\in\tau_O$, $\text{Id}$ es continua.

2. $$\begin{align*} \text{Id}:(\mathbb{R}^2,\tau_E)&\longrightarrow(\mathbb{R}^2,\tau_0)\\ u&\longmapsto u \end{align*}$$ Tomando $$\text{I}_2=\Big\{ (x,y)\in\mathbb{R}^2\big|x=0\land |y|<2 \Big\}\subset\mathbb{R}^2$$ tenemos que $\text{I}_2=\text{Id}^{-1}(\text{I}_2)$ pero $\text{I}_2\notin\tau_E$. 
   $\therefore$ No es continuo $\text{Id}$.


Como sabemos si $u,v\in\mathbb{R}^n$ $$u\cdot v=u\text{ I }v^{\top}$$ donde $u$ y $v$ los vemos como vectores fila y $\text{I}$ es la matriz identidad en $\mathcal{M}_n(\mathbb{R})$. $$||u||=(u\cdot u)^{\frac{1}{2}}$$
Sean $u,v,w\in\mathbb{R}^n$ y $\alpha,\beta,\gamma\in\mathbb{R}$
1. $(\alpha u)\cdot\gamma=\alpha(u\cdot v)$
2. $u\cdot v=v\cdot u$
3. $(u+v)\cdot w=u\cdot w+v\cdot w$
4. $u\cdot\theta=0$
5. $u^2=u\cdot u\geq0$
6. $u\cdot(\alpha v+\beta w)=\alpha u\cdot v+\beta u\cdot w$
7. $(u+v)\cdot(u+v)=u^2+v^2+2u\cdot v$


##### Propiedades de la norma.
1. $||u||\geq0\land ||u||=0$ sí y sólo si $u=0$.
2. $||\alpha u||=|\alpha|\ ||u||$.
3. $||u+v||\leq ||u||+||v||$.
4. $|u\cdot v|\leq ||u||\ ||v||$.
5. $||u-v||=||v-u||$.