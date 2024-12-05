---
date: 2024-09-06
video:
  - https://www.youtube.com/watch?v=rkrPyEq3Ikc
tags:
  - contexto/academico
  - tema/algebra-lineal
---

video:
  - ![](https://www.youtube.com/watch?v=rkrPyEq3Ikc)

# Sistemas de ecuaciones

## Vectores
Una ecuación lineal en $n$ variables con coeficientes en un campo $F$ es una expresión formal de la forma:
$$
a_{1}x_{1}+ a_{2}x_{2}+\dots+a_{n}x_{n} = b
$$
donde $a_{1},a_{2},\dots,a_{n}$ y $b \in F$.

Recordemos que $F^{n} = F \times F \times \dots \times F = \left\{ (x_{1}, \dots, x_{n}) | x_{i} \in F, \forall i = 1,\dots,n \right\}$.

A estos elementos de $F^{n}$ los llamaremos [[vectores]].


## Solución de ecuación
Una solución de la ecuación $ax_{1} + \dots + a_{n}x_{n} =b$ es un vector $\bar{s} = (s_{1}, \dots, s_{n}) \in F^{n}$ tal que $a_{1}s_{1} + \dots + a_{n} s_{n} = \sum_{i=1}^{n}a_{i}s_{i} =b$

### Escritura
Un sistema de $m$ ecuaciones en $n$ variables con coeficientes en un campo $F$, lo escribimos como:
$$
\begin{align}
a_{11}x_{1} + \dots + a_{1n}x_{n} &= b_{1} \\
a_{21}x_{1} + \dots + a_{2n}x_{n} &= b_{2} \\
&\vdots \\
a_{i1}x_{1} + \dots + a_{in}x_{n} &= b_{i} \\
&\vdots \\
a_{m1}x_{1} + \dots + a_{mn}x_{n} &= b_{m}
\end{align}
$$

Donde $a_{ij}$ es el coeficiente de $x_{j}$ en la $i-$ésima ecuación.

### Solución del sistema

Una solución del sistema es un vector $\bar{s} = (s_{1},\dots, s_{n}) \in F^{n}$ tal que $\bar{s}$ es solución de cada una de las ecuaciones del sistema. Esto es $\forall i = 1,\dots,m, \qquad \sum_{j=1}^{n} a_{ij}s_{j}=b_{i}$ 

## La matriz de coeficientes y la matriz aumentada

Consideremos el sistema

$$
\begin{align}
a_{11}x_{1} + \dots + a_{1n}x_{n} &= b_{1} \\
a_{21}x_{1} + \dots + a_{2n}x_{n} &= b_{2} \\
&\vdots \\
a_{i1}x_{1} + \dots + a_{in}x_{n} &= b_{i} \\
&\vdots \\
a_{m1}x_{1} + \dots + a_{mn}x_{n} &= b_{m}
\end{align}
$$

### Sistema homogéneo
Diremos que el sistema es homogéneo si $b_{i} = 0 \qquad \forall i = 1, \dots,m$

### Sistema no homogéneo
Diremos que es no homogéneo si existe $j, 1 \leq j \leq m$ tal que $b_{j} \neq 0$.

### Matriz de coeficientes
[[Ayudantía 09#Matriz asociada]]

### Matriz aumentada
[[Ayudantía 09#Matriz aumentada]]

# Resolución de matrices

Sea $A$ una matriz de $m \times n$, entonces existe una única matriz $R$ de $m \times n$ que está en la [[Forma Escalonada Reducida por filas]], que es equivalente a la matriz $A$.
$$
A \xrightarrow[]{e_{1}} e_{1}A \dots \xrightarrow[]{e_{k}} e_{1}\dots e_{k} A = R
$$

## Rango por filas de R
Sea $R$ una matriz de $m \times n$ que está [[Forma Escalonada Reducida por filas|FER]].
Definimos el [[rango por filas de R]] como el número de renglones no nulos de $R$. $I_{n}$

>[!remark] Notación
> Escribimos $rango_{f}(R)$

>[!remark]
> $rango_{f}(R) \leq m$


## Solución trivial

Supongamos que tenemos las ecuaciones:
$$
\begin{cases}
2x_{1} - 4x_{2} - 6x_{3} &= 0 \\
x_{1} - 2 x_{2} + 3 x_{3} &= 0
\end{cases}
$$

Podemos decir que $\left( 0,0,0 \right) \in \mathbb{R}^{3}$ es una posible solución, pues al sustituir las variables por ceros, el resultado en ambas ecuaciones, es cero. 
Esta es llamada la *solución trivial*. ([[Ayudantía 09#Solución trivial]] )

## Pasos para encontrar la solución

#### Paso 1
Encontrar la matriz de coeficientes asociada del sistema ([[Ayudantía 09#Matriz asociada]]).

$$
A = \begin{pmatrix}
2 & -4 & -6 \\
1 & -2 & 3
\end{pmatrix}
$$
#### Paso 2
Aplicamos operaciones elementales por filas hasta obtener la [[Forma Escalonada Reducida por filas]] equivalente por filas a $A$.

$$
\begin{pmatrix}
2 & -4 & -6 \\
1 & -2 & 3
\end{pmatrix}
\xrightarrow[]{A_{1} \to A_{2}}
\begin{pmatrix}
1 & -2 & 3 \\
2 & -4 & -6 
\end{pmatrix}
\xrightarrow[]{A_{2} \to A_{2} - 2A_{1}}
\begin{pmatrix}
1 & -2 & 3 \\
0 & 0 & -12 
\end{pmatrix}
$$
$$
\xrightarrow[]{A_{2} \to - \frac{1}{12} A_{2} }
\begin{pmatrix}
1 & -2 & 3 \\
0 & 0 & 1 
\end{pmatrix}
\xrightarrow[]{A_{1} \to A_{1} -  3A_{2} }
\begin{pmatrix}
1 & -2 & 0 \\
0 & 0 & 1 
\end{pmatrix} = R
$$

#### Paso 3
Traducimos la matriz obtenida a un sistema de ecuaciones
$$
\begin{cases}
x_{1} - 2 x_{2} &= 0 \\
x_{3} &= 0
\end{cases}
$$
Resolvemos:
$$
\begin{align}
x_{1} = 2x_{2}  \\
x_{3} = 0
\end{align}
$$
#### Paso 4
Escribimos el conjunto de soluciones:
$$
\left\{ \left( 2x_{2},x_{2},0 \right) | x_{2} \in \mathbb{R} \right\} 
$$

Una solución particular sería $(2,1,0)$.

# Notación matricial para un sistema de ecuaciones

Consideremos
$$
\begin{align}
a_{11}x_{1} + \dots + a_{1n}x_{n} &= b_{1} \\
&\vdots \\
a_{m1}x_{1} + \dots + a_{mn}x_{n} &= b_{m}
\end{align}
$$

que es representada con la matriz
$$
A = \begin{pmatrix}
a_{11}  & \dots & a_{1n} \\
 & \vdots \\
a_{m 1}  & \dots  & a_{mn}
\end{pmatrix} \quad
b = \begin{pmatrix}b_{1} \\ \vdots \\ b_{n}\end{pmatrix}
$$

Consideremos la matriz
$$
x = \begin{pmatrix}
x_{1} \\ \vdots \\ x_{n}
\end{pmatrix}
$$
Si multiplicamos $Ax$ tenemos:
$$
\begin{pmatrix}
a_{11}  & \dots & a_{1n} \\
 & \vdots \\
a_{m 1}  & \dots  & a_{mn}
\end{pmatrix}
\begin{pmatrix}
x_{1} \\ \vdots \\ x_{n}
\end{pmatrix}
$$
$$
\begin{pmatrix}
a_{11} x_{1} + \dots + a_{1n} x_{n} \\
\vdots \\
a_{m1} x_{1} + \dots + a_{mn} x_{n}
\end{pmatrix}
=
\begin{pmatrix}
b_{1}\\ \vdots \\b_{n}
\end{pmatrix}
$$

Por lo tanto, podemos reescribir el sistema de ecuaciones como:
$$
Ax = b
$$

# Ecuaciones equivalentes

Sean $A, A'$ matrices de $m \times n$ y $b$ y $b'$ matrices de $m \times 1$. 
Diremos que los sistemas de ecuaciones $Ax = b$ y $A'x = b'$ son equivalentes si tienen el mismo conjunto de soluciones.
$$
Ax = 0 \qquad Rx = 0
$$

