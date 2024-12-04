# Espacios vectoriales 


> [!ejemplo] Ejemplo 1


Dado $F$ un campo, $F$ es un $F-$espacio vectorial con las siguientes operaciones:
- la suma es, la suma definida en $F$.
- el producto por escalares es, el producto definido en el campo. 

Por lo tanto:
- $\mathbb{Q}$ es un $\mathbb{Q}-$ espacio vectorial.
- $\mathbb{R}$ es un $\mathbb{R}-$ espacio vectorial.
- $\mathbb{C}$ es un $\mathbb{C}-$ espacio vectorial.


>[!ejemplo] Ejemplo 2

Sea $F$ un campo y $n \in \mathbb{N}$. El producto cartesiano $F^{n} = F \times F \times \dots \times F$ es un $F-$espacio vectorial con las siguientes operaciones. 
$$
F^{n} = \left\{ (a_{1}, a_{2}, \dots , a_{n}) \quad | \quad a_{i} \in F, 1 \leq i \leq n \right\} 
$$
La suma:
$(a_{1}, a_{2}, \dots, a_{n}) + (b_{1}, b_{2}, \dots , b_{n}) = (a_{1}+b_{1}, a_{2}+b_{2}, \dots, a_{n} + b_{n})$

Un neutro aditivo:
$(0,0,\dots,0)$

Un inverso aditivo:
$(-a_{1}, -a_{2}, \dots, -a_{n})$

El producto por escalares:
$\lambda (a_{1}, \dots, a_{n}) = (\lambda a_{1}, \lambda a_{2}, \dots, \lambda a_{n})\qquad \lambda \in F$

## El espacio cero o espacio trivial

Sea $\{ x \}$ un conjunto con un solo elemento. 
Sea $F$ un campo.
$\{ x \}$ es un $F-$espacio vectorial con las siguientes operaciones:

$$
\begin{align*}
x + x &=  x\\
\lambda x &= x \qquad \forall \lambda \in F
\end{align*}
$$

$$
\begin{align*}
x + (x+x) &=  x+x &=  x\\
(x+x) +x &= x+x &= x
\end{align*}
$$
$x$ es neutro aditivo pues: $x +x = x$.
$x$ es inverso aditivo de $x$, pues $x+x = x$.
$1_{F}x = x$

$\lambda (\mu x) = \lambda x = x$
$(\lambda \mu) x = x$

$(\lambda + \mu) x = x$
$\lambda x + \mu x = x + x = x$

$\lambda (x+x) = \lambda x = x$
$\lambda x + \lambda x = x+x = x$

Por lo tanto $V = \{ x \}$ es un $F-$espacio vectorial.


>[!ejemplo] Nota:
>A los elementos de un espacio vectorial los llamamos vectores.


Sean $m,n \in \mathbb{N}$, y sea $\mathcal{M}_{m \times n} (F) = \left\{ \quad (a_{ij}) \quad | \quad a_{ij} \in F, 1 \leq i \leq m, 1 \leq j \leq n \quad \right\}$
> $(a_{ij}) + (b_{ij}) = (a_{ij} + b_{ij})$
> $\lambda(a_{ij}) = (\lambda a_{ij})$
> $1_{F} (a_{ij}) = (1_{F}a_{ij}) = (a_{ij})$

## Subespacios vectoriales

>[!def] subespacio vectorial
>Sea $V$ en $F-$espacio vectorial, y $S$ un subconjunto de $V$.
>Diremos que $S$ es un subespacio de $V$ si satisface: 
>   1.  $S \neq \emptyset$
>   2. $\forall v, v' \in S, \quad  \underset{ S \text{ es cerrado bajo la suma} }{ v + v' \in S }$
>   3. $\forall \lambda \in F, \quad \forall v \in S, \quad  \underset{ S \text{ es cerrado bajo el producto por escalares} }{ \lambda v \in S }$




