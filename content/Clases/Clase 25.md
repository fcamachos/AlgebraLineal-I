---
fecha: 2024-10-18
video:
  - https://www.youtube.com/watch?v=YG9zOik0chA
tags:
  - contexto/academico
  - tema/algebra-lineal
media_link: https://www.youtube.com/watch?v=YG9zOik0chA
---

video:
  - ![](https://www.youtube.com/watch?v=YG9zOik0chA)

Vectores canónicos en $F^{n}$ $\bar{e_{1}},\bar{e_{2},\dots, \bar{e_{n}}}$ generan a $F^{n}$ y son linealmente independientes.

Las matrices canónicas $\{ E^{ij} \in M_{m\times n} (F) \quad \Big| \quad 1 \leq i \leq m , 1 \leq j \leq n \}$ generan a $M_{m \times n}(F)$ y son linealmente independientes.

Sea $V$ un $F-e.v.$ diremos que $V$ está finítamente generado si existen $v_1 , \dots, v_{n}\in V$ tal que $\langle v_1 , \dots, v_{n \rangle}= V$. 

---
1 def
Sea $V$ un $F-e.v.$  finitamente generado. Un conjunto finito de vectores $v_1 , \dots, v_{n} \in V$ es base de $V$ si:

i) $v_1 , \dots, v_n$ generan a $V$. Es decir: $\langle v_1 , \dots, v_{n} \rangle = V$
ii) $v_1 , \dots, v_n$  son vectores linealmente independientes.

Cualquier conjunto de vectores que contiene al vector cero es linealmente dependiente.

---
2 def
Sea $V$ un $F-e.v.$  finitamente generado y $\{ v_1 , \dots, v_n \}$ un conjunto de vectores de $V$.

a)
Diremos que el conjunto $\{ v_1 , \dots, v_n \}$ es mínimo generador si $\{ v_{1} , \dots, v_{n} \}$ generan y para cada $1 \leq i \leq m$, $\{  v_1 , \dots, v_{n} \} \setminus \{ v_{i} \}$ ya no genera a $V$.

b)
Diremos que el conjunto $\{ v_{1} , \dots, v_{n} \}$ es máximo linealmente independiente si $\{ v_{1} , \dots, v_{n} \}$ es linealmente independiente y para $w \in V, w \neq v_{i}, \{  v_{1} , \dots, v_{n}, w \}$ es linealmente dependiente. 

Ejemplos:

En $\mathbb{R}^{2}$
$\{ (1,0), (0,1) \}$ es un conjunto mínimo de generadores.

$\{ (1,0), (0,1) \}$ genera a $\mathbb{R}^{2}$ ya que si $(a,b) \in \mathbb{R}^{2}, (a,b) = a(1,0)+b(0,1)$.


$\{ (1,0), (0,1) \} \setminus \{  (1,0) \} = \{ (0,1) \}$ ya no genera a $\mathbb{R}^{2}$. De igual forma:
$\{ (1,0), (0,1) \} \setminus \{  (0,1) \} = \{ (1,0) \}$ ya no genera a $\mathbb{R}^{2}$.
Por lo tanto, es un conjunto máximo linealmente independiente. 


Sea $(a,b) \in \mathbb{R}^{2}$
PD: $\{ (1,0), (0,1), (a,b) \}$ es linealmente dependiente.

Tenemos que 
$$
\begin{align}
(a,b) &= a(1,0) + b(0,1) \\
& \implies (0,0) = -1(a,b) + a(1,0) + b(0,1)
\end{align}
$$
Por lo tanto, es linealmente dependiente.


---
3 def
[23:22]()  
Sea $V$ un $F-e.v.$ finítamente generado y $v_{1} , \dots, v_{n} \in V$
Diremos que $\{ v_{1} , \dots, v_{n} \}$ es base de $V$ si:
i) $\{ v_{1} , \dots, v_{n} \}$ genera a $V$
ii) $\{ v_{1} , \dots, v_{n} \}$ es linealmente independiente.


Los vectores canónicos en $F^{n}$ ${} \bar{e_{1}},\bar{e_{2}},\dots, \bar{e_{n}} {}$ son base de $F^{n}$.

Las matrices canónicas $\{  E^{ij} \in M_{m \times n} (F) \quad \Big| \quad 1 \leq i \leq m, 1 \leq j \leq n \}$ es base de $M_{m \times n}(F)$.

Un conjunto linealmente dependiente puede ser generador, pero tiene una infinidad de soluciones. 

---
4
Teorema
[35:00]()
Sea $V$ un $F-e.v.$ finitamente generado y supongamos que $\{  v_{1} , \dots, v_{n} \}$ es una base de $V$. 

Entonces cada vector $w \in V$ se expresa de manera única como $w = \alpha_{1} v_{1} + \dots + \alpha_{n}v_{n}$.

`\begin{proof}`
[38:48]()


`\end{proof}`


