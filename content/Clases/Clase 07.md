---
date: 2024-08-21
video: 
tags:
  - contexto/academico
  - tema/algebra-lineal
---

[[matriz]]
> De ahora en adelante, los elementos del [[campo]] $F$ los llamaremos [[escalares]].

# Producto por escalares

> [!def] Producto por escalar
Sea $A = (a_{ij})$ una matriz de $m \times n$ y $\lambda \in F$. Definimos $\lambda A$ como la matriz de $m \times n$ cuya entrada $(i,j)$ es $(\lambda A)_{(i,j)}= \lambda A_{(i,j)} = \lambda a_{ij}$

^79f32d

> Ejemplo:

$\lambda = 2$
$$
\begin{align}
A &= \begin{pmatrix}
-1 & 5 & 3 & 8  \\
0 & 1 & 1 & 1 \\
4 & 2 & 2 & 0
\end{pmatrix} \\
2A &= \begin{pmatrix}
-2 & 10 & 6 & 16 \\
0 & 2 & 2 & 2 \\
8 & 4 & 4 & 0
\end{pmatrix}
\end{align}
$$
## Propiedades del producto por un escalar 

Sean $A \text{ y } B$ matrices de $m \times n$ y $\alpha, \beta \in F$

>[!prp|a)] Asociativa
>$\alpha (\beta A) = (\alpha \beta)A$

^a88a93

>[!prp|b)] Neutro
> $1_{F}A = A$

^85f5fe

>[!prp|c)] Distribución
>$\alpha (A+B)= \alpha A + \alpha B$

^69d19c

>[!prp|d)] Distribución II
>$(\alpha + \beta)A= \alpha A + \beta A$

^f2a63e

`\begin{proof}`@[[#^a88a93]] 
P.D. $(\alpha (\beta A))_{(i,j)}=((\alpha \beta)A)_{(i,j)}$ 

Por [[#^79f32d]] tenemos que:
$$
\begin{align}
(\alpha(\beta A))_{(i,j)} &= (\alpha (\beta A)_{(i,j)})_{(i,j)}  \\
&= (\alpha(\beta a_{ij}))_{(i,j)} \\
&= (\alpha  \beta a_{ij}) \\
&_{\text{Por asociatividad}}  \\
&= (\alpha\beta)a_{ij} \\
&= ((\alpha\beta)A)_{(i,j)}
\end{align}
$$

`\end{proof}`

`\begin{proof}`@[[#^85f5fe]] 

P.D. $(1 A)_{(i,j)} = (A)_{(i,j)}$

Por [[#^79f32d]] tenemos que:
$$
\begin{align}
(1A)_{(i,j)} &= 1 a_{ij} \\
&= a_{ij} \\
&= (A)_{(i,j)}
\end{align}
$$

`\end{proof}`

`\begin{proof}`@[[#^69d19c]] 

P.D. $(\alpha (A+B))_{(i,j)} = (\alpha A + \alpha B)_{(i,j)}$ 

Teniendo en cuenta: 
- [[#^79f32d]] 
- [[campo#^f59fca]] 
- [[Clase 06#^70b466]]   
 
Tenemos que:
$$
\begin{align}
(\alpha (A+B))_{(i,j)} &= \alpha (A+B)_{(i,j)} \\
&= \alpha (A_{(i,j)} + B_{(i,j)}) \\
&= \alpha \left( a_{ij} + b_{ij} \right)  \\
& _{\text{Por distribución:}} \\
&= \alpha a_{ij} + \alpha b_{ij} \\
&= \alpha A_{(i,j)} + \alpha B_{(i,j)} \\
&_{\text{Por def. suma de matrices}} \\
&= (\alpha A + \alpha B)_{(i,j)}
\end{align}
$$
`\end{proof}`

`\begin{proof}`@[[#^f2a63e]] 

P.D.  $(\alpha + \beta)A_{(i,j)} = \alpha A_{(i,j)} + \beta A_{(i,j)}$ 

Teniendo en cuenta:
- [[#^79f32d]] 
- [[campo#^f59fca]] 
Tenemos que:
$$
\begin{align}
(\alpha + \beta)A_{(i,j)} &= (\alpha + \beta) a_{ij}  & \text{Def. 1}\\
&=\alpha a_{ij} + \beta a_{ij} & \text{Axm. 9} \\
&=\alpha A(_{i,j}) + \beta A_{(i,j)}
\end{align}
$$

`\end{proof}`

# Producto de matrices

Sea $A=(a_{il})$ una matriz de $m \times n$ y $B=(b_{lj})$ una matriz de $n \times q$.
>[!cor|*] Condición de multiplicidad
>El número de columnas de la primer matriz debe ser igual que el número de filas de la segunda.

>[!def] Producto AB
> Consideremos: $1 \leq i \leq m \quad 1 \leq l \leq n \quad 1 \leq j \leq q$ 
> El producto $A_{m \times n}B_{n \times q}$ da una matriz  $P_{m \times q}$  cuya entrada $(i,j)$ es:
> $$ (AB)(i,j) = \sum_{l=1}^{n} a_{il}b_{lj}  $$

^ad1ebf

## Otra forma de recordarlo: 

Sea $A=(a_{ij})$ de $m \times n$. Denotamos por $A_{i}$ al $i-$ésimo renglón de $A$, $1 \leq i \leq m$. 
$$
A_{i} = \begin{pmatrix}
a_{i1}  &  a_{i 2}  &  \dots  &  a_{i n}
\end{pmatrix}_{1 \times n}
$$
Denotamos por $A^{j}$ a la $j-$ésima columna de $A$
$$
A^{j} = \begin{pmatrix}
a_{1j} \\
a_{2j} \\
\vdots  \\
a_{mj}
\end{pmatrix}_{m \times 1}
$$
$$A_{i} B^{j} = \begin{pmatrix} a_{i1} & a_{i 2} & \dots & a_{i n} \end{pmatrix} \begin{pmatrix} b_{1j} \\ b_{2j} \\ \vdots \\ b_{nj} \end{pmatrix} = \sum_{l=1}^{n} a_{il} b_{lj} = (AB)_{(i,j)}$$
Es decir:
$$
\begin{pmatrix}
A_{1}B^{1}  & A_{1}B^{2} & A_{1}B^{j}  & A_{1}B^{q} \\
A_{2}B^{1} & A_{2}B^{2}  & A_{2}B^{j} & A_{2}B^{q}  \\
A_{i}B^{1} & A_{i}B^{2} & A_{i}B^{j} & A_{i}B^{q} \\
A_{m}B^{1} & A_{m}B^{2} & A_{m}B^{j} & A_{m}B^{q}
\end{pmatrix}
$$

