---
date: 2024-09-18
video:
  - https://www.youtube.com/watch?v=RtcJVNyo32g
tags:
  - contexto/academico
  - tema/algebra-lineal
---

video:
  - ![](https://www.youtube.com/watch?v=RtcJVNyo32g)

# Matriz invertible

Sea $A$ una matriz de $n \times n$, $A$ es invertible si existe una matriz $B$ de $n \times n$ tal que 
$$
AB = I = BA
$$

# Matriz inversa

Sea $A$ una matriz de $n \times n$, entonces, existe una única matriz $B$ de $n \times n$ tal que $AB = I = BA$.

`\begin{proof}`

Supongamos que B y B' son matrices de $n \times n$ tales que $AB = I = BA$ y $AB' = I = B'A$

> PD
> $B = B'$

$B' = B'I = B' (AB) = (B' A)B = IB = B$

`\end{proof}`

$B$ se llama *la inversa de $A$* y la denotamos como $A^{-1}$.

## Matriz inversa de I

La matriz identidad $I$ de $m \times n$ es invertible, ya que $II=I$. En particular $I^{-1} = I$.


## Inversa de productos

Si $A$ y $C$ son matrices invertibles, entonces $AC$ es invertible y $(AC)^{-1} = C^{-1}A^{-1}$.

`\begin{proof}`

Probemos que
$$
(AC)(C^{-1}A^{-1}) = I \qquad \text{y} \qquad (C^{-1}A^{-1})(AC) = I
$$
luego, se sigue por la unicidad de la inversa que $(AC)^{-1} = C^{-1}A^{-1}$.

Comenzando:
$$
\begin{align*}
(AC)(C^{-1}A^{-1}) &= A(CC ^{-1})A^{-1}\\
&= A I A^{-1} \\
&= A A^{-1}\\
&= I
\end{align*}
$$
Por otro lado:
$$
\begin{align*}
(C^{-1}A^{-1})(AC) &= C^{-1} (A ^{-1} A) C\\
&= C ^{-1} I C\\
&= C ^{-1} C\\
&= I
\end{align*}
$$
`\end{proof}`


### Inversa de productos extensos

Sean $A_{1}, A_{2}, \dots, A_{r}$ matrices invertibles de $n \times n$, entonces el producto $A_{1} A_{2} \dots A_{n}$ es invertible y 
$$
(A_{1}A_{2}\dots A_{n})^{-1} = A^{-1} _{n} A^{-1} _{n-1} \dots A^{-1} _{2} A^{-1} _{1}
$$
## Matriz elemental

Sea $E$ una matriz de $n \times n$, $E$ es una matriz elemental si existe una [[operaciones elementales por filas]] $e$, tal que: $E = eI$

### Operación elemental inversa

Sea $e$ una operación elemental por filas. Entonces  $e ^{-1}$ es su operación inversa:
$$
\begin{align*}
A \xrightarrow[]{e} eA \xrightarrow[]{e ^{-1}} e^{-1}eA &=  A\\
A \xrightarrow[]{e ^{-1}} e ^{-1} A \xrightarrow[]{e } e e^{-1}A &=  A
\end{align*}
$$

###  Multiplicación de una Matriz elemental con otra

Sea A una matriz de $n \times n$ y $E ^{ij}$ una [[matriz canónica]] de $n \times n$

[[matriz canónica#^92e293]] 

, entonces:

$E ^{ij} A$ Es la matriz de $n \times n$ cuyo $i-$ésimo renglón es igual al $j-$ésimo renglón de $A$ y todos los demás renglones de $E^{ij}A$ son $0$.


### Formas de una matriz elemental


> [!lemma] 
> Una matriz elemental $E$ de $n \times n$ es de una de las siguientes formas:
> a)
> $$E = eI $$
> si $e$ es $i \leftrightarrow j \qquad i \neq j$
> $$E = I - E ^{ii} - E ^{jj} + E ^{ ij} + E ^{ji} \qquad j \neq i$$
> b)
> Si $e$ es $i \to ci \quad c \neq 0$
> $$E = I - E ^{ii} + c E ^{ii}, \quad c \neq 0$$
> c)
> Si $e$ es $i \to i + cj\qquad i \neq j, c \in F$
> $$E = I + c E ^{ij} \qquad c \in F, i \neq j$$

> Ejemplo: b)

$$
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix}_{I}
\xrightarrow[A_{2} \to 3 A_{2}]{e}
\begin{pmatrix}
1 & 0 & 0 \\
0 & 3 & 0 \\
0 & 0 & 1
\end{pmatrix}_{eI =E}
$$
$$
\begin{align}
i &= 2  \qquad \text{Por el segundo renglón } A_{2} \\
c &= 3
\end{align}
$$
$$
\begin{pmatrix}
1 & 0 & 0 \\
0 & 3 & 0 \\
0 & 0 & 1
\end{pmatrix}_{E} = 
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix}_{I} - 
\begin{pmatrix}
0 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 0
\end{pmatrix}_{E^{ii}} +
3 \begin{pmatrix}
0 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 0
\end{pmatrix}_{c E ^{ii}}
$$
$$
\begin{align*}
&= \begin{pmatrix}
1 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 1
\end{pmatrix} + \begin{pmatrix}
0 & 0 & 0 \\
0 & 3 & 0 \\
0 & 0 & 0
\end{pmatrix}= \begin{pmatrix}
1 & 0 & 0 \\
0 & 3 & 0 \\
0 & 0 & 1
\end{pmatrix}
\end{align*}
$$


> Ejemplo de cómo encontrar la matriz inversa, en el [video](https://youtu.be/RtcJVNyo32g?si=8y-I-u4K1Spbd2GH&t=3060), minuto 51.


