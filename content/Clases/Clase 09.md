---
date: 2024-08-26
video:
  - https://www.youtube.com/watch?v=vrw8YdSh6YA
tags:
  - contexto/academico
  - tema/algebra-lineal
---
# Propiedades del producto de matrices


## Distributividad
>[!prp] Distributividad
Si los productos $AB,BC$ están definidos, entonces:
$$A(BC) = (AB) C$$

## Identidad 
>[!prp] Matriz Identidad
Si $A$ de $m \times n$, e $I_{m}$ es la matriz identidad de $m \times m$, e $I_{n}$ es la matriz identidad de $n \times n$. Entonces $I_{m} A = A$ y $A I_{n} = A$

^613b9b

## Leyes distributivas  
>[!prp] Leyes distributivas
Sean $A,B,C y D$ matrices del tamaño adecuado, entonces: 
$$A(B+C) = AB + AC$$
Y
$$(B+C)D = BD + BC$$

---

`\begin{proof}`@[[#^613b9b]]

a)
Tenemos 
$$
A = \begin{pmatrix}
a_{11}  & a_{12}  & \dots & a_{1j} & a_{1n} \\
a_{21} & a_{22}  & \dots & a_{2j}  & a_{2n} \\
\vdots \\
a_{m_{1}}  & a_{m_{2}}  & \dots & a_{mj}  & a_{mn}
\end{pmatrix}
$$
> notar la $j-$ésima columna de $A$


$$
I = \begin{pmatrix}
e_{11}  & e_{12} & \dots  & e_{1m} \\
\vdots \\
e_{i1}  & e_{i2} & \dots  & e_{im} \\
e_{m1}  & e_{m2} & \dots  & e_{mm}
\end{pmatrix}
$$

> Notar el $i-$ésimo renglón de $I_m$


P.D. 
$I_{m}A = A$, es decir, para cada $1 \leq i \leq m, 1 \leq j \leq n$:
$(I_{m}A)(ij)=A(i,j)=a_{ij}$

Notemos que la multiplicación $I_{m \times m}A_{m \times n}$ da como resultado una matriz de $m \times n$, por lo que *"vamos por buen camino"*.

Recordemos que para calcular la entrada $(i,j)$ de 
$(I_{m}A)(i,j)= (I_{m})_{i} A^{j}$     (Ver [[Clase 07#Otra forma de recordarlo]])


Por lo que
$$
= \sum_{j=1}^{m} e_{ik}a_{kj} 
$$


Como $I_{m}$ es la matriz identidad de $m \times m$, tenemos que para $1 \leq i \leq m$ y $1 \leq j \leq n$:
$$
e_{ij} = \begin{cases}
1 & i = j \\
0  & i\neq j
\end{cases}
$$
Por lo que:
$$
= \sum_{j=1}^{m} e_{ik}a_{kj} = e_{ii}a_{ij} = 1 a_{ij} = a_{ij}
$$
Pues $e_{ik} = 0$ si $k \neq i$.
`\end{proof}`

Para la demostración de b) es un proceso silimar 

---

>[!rmk] El producto de matrices no es, en general, conmutativo:
>Ejemplo 1:
>$A_{3 \times 2} B_{2 \times 5} \neq B_{2 \times 5} A_{3 \times 2}$
>Pues el tamaño de $BA$ no está definido. 
>Ejemplo 2:
>$$\begin{pmatrix} 2 & 2\\2 & 2 \end{pmatrix} \begin{pmatrix} 3 & 3\\3 & 3 \end{pmatrix} \neq \begin{pmatrix} 3 & 3\\3 & 3 \end{pmatrix} \begin{pmatrix} 2 & 2\\2 & 2 \end{pmatrix}$$
>El único caso donde es conmutativo, es con las matrices de 1 elemento. 


# Matrices Invertibles e Inversos

Sea $A$ una matriz de $n \times n$:

>[!def] Inverso Izquierdo
> $B$ una matriz de $n \times n$ es inverso izquierdo de $A$ si:
> $$BA = I_{n}$$

>[!def] Inverso Derecho
> $C$, una matriz de $n \times n$ es inverso derecho de $A$ si:
> $$AC = I_{n}$$

> [!def] Matriz invertible
> Diremos que una matriz $A$ es invertible si existe una matriz $D$ de $n \times n$ tal que:
> $$DA = I_{n} =AD$$

## Equivalencia de matrices

> [!def] Equivalencia de matrices
Sean $A,B \text{ y } C$ matrices de $n \times n$. 
Si $B$ es inversa izquierda de $A$ y $C$ es inversa derecha de $A$, entonces, $B = C$.

^7c9456

`\begin{proof}`@[[#^7c9456]]

Tenemos que:

$$
\begin{align}
BA &= I_{n} \\
AC &= I_{n} \\
\implies B &= BI_{n} = B(AC) \\
_{\text{Por asociatividad}} \\
&= (BA) C \\
&= I_{n} C = C
\end{align}
$$
`\end{proof}`

## Existencia de una única matriz inversa

>[!def] Unicidad de la matriz inversa
Sea $A$ una matriz de $n \times n$ invertible. Entonces A tiene una única matriz inversa. Es decir, existe una única matriz $D$ de $n \times n$ tal que $AD = I_{n} = DA$.

^d81280

`\begin{proof}`@[[#^d81280]] 

Supongamos que $D$ y $D'$ son inversas de $A$. Entonces:
$$
\begin{align}
AD = I_{n} = DA \\
AD' = I_{n} = D'A
\end{align}
$$

P.D. 
$$
D = D'
$$
Tenemos:
$$
\begin{align}
D' = D'I_{n} &= D'(AD) \\
_{\text{Por asociatividad}} \\
&= (D'A)D = I_{n}D = D
\end{align}
$$

`\end{proof}`


## Notación

Si $A$ es una matriz de $n \times n$ invertible, denotamos a la matriz inversa de $A$ como:
$$
A^{-1}
$$

> [!prp] La inversa de una inversa
Si $A$ es una matriz invertible de $n \times n$, entonces $A^{-1}$ también lo es. Y $(A^{-1})^{-1}=A$

^bff137

`\begin{proof}`@[[#^bff137]]

Para que $A$ sea la inversa de $A^{-1}$, hay que ver que $AA^{-1}=I_{n} = A^{-1}A$, lo cual es cierto pues $A^{--1}$ es la inversa de $A$.

`\end{proof}`