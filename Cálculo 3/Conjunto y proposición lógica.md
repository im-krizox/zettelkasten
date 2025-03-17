## Conjunto.
---
Una agrupación (*colección*) de objetos en un universo que hacen verdadera una proposición lógica abierta.

**Proposición lógica:** 


### Unión, intersección y otras operaciones.
---
#### Unión:
$$A\cup B=\Big{\{}x\in\mathbb{U}|P(x)\lor Q(x)\Big{\}}$$ $$A\cap B=\Big{\{}x\in\mathbb{U}|P(x)\land Q(x)\Big{\}}$$ $$A\subset B\Longleftrightarrow\forall x\in A:Q(x)$$ $$A\subsetneq B=A\subset B\land B\not\subset A$$ $$\mathbb{U}\backslash A,A^C x\in\mathbb{U}:¬P(x)$$ $$A\backslash B:=\Big{\{}x\in\mathbb{U}|P(x)\land¬Q(x)\Big{\}}$$ $$A\not\subset B\Rightarrow\exists xA:¬Q(x)$$ $$A=B\Leftrightarrow A\subset B\land B\subset A$$ $${(A^C)}^C=A$$ $$A-B\cup B-A$$ 

## Producto cartesiano.
---
Sean $A$ y $B$ dos conjuntos.
- Una pareja ordenada $(x,y)=\big{\{}x,\{x,y\}\big{\}}$.
- $x$ es la primera entrada.
- $y$ la segunda entrada.
$$(x,y)\neq(y,z)$$ $$\big{\{}x,\{x,y\}\big{\}}^{\not\subset}_{\not\supset}\big{\{}y,\{x,y\}\big{\}}$$ $$A\times B:=\big{\{} (a,b)|a\in A\land b\in B \big{\}}$$ $$A=B\Rightarrow A^2=A\times A$$
$$\Big{\{}a,\big{\{}a,\{a\}\big{\}}\Big{\}}$$ $$A\times B\times C:=\big{\{}(a,b,c)|a\in A\land b\in B\land c\in C\big{\}}$$

Ahora para un conjunto de $n$ elementos
$A_1,\ldots,A_n$ son un conjunto
$${\prod}_{i=1}^nA_i=A_1\times\ldots\times A_n:=\big{\{}\underbrace{(x,\ldots,x_n)}_{\text{n-tuplas}}|x_1\in A_1\land\ldots\land x_n\in A_n\big{\}}$$ 

## Función.
---
Sean $A$ y $B$ dos conjuntos $F\subset A\times B$ es una función si $\forall a \in A,\exists!b\in B:(a,b)\in F$, $(a,b)=(a,c)\Leftrightarrow b=c$.

- Función identidad.
- Función constante.
- Función fuera del dominio.
- Funciones inyectivas.
- Funciones subyectivas.
- Funciones suprayectivas.

 
