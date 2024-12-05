---
tags:
  - contexto/academico
  - tema/algebra-lineal
date: 2024-09-02
video:
  - https://www.youtube.com/watch?v=8U4QEu1gvyo
---
Recordemos [[Clase 10#Notación]]

# Forma escalonada reducida por filas

Sea $R$ una matriz de $m \times n$. Diremos que $R$ está en la forma escalonada reducida por filas si $R= (0)$ ó $R$ satisface lo siguiente:

- i) Los renglones nulos de $R$ están debajo de los renglones no nulos de $R$. 
$$
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 0 \\
0 & 0 & 0
\end{pmatrix}
$$
	Esto es, si $R$ tiene $r$ renglones no nulos, entonces $R_{r+1}, \dots, R_{m}$ son los renglones nulos de $R$.
	
- ii) Para cada $i \geq 2$, la primera entrada no nula del renglón no nulo $R_{i}$ está en la columna a la derecha de la primera entrada no nula del renglón $R_{i-1}$.  Esto es, si $R_{i}$ es un renglón no nulo de R y la primera entrada distinta de cero está en la entrada $(i,k_{i})$, entonces, $k_{i-1} < k_{i}$.
- iii) Si $R_{1},\dots, R_{r}$ son los renglones no nulos de $R$ y $a_{1 k_{1}},a_{2k_{2}}, \dots, a_{rk_{r}}$ son las primeras entradas no nulas de $R_{1},\dots, R_{r}$ contando de izquierda a derecha, entonces: $a_{1k_{1}} = a_{2k_{2}} =\dots = a_{rk_{r}}=1$


> Ejemplo:

$$
\begin{align}
\begin{pmatrix}
0 & -1 & 2 & 7 & 9 & 20 \\
0 & 0 & 1 & -2 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 27
\end{pmatrix}
\end{align}
$$
Esta matriz cumple con:
- i) No hay renglones nulos
- ii) Sí cumple pues toda entrada diferente de cero está más a la derecha que el renglón superior.
- iii) No cumple porque los elementos más a la derecha no son 1's.


## 2 x 2

Describir todas las matrices de $2 \times 2$, distintas a la matriz cero, con entradas reales, que estén en la forma escalonada reducida por filas. 

$a,b,c,d \in \mathbb{R}$
$$
A = \begin{pmatrix}
a & b \\
c & d
\end{pmatrix} \neq 
\begin{pmatrix}
0 & 0  \\
0 & 0
\end{pmatrix}
$$

Si $A \neq (0)$, tenemos dos posibilidades. Que el primer renglón de $A$ es no nulo o el segundo es no nulo.

> Caso 1
> El primer renglón es no nulo.

En este caso tenemos que $a \neq 0$ ó $b \neq 0$.

>> Si $a \neq 0$, entonces $a = 1$
$$
\begin{pmatrix}
1 & b \\
c & d
\end{pmatrix}
$$


Ahora bien, si el segundo renglón es nulo entonces:
$$
\begin{pmatrix}
1 & b \\
0 & 0
\end{pmatrix}
$$
Si el segundo renglón es no nulo, entonces: $c \neq 0$ ó $d \neq 0$. Pero, $c \neq 0$ no es posible porque la matriz satisface ii).
Por lo tanto, $d \neq 0$ y $d$ es la primera entrada no nula del segundo renglón, por lo que $d = 1$:
$$
\begin{pmatrix}
1 & b \\
0 & 1
\end{pmatrix}
$$

>> Si $b \neq 0$ y $a = 0$ entonces:


 $$\begin{pmatrix}0 & 1\\c & d\end{pmatrix}$$

Por lo tanto, $c = 0$ y $d = 0$:
$$
\begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix}
$$

