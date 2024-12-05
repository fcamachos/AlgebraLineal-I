---
date: 2024-10-24
video: 
tags:
  - contexto/academico
  - tipo/estudio
  - tema/algebra-lineal
pdf:
  - "[[20241023 Clase 23 y 25 octubre.pdf]]"
---

pdf:
  - "[[20241023 Clase 23 y 25 octubre.pdf]]"


> 1


Sea $V$ un $F-e.v.$ y $X \subseteq V$ un conjunto finito de vectores linealmente independientes, entonces cualquier subconjunto de este conjunto es l.i. 

`\begin{proof}`
Sean $v_1 , \dots, v_{k} \in X$

PD 
$\{ v_1 , \dots, v_{k}  \} \subseteq X$ es l.i.

sup que $0_{V} = \alpha_{1} v_{1} + \dots + \alpha_{k} v_{k}$

Llamemos $v_{k+1} , \dots, v_m$ 
...


Como $X = \{  v_1 , \dots, v_{k}, v_{k+1} , \dots, v_n \}$ es l.i.
Entonces $\alpha_{1} = \dots = \alpha _{k} = 0$
Por lo tanto $\{  v_1 , \dots, v_k \}$ es l.i.

`\end{proof}`

---

> 2

Matriz, con $m > n$ tiene solución no trivial. 

`\begin{proof}`
Sea R la forma de Hermit de A. Como A y R son equivalentes por filas, los sistemas Ax = 0 y Rx = 0 son equivalentes. Esto es, tienen el mismo conjunto de soluciones.

Probaremos que el sistema $Rx = 0$ tiene solución no trivial. 

Sea $r$ el rango por filas de $R$ que es igual al número de renglones no nulos de $R$.

El número de renglones de $R=m$
El número de columnas de $R= n$
Por HI $m>n$
$r \leq m < n \implies r < n \implies n-r > 0$
Por lo que el sistema $Rx = 0$ tiene solución no trivial. 
`\end{proof}`

---

> 3

>[!def]
Sea $V$ un $F-e.v.$  finítamente generado y $\{  v_1 , \dots, v_m \}$ un conjunto de generadores de $V$.
Entonces cualquier subconjunto linealmente independiente de $V$ tiene a lo más $m$ vectores. 

`\begin{proof}`

Probaremos que cualquier subconjunto de $V$ con más de $m$ vectores es linealmente dependiente. 

Sea $\{ w_1 , \dots, w_n \}$ un subconjunto de $V$ y supongamos que $n >m$.

> PD
> $\{  w_1 , \dots, w_n \}$ es l.d.

Como los vectores generan a $V$, entonces para cada $1 \leq j \leq n$, el vector $w_{j}$  
...

existen escalares $a_{1j}, \dots, a_{mj} \in F$ tales que $w_{j}= a_{1j}v_{1} + a_{2j}v_{2} + \dots + a_{mj}v_{m} = \sum_{i=1}^{m} a_{ij}v_{j}$

Consideremos la matriz:
$$
A = \begin{pmatrix}
a_{ij}
\end{pmatrix} = 
\begin{pmatrix}
a_{11}  & \dots &  a_{1n} \\
 & \vdots \\
a_{m1}  & \dots  & a_{mn}
\end{pmatrix}
$$
La columna 1 es $w_{1}$, la última columna es $w_{n}$.

Ahora bien, el sistema homogéneo $Ax= 0$ tiene solución no trivial, ya que $n > m$.

Sea $s = ( s_1 , \dots, s_{n} ) \in F^{n}$ una solución no trivial de $Ax=0$

$$
\begin{pmatrix}
a_{11}  & \dots &  a_{1n} \\
 & \vdots \\
a_{m1}  & \dots  & a_{mn}
\end{pmatrix}
\begin{pmatrix}
s_{1}\\
\vdots \\
s_{n} 
\end{pmatrix} =
\begin{pmatrix}
\sum_{j=1}^{n} a_{ij}s_{j} \\
\vdots \\
\sum_{j=1}^{n} a_{mj}s_{j} 
\end{pmatrix} = 0
$$

Entonces 
$s_{1}w_{1} + \dots + s_{n} w_{n} = \sum_{i=1}^{m} \sum_{j=1}^{n} (a_{ij}s_{j})v_{i} = 0_{V}$

Esta es una combinación lineal no trivial  de los vectores $w_1 , \dots, w_n$ ya que al menos uno de los escalares ${} s_1 , \dots, s_n$ es no nulo.
De aqui que $\{ w_1 , \dots, w_n \}$ es l.d.

`\end{proof}`

---

> 4

Sea $V$ un $F-e.v.$  finitamente generado, entonces, cualesquiera dos bases de $V$ tienen el mismo número de elementos.

`\begin{proof}`
Supongamos que $B = \{  v_1 , \dots, v_m \}$ y $C = \{  w_1 , \dots, w_n \}$ son bases de $V$.

>PD
>$n = m$

Tenemos que:
a) $\{ v_1 , \dots, v_m \}$ genera a $V$ y $\{ w_1 , \dots, w_n \}$ es l.i. por (3) $n \leq m$
b) $\{ w_1 , \dots, w_n \}$ genera a $V$ y ${} \{ v_1 , \dots, v_n \}$ es l.i. por (3) $m \leq n$

Por lo tanto $m = n$.
`\end{proof}`

---

> 5

>[!def] Dimensión de V sobre F
>Sea $V$ un espacio finitamente generado.
>Definimos la dimensión de $V$ sobre $F$ como el número de vectores de cualquier base de $V$. Y lo denotamos como 
>$$dim_{F}V$$

---

> 6

Ejemplos:

a) $dim_{F}F ^{n} = n$

ya que la base canónica de $F ^{n}$ tiene $n$ elementos.

b) $dim_{F}M_{m \times n}(F) = mn$ 

Un caso particular sería
$dim_{F}M_{3 \times 2}(F)$
$$
\begin{align*}
\begin{pmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22}  \\
a_{31} & a_{32}
\end{pmatrix} &= 
a_{11} 
\begin{pmatrix}
1 & 0 \\
0 & 0 \\
0 & 0
\end{pmatrix} +
a_{12} 
\begin{pmatrix}
0 & 1 \\
0 & 0 \\
0 & 0
\end{pmatrix} +
a_{21} 
\begin{pmatrix}
0 & 0 \\
1 & 0 \\
0 & 0
\end{pmatrix}\\
& +a_{22} 
\begin{pmatrix}
0 & 0 \\
0 & 1 \\
0 & 0
\end{pmatrix} +
a_{31} 
\begin{pmatrix}
0 & 0 \\
0 & 0 \\
1 & 0
\end{pmatrix} +
a_{32} 
\begin{pmatrix}
0 & 0 \\
0 & 0 \\
0 & 1
\end{pmatrix}
\end{align*}
$$


Las matrices canónicas de $3 \times 2$ generan una dimensión de 6 vectores.

De manera general:
$$
\begin{pmatrix}
a_{11}  & \dots &  a_{1n} \\
 & \vdots \\
a_{m1}  & \dots  & a_{mn}
\end{pmatrix} = a_{11} E^{11} + \dots + a_{mn} E^{mn}
$$

---

