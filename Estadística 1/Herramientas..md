Metadata:
18-08-2023
07:19
Herramientas.

## Apunte.
---
###### Página del curso.
---
La plataforma que usaremos es [Piazza](https://piazza.com/unam.mx/other/ei20241), el código de acceso es **150621**.


##### Breve introducción a $\LaTeX$.
---
$\LaTeX$ es una herramienta para crear documentos de una gran calidad tipográfica en donde los usuarios se ocupan en mayor medida al contenido del texto en lugar del formato.

###### Principales clases de documentos.
---

| Clase | Propósito |
| ---- | ---- |
| article | Artículos para revistas |
| report | Textos largos como tesis o reportes |
| book | Libros o documentos con una estructura similar |
| letter | Cartas |

###### Paquetes.
---

| Nombre | Función |
| --- | --- |
| amsmath amssymb amsfont | Permiten el uso de símbolos matemáticos |
| babel | Escribir en diversos idiomas |
| inputec | Codificación de entrada |

###### Estructura de un documento.
---
\\documentclass\[11pt,a4paper\]{report}
\\usepackage\[utf8\]{inputec}
- [x] \\usepackage\[spanish\]{babel}
- [x] \\usepackage{amsmath}
- [x] \\usepackage{amssymb}
- [x] \\usepackage{amsfont}
\\title{Título}
\\author{Nombre}
\\date{today}
\\begin{document}
\\maketitle
...
...
...
\\end{document}

###### $\LaTeX$ en línea.
---
- Crear una cuenta en [Overleaf](https://es.overleaf.com).
- New project
	- Blank project
		- Escribir nombre del documento
			- Create
- Menu
	- Spell check spanish

###### Partes de un documento.
---
\\section*{  } con número
\section{  } sin número
\\subsection{  }
\\subsubsection{  }
\\part{  }
\\chapter{  }
\\textbf{Negrita}
\\textit{cursiva}

###### Tamaños de fuente.
---
\\Huge
\\huge
\\LARGE
\\Large
\\large
\\normalsize
\\small
\\tiny

###### Listas numeradas y viñetas.
---
\\begin{itemize}
	\\item Viñeta 1
	\\item Viñeta 2
\\end{itemize}

\\begin{enumerate}\[a)\]
	\\item Punto 1
	\\item Punto 2
\\end{enumerate}

###### Alineación del texto.
---
\\begin{center}
	...
	...
	...
\\end{center}
(flushleft, flushright)

###### Composición de ecuaciones.
---
$x^2+2x+3=0$
\$x^2+2x+3=0\$

###### Alinear expresiones con algún elemento.
---
$$\begin{align*} c^2&=a^2+b^2\\ &=2^2+3^2\\ &=13 \end{align*}$$
\$\$\\begin{align*}
	c^2&=a^2+b^2\\\\
	&=2^2+3^2\\\\
	&=13
\\end{align*}\$\$

###### Tablas.
---
\\begin{table}\[h]
	\\centering
		\\begin{tabular}{c | c c}
			a & b & c
		\\end{tabular}
\\end{table}

a | b c

| Var 1 | Var 2 | Var 3 |
| --- | --- | --- |
| 1 | 2 | 3 |

\\begin{tabular}{| c | c | c |}
	\\hline
		Var 1 & Var 2 & Var 3 \\\\
	\\hline
		1 & 2 & 3 \\\\
	\\hline
\\end{tabular}

###### Insertar una imagen.
---
\\usepackage{graphicx}
\\includegraphics\[width= ancho, height=alto]{imagen.jpg}
	\[scale=escala]


Además estaremos usando ``R``, [[Breve introducción a R.]]

