$A$ es una matriz escalonada reducida por filas (FER) si:

1. Todos los renglones nulos de $A$ están abajo.
2. El primer término no nulo de un renglón de $A_{i}$ (pivote) está más a la derecha que el renglón de arriba. 
3. Los "pivotes" deben ser 1, y el resto de términos en la columna deben ser 0. 

> Ejemplo de matriz escalonada reducida:

$$
A =
\begin{pmatrix}
1 & -1 & 0 & 2  \\
0 & 0 & 1 & -1 \\
0 & 0 & 0 & 0
\end{pmatrix}
$$

Ejemplo 2:
 > $$\begin{pmatrix}1 & 2 & 0\\0 & 0 & 1 \\ 0 & 0 & 0 \end{pmatrix}$$
 > En las columnas pivote, el resto es cero, cuando no se trata de un pivote, el número puede ser distinto de $1$.
 
 