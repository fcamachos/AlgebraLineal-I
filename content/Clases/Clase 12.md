---
date: 2024-09-04
video:
  - https://www.youtube.com/watch?v=2uUnlDYrfO0
tags:
  - contexto/academico
  - tema/algebra-lineal
---

video:
  - ![](https://www.youtube.com/watch?v=2uUnlDYrfO0)

# Pivotes 


Sea $A = (a_{ij})$ una matriz de $m \times n$ no nula:

>[!def]
>Si el renglón $A_{i}$ es no nulo, definimos la entrada pivote del renglón $A_{i}$ como la primera entrada no nula contando de izquierda a derecha.

>[!def]
>Si el renglón $A_{i}$ es no nulo y la entrada pivote de $A_{i}$ se encuentra en la columna $k$, llamamos a la columna $k$, la columna pivote del renglón $A_{i}$.



> Ejemplo:

$$
A = \begin{pmatrix}
0 & 0 & -1 & 2 & 3 & 0 \\
1 & 0 & 2 & 0 & 0 & -1 \\
0 & 0 & 0 & 0 & 0 & 1 \\
0 & 0 & 0 & 0 & 0 & 0
\end{pmatrix}
$$

- Para el primer renglón, la entrada pivote está en la tercera columna.
- Para el segundo renglón, la entrada pivote está en la primera columna. 
- Para el tercer renglón, la entrada pivote está en la sexta columna.

---

# Forma Escalonada Reducida por filas (FER)
[[Ayudantía 08#Matriz escalonada reducida]]

Sea $R$ una matriz de $m \times n$. Diremos que $R$ está en la forma escalonada reducida por filas (FER) si $R = (0)$, o bien, $R \neq (0)$ y satisface:
- Todos los renglones nulos de $R$ están abajo de los renglones no nulos de $R$. Esto es, si $R$ tiene $r$ renglones no nulos, entonces $R_{r+1}, \dots, R_{m}$ son nulos. 
- Si $R_{i}$ es un renglón no nulo con $i > 1$ y la entrada pivote de $R_{i}$ está en la columna $k_{i}$ y la entrada pivote del renglón $R_{i-1}$, está en la columna $k_{i-1}$, entonces $k_{i-1} < k_{i}$. 
- Si $R_{i}$ es un renglón no nulo y $a_{ik_{1}}$ es su entrada pivote, entonces $a_{ik_{i}} = 1$ 
- Si $R_{i}$ es un renglón no nulo y $a_{ik_{i}}$ es su entrada pivote, entonces las entradas de la columna $k_{i}$ son todas cero excepto $a_{ik_{i}}=1$.

 > Ejemplo:
 > $$\begin{pmatrix}1 & 2 & 0\\0 & 0 & 1 \\ 0 & 0 & 0 \end{pmatrix}$$
 > En las columnas pivote, el resto es cero, cuando no se trata de un pivote, el número puede ser distinto de $1$.
 
 ---
# Equivalencia de matrices por filas


Sean $A$ y $B$ matrices de $m \times n$. Diremos que $A$ es equivalente por filas a $B$ si existen un número finito de [[Clase 10#Operaciones elementales por filas|operaciones elementales por filas]] $e_{i}, \dots , e_{k}$ tales que $B = e_{k}e_{k-1} \dots e_{2}e_{1}A$. 

> Ejemplo:

Muestra que $A$ es equivalente por filas a $I$.

$$
\begin{align}
A= \begin{pmatrix}
-\frac{1}{2} & 2  \\
3 & 3
\end{pmatrix} & &
I= \begin{pmatrix}
1 & 0  \\
0 & 1
\end{pmatrix}
\end{align}
$$

$$
\begin{align}
A= \begin{pmatrix}
-\frac{1}{2} & 2  \\
3 & 3
\end{pmatrix} 
\xrightarrow[e_{1}]{A_{1} \to -2A_{2}} 
\begin{pmatrix}
1 & -4  \\
3 & 3
\end{pmatrix}
\xrightarrow[e_{2}]{A_{2} \to - \frac{1}{3} A_{2}} 
\begin{pmatrix}
1 & -4  \\
-1 & -1
\end{pmatrix} 
\xrightarrow[e_{3}]{A_{2} \to A_{1} + A_{2}} 
\begin{pmatrix}
1 & -4  \\
0 & -5
\end{pmatrix} \\
\xrightarrow[e_{4}]{A_{2} \to - \frac{1}{5} A_{2}} 
\begin{pmatrix}
1 & -4  \\
0 & 1
\end{pmatrix} 
\xrightarrow[e_{5}]{A_{1} \to A_{1} + 4 A_{2}} 
\begin{pmatrix}
1 & 0  \\
0 & 1
\end{pmatrix}
\end{align}
$$

Notemos que cada operación elemental tiene su inversa:
$$
\begin{align}
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} \xrightarrow[e_{5}']{A_{1} \to A_{1} - 4 A_{2}}
\begin{pmatrix}
1 & -4 \\
0 & 1
\end{pmatrix} \dots
\end{align}
$$

Por lo que $A \to B \to A$. Por lo tanto es [[simétrica]], [[reflexiva]] y [[transitiva]]. Es decir, tiene una [[relación de equivalencia]]. 

