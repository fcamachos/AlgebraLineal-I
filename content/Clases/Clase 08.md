---
date: 2024-08-23
video:
  - https://www.youtube.com/watch?v=rcEvdtgcgx0
tags:
  - contexto/academico
  - tema/algebra-lineal
---

video:
  - ![](https://www.youtube.com/watch?v=rcEvdtgcgx0)


Recordemos la definición de producto de matrices:
[[Clase 07#^ad1ebf]] 

Y la notación para las filas y columnas de $A$: [[Clase 07#Otra forma de recordarlo]]


# Propiedades del producto de matrices


## Asociativo

El producto de matrices (cuando está definido) es asociativo.

Sean $A_{m \times n}\quad B_{n \times q} \quad C_{q \times r}$
$$
\begin{align}
AB_{m \times q} &\qquad BC n \times r \\
((AB)C)_{m \times r} &\qquad A(BC)_{m \times r}
\end{align}
$$
Podemos notar que ambas matrices tienen el mismo tamaño $(m \times r)$. 
$$
\begin{align}
A= (a_{ik}) \qquad B= (b_{kl}) \qquad C= (c_{lj})\\
i = 1,\dots,m \qquad l = 1,\dots ,q \\
k = 1, \dots, n \qquad j =1, \dots, r
\end{align}
$$

P.D. Para cada $1 \leq i \leq m$ y $1 \leq j \leq r$
$$
((AB)C)(i,j) = (A(BC))(i,j)
$$

Entonces:
$$
\begin{align}
((AB)C)(i,j) = (AB)_{i}C^{j}  \\
AB= \begin{pmatrix}
A_{1}B^{1} & \dots & A_{1}B^{q} \\
\vdots \\
A_{i}B^{1} & \dots & A_{i}B^{q} \\
\vdots \\
A_{m}B^{1} & \dots & A_{m}B^{q}
\end{pmatrix}
\end{align}
$$

Para cada $l= 1, \dots , q$: $A_{i}B^{l}=(a_{il} \dots a_{i n}) \begin{pmatrix} b_{1l}\\b_{2l} \\ \vdots \\ b_{nl} \end{pmatrix} = \sum_{k=1}^{n}a_{ik}b_{kl}$

Ahora, multiplicando por C en la $j-$ésima columna:
$$
\begin{align}
(AB)_{i}C^{j} =   \\
\begin{pmatrix}
\sum_{k=1}^{n}a_{ik}b_{k 1}  & \sum_{k=1}^{n}a_{ik}b_{k 2}  & \dots  & \sum_{k=1}^{n}a_{ik}b_{k q}\\
\end{pmatrix}
\begin{pmatrix}
c_{1j} \\ c_{2j} \\ \vdots \\ c_{qj}
\end{pmatrix} =  \\
c_{1j} \sum_{k=1}^{n}a_{ik}b_{k 1} + c_{2j} \sum_{k=1}^{n}a_{ik}b_{k 2}  + \dots  + c_{qj} \sum_{k=1}^{n}a_{ik}b_{k q} =  \\
\sum_{l=1}^{q} \sum_{k=1}^{n} c_{lj} (a_{ik}b_{kl})
\end{align}
$$

Por otro lado tenemos:
$$
\begin{align}
(A(BC))(i,j) = A_{i}(BC)^{j} \\
 \\
\sum_{k=1}^{n} \sum_{l=1}^{q} (c_{lj}a_{ik}) b_{kl}
\end{align}
$$

Por asociatividad de la multiplicación en el campo tenemos que:
$$
\sum_{l=1}^{q} \sum_{k=1}^{n} c_{lj} (a_{ik}b_{kl}) = \sum_{k=1}^{n} \sum_{l=1}^{q} (c_{lj}a_{ik}) b_{kl}
$$

Esta resulta ser una de las demostraciones más compliadas en las matrices por el manejo de distintos índices.

---

## Identidad

$I_{m \times m}A_{m \times n} = A$
$A_{m \times m}I_{n \times n} = A$


## Ley distributiva



$A(B+C) = AB + AC$

