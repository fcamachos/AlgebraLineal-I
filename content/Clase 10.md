---
tags:
  - contexto/academico
  - tema/algebra-lineal
date: 2024-08-30
video:
  - https://www.youtube.com/watch?v=xf0iqNi3XVQ
---
# Operaciones elementales por filas 
aplicadas a una matriz $A$ de $m \times n$

Sean la ecuaciones:
$$
\begin{align}
3x -2y + 5z = -1 \\
2x + y = 0
\end{align}
$$
Estas pueden ser representadas mediante una matriz $A$ tal que:
$$
A = \begin{pmatrix}
3 & -2 & 5 & | & -1 \\
2 & 1 & 0 & | & 0
\end{pmatrix}
$$

Para resolver este sistema de ecuaciones


Hay 3 tipos de [[operaciones elementales por filas]]:


## 1. Intercambio de renglones distintos. 
$$
A \xrightarrow[i \neq j]{A_{i} \to A_{j}} A'
$$

> Ejemplo:

Sea la matriz $A_{3 \times 4}$:
$$
A= \begin{pmatrix}
0 & -1 & 2 & 3  \\
5 & 7 & -2 & 0  \\
0 & 0 & -2 & 1
\end{pmatrix}
$$
Aplicando el cambio de renglones $A_{1} \to A_{2}$ tenemos:

$$
\begin{pmatrix}
0 & -1 & 2 & 3  \\
5 & 7 & -2 & 0  \\
0 & 0 & -2 & 1
\end{pmatrix} 
\xrightarrow{A_{1}\to A_{2}} 
\begin{pmatrix}
5 & 7 & -2 & 0  \\
0 & -1 & 2 & 3  \\
0 & 0 & -2 & 1
\end{pmatrix}
$$


## 2. Multiplicación de un renglón por escalar

Multiplicar el $i-$ésimo renglón por un escalar $c \in F, c \neq 0$
$$
A \xrightarrow[]{A_{i} \to cA_{i}} A'
$$

> Ejemplo:

$$
A= \begin{pmatrix}
0 & -1 & 2 & 3  \\
5 & 7 & -2 & 0  \\
0 & 0 & -2 & 1
\end{pmatrix}
\xrightarrow[]{A_{3} \to \frac{1}{\pi}A_{3}}
\begin{pmatrix}
0 & -1 & 2 & 3  \\
5 & 7 & -2 & 0  \\
0 & 0 & -\frac{2}{\pi} & \frac{1}{\pi}
\end{pmatrix}
$$

## 3. Suma de escalar

Sumar al renglón $i$, $c$ veces el renglón, $c \in F$ y con $i \neq j$
$$
A \xrightarrow[]{A_{i} \to A_{i} + cA_{j}} A'
$$

> Ejemplo:

$$
A= \begin{pmatrix}
0 & -1 & 2 & 3  \\
5 & 7 & -2 & 0  \\
0 & 0 & -2 & 1
\end{pmatrix}
\xrightarrow[]{A_{2} \to A_{2}+(-1)A_{1}}
\begin{pmatrix}
0 & -1 & 2 & 3  \\
5 & 8 & -4 & -3  \\
0 & 0 & -2 & 1
\end{pmatrix}
$$


## Notación

Usamos letras $a,b,c \dots$ para denotar a una operación elemental por filas.
Si $A$ es una matriz de $m \times n$ y $e$ es una operación elemental por filas, denotamos por $eA$ a la matriz que se obtiene después de aplicar la operación elemental $e$ a la matriz $A$.

Además, si $e_{1}, \dots,e_{n}$ son operaciones elementales por filas:
$$
A \xrightarrow[]{e_{1}} e_{1}A \xrightarrow[]{e_{2}}e_{2} e_{1} A \dots \xrightarrow[]{e_{n}} e_{n} e_{n-1} \dots e_{2} e_{1} A
$$

## Ejemplo de operaciones elementales por filas:

Se resolverá el siguiente sistema de ecuaciones siguiendo el algoritmo de ?? 
$$
\begin{align}
3x +2y -z &= 0 \\
x +y +z &= 0 \\
x -z &= 0
\end{align}
$$

$$
\begin{pmatrix}
3 & 2 & -1 \\
1 & 1 & 1 \\
1 & 0 & -1
\end{pmatrix}
\xrightarrow[A_{3} \to A_{3}+ -\frac{1}{3}A_{3}]{A_{2} \to A_{2}+ -\frac{1}{3}A_{1}}
\begin{pmatrix}
3 & 2 & -1 \\
0 & \frac{1} {3} & \frac{4}{3} \\
0 & - \frac{2}{3} & - \frac{2}{3}
\end{pmatrix}
\xrightarrow[A_{3} \to 3A_{3}]{A_{2} \to 3A_{2}}
\begin{pmatrix}
3 & 2 & -1 \\
0 & 1 & 4 \\
0 & - 2 & - 2
\end{pmatrix}
\xrightarrow[A_{3} \to A_{3}+ -2A_{2}]{A_{1} \to A_{1}+ -2A_{2}}
\begin{pmatrix}
3 & 0 & -9 \\
0 & 1 & 4 \\
0 & 0 & 6
\end{pmatrix}
$$

$$
\xrightarrow[]{A_{3} \to \frac{1}{6} A_{1}}
\begin{pmatrix}
3 & 0 & -9 \\
0 & 1 & 4 \\
0 & 0 & 1
\end{pmatrix}
\xrightarrow[A_{1} \to A_{1} + 9A_{3}]{A_{2} \to A_{2} - 4 A_{3}}
\begin{pmatrix}
3 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix}
\xrightarrow[]{A_{1} \to \frac{1}{3} A_{1}}
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix}
$$
Por lo que la solución al sistema de ecuaciones es:
$$
\begin{align}
x &= 0 \\
y &= 0 \\
z &= 0
\end{align}
$$

