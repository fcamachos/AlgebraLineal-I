---
date: 2024-11-04
video: 
tags:
  - contexto/academico
  - tema/algebra-lineal
  - tipo/estudio
pdf:
  - "[[20241104 Clase noviembre 4.pdf]]"
---

pdf:
  - "[[20241104 Clase noviembre 4.pdf]]"


1

Si $V$ un $F-e.v.$  y $S,T$ son subespacios se define la suma de $S+T$ como el conjunto $\{ x+y \quad \Big| \quad x \in S, y \in T \}$

En Clase 30 se probo que $S + T$ es subespacio de $V$.

La suma de los subespacios sigue siendo subespacio de $V$.

$\sum_{i=1}^{k}S_{i}$

Se prueba por inducción sobre $k \geq 2$ que $s_{1} + \dots + s_{n} = \sum_{i=1}^{k}S_{i}$ es subespacio de $V$.

---

2
la suma directa...

---
4

Sea $V$ un $F-e.v.$  y $S$ y $T$ dos subespacios de $V$.
La suma $S+T$ es directa sii cada vector $v \in S + T$ se expresa de manera única como $v= x+y$ donde $x \in S, y \in T$.

`\begin{proof}`
...
`\end{proof}`

---
5

Un espacio de dimensión finita es por definición uno creado por una base finita. 

Sea $V$ un $F-e.v.$  de dimensión finita y $S$ y $T$ subespacios de $V$.

Si la suma $S + T$ es directa, y $B$ es una base de $S$ y $C$ es una base de $T$, entonces, la unión de ${} B \cup C {}$ es base de $S + T$

`\begin{proof}`
Como $V$ es de dimensión finita, $S$ y $T$ también son de dimensión finita, y además, $dim_{F}S \leq dim_{F}V$ y $dim_{F}T \leq dim_{F}V$

Sean $B = \{ v_{1} , \dots, v_{m} \}$ base de $S$ y $C = \{ w_{1} , \dots, w_{k} \}$ base de $T$.

observemos que $B \cap C = \emptyset$ ya que, si $v_{i} = w_{j}$ para algún $1 \leq i \leq m$ y $1 \leq j \leq k$ entonces $v_{i} = w_{j} \in S \cap T = \{ 0_{V} \} \implies B \text{ y } C$. tienen como elemento al vector cero, pero esto no es posible pues $B$ y $C$ son linealmente independiente. 

PD
$B \cup C = \{  v_{1} , \dots, v_{m}, w_{1} , \dots, w_{k} \}$ es base de $S + T$.

Sea $z \in S + T$, entonces $z = x + y \quad \Big| \quad x \in S, y \in T$

Como $B = \{  v_{1} , \dots, v_{m} \}$ es base de $S$, $x$ se expresa como $x = \alpha_{1} v_{1} + \dots + \alpha_{m} v_{m}$.
Como $C = \{ w_{1} , \dots, w_{k} \}$...


entonces $z = x+y = \alpha_{1}v_{1} + \dots + \alpha_{m}v_{m} + \beta_{1}w_{1}+ \dots + \beta_{k}w_{k}$.

$\therefore \{ v_{1} , \dots, v_{m}, w_{1}, \dots, w_{k} \}$ genera a $S + T$

PD
$\{ v_{1} , \dots, v_{m}, w_{1}, \dots, w_{k} \}$ es linealmente independiente. 

supongamos que $0_{V} = \alpha_{1} v_{1} + \alpha_{m}v_{m} + \beta_{1}w_{1}+\dots+\beta_{k}w_{k}$ 
entonces...



`\end{proof}`

---

>[!info] Notación
Si  la suma de los subespacios es directa, escribimos $S \oplus T$.

---
Próximamente:
Sea $V$ un $F-e.v.$  de dimensión finita y $S,T$ subespacios de $V$.

Teorema de las dimensiones:
$dim(S+T) = dim(S) + dim(T) - dim(S \cap T)$

