# Matrices

Sean $m,n \in \mathbb{N}$, una [[matriz]] de orden $m \times n$ o tamaño $m \times n$ con entradas en un campo $F$, es un arreglo ordenado de $m$ renglones y $n$ columnas, que representamos en la forma:

$$
A =\begin{pmatrix}
a_{11} a_{12} \dots a_{1j} a_{1j+1} \dots a_{1 n} \\
a_{21} a_{22} \dots a_{2j} a_{2j+1} \dots a_{2 n} \\
\vdotswithin \\ \\
a_{i1} a_{i2} \dots a_{ij} a_{ij+1} \dots a_{i n} \\
\vdotswithin \\ \\
a_{m1} a_{m2} \dots a_{mj} a_{mj+1} \dots a_{m n}
\end{pmatrix}
$$

Notación
$A = (a_{ij})_{m \times n}$

La entrada $(i,j)$ de $A$ también la denotamos por:  $A(i,j)$

---

> [!prp|a)] Matrices cuadradas
> Una matriz $A$ se dice que es cuadrada si el número de renglones de $A$ es igual al número de columnas de $A$.

---

> [!prp|b)] Matriz identidad
> La matriz identidad de $n \times n$ denotada por $I_{n} = I$ es la matriz cuyas entradas son para cada $1 \leq i \leq n$ y  $1 \leq j \leq n$ 
> $I_{n} (i,j) = \begin{cases} 1 & \text{ si } \quad i=j \\ 0 & \text{ si } \quad i\neq j  \end{cases}$

> [!example] 
>$n=1$  : $I_{1} = (1)$
>$n=2$ :  $I_{2} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$
>$n=3$ :  $I_{3} = \begin{pmatrix} 1 & 0 & 0\\ 0 & 1 & 0 \\ 0& 0& 1 \end{pmatrix}$

---

>[!prp|c)] Matriz cero
>La matriz cero de orden $m \times n$, es la matriz que tiene todas sus entradas igualadas a cero. 

>[!example]
>$\begin{pmatrix} 0\end{pmatrix}_{1 \times 1}$
>$\begin{pmatrix} 0 &0 \\ 0&0 \end{pmatrix}_{2 \times 2}$
>$\begin{pmatrix} 0  \\ 0 \end{pmatrix}_{2 \times 1}$
>$\begin{pmatrix} 0 &0 \end{pmatrix}_{1 \times 2}$


---

>[!prp|d)] Diagonal de una matriz
>Si $A$ es una matriz de $n \times n$, la diagonal de la matriz $A$ está constituida por las entradas $A(i,i)$ para $i=1, \dots,n$.

>[!exm]
>$\begin{pmatrix}a&  &  \\  & \ddots &  \\  &  & b\end{pmatrix}_{3 \times 3}$

---

>[!prp|e)] Matriz diagonal
>Diremos que una matriz $A$ de orden $n \times n$ es diagonal si $A(i,j) = 0$ si $i \neq j$. 
>Es decir que todas las entradas de la matriz $A$ que no están en la diagonal, son cero.

>[!exm]
>$\begin{pmatrix}1& 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0\end{pmatrix}_{3 \times 3}$


---

>[!prp] Matrices canónicas de $m \times n$
>Para cada $1 \leq i \leq m$ y $1 \leq j \leq n$ definimos la matriz $E^{ij}$ como la matriz cuya entrada $(k,l)$ está dada por: 
>$E ^{ij}(k,l)= \begin{cases} 1 & \text{si} & (k,l) = (i,j) \\ 0 & \text{si} & (k,l) \neq (i,j)\end{cases}$

>[!exm]
>Las matrices canónicas de orden $2 \times 3$:
>$1 \leq i \leq 2 \qquad 1 \leq j \leq 3$
>$(1,1) \quad (1,2) \quad (1,3)$
>$(2,1) \quad (2,2) \quad (2,3)$ 
>$E ^{11} = \begin{pmatrix}1 & 0 & 0 \\ 0 & 0 & 0 \end{pmatrix}$
>Es decir la matriz $E ^{ij}$ tiene en la entrada $(i,j)$ y cero en todas las demás.
>Por lo tanto:
>$E ^{11} = \begin{pmatrix}1 & 0 & 0 \\ 0 & 0 & 0 \end{pmatrix}$
>$E ^{12} = \begin{pmatrix}0 & 1 & 0 \\ 0 & 0 & 0 \end{pmatrix}$
>$E ^{13} = \begin{pmatrix}0 & 0 & 1 \\ 0 & 0 & 0 \end{pmatrix}$
>$E ^{21} = \begin{pmatrix}0 & 0 & 0 \\ 1 & 0 & 0 \end{pmatrix}$
>$E ^{22} = \begin{pmatrix}0 & 0 & 0 \\ 0 & 1 & 0 \end{pmatrix}$
>$E ^{23} = \begin{pmatrix}0 & 0 & 0 \\ 0 & 0 & 1 \end{pmatrix}$ 


---

>[!prp] Vectores canónicos de $F ^{n}$
> Sea $n \in \mathbb{N}$ , y $F ^{n}= F \times F \times \dots \times F$ , los elementos de $F ^{n}$ son $n-$adas ordenadas de elementos de $F$. 
> Un elemento típico de $F ^{n}$ es $(a_{1},a_{2},\dots,a_{n}), a_{i} \in  F \forall i$ 
> Los vectores canónicos de $F ^{n}$ denotado por $\bar{e_{1}},\bar{e_{2}},\dots, \bar{e_{n}}$ están dados por:
> $\bar{e_{i}}$ tiene su $i-$ésima coordenada igual a 1 y todas las demás, cero:
> $\bar{e_{i}}= (\delta_{ik})^{n}_{k=1}$ donde $\delta_{ik}= \begin{cases} 1 & i=k \\ 0 & i \neq k\end{cases}$


Matrices canónicas de $1 \times 3: (1,1) \qquad (1,2) \qquad (1,3)$
$$
\begin{align}
E^{11}= (1 \quad0 \quad 0) \\
E^{12}= (0 \quad 1 \quad 0)  \\
E^{13}= (0 \quad0 \quad 1) 
\end{align}
$$

