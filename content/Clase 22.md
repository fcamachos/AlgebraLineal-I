---
date: 2024-10-11
video:
  - https://www.youtube.com/watch?v=7lrRNoJfQ8Y
tags:
  - contexto/academico
  - tema/algebra-lineal
pdf:
  - "[[20241016 16 de octubre parte 1.pdf]]"
  - "[[20241016 16 de octubre parte 2.pdf]]"
---
# Subespacios vectoriales 

Continuación de [[Clase 19?#Subespacios vectoriales]]


[[Clase 19?#^c6fd64]] 



>[!def]
>Sea $V$ un $F-e.v.$ y $S \subseteq V$.
>Son equivalentes si
> 1. $S$ es subespacio de $V$.
> 2. $0_{V} \in S$ y $\forall \alpha,\beta \in F$ y $v,v' \in S, \quad \alpha v + \beta v' \in S$.

^124107

`\begin{proof}`@[[#^124107]] 

> [!todo] $\mathtt{1.} \implies \mathtt{2.}$ 

Como $S \neq \emptyset$, podemos tomar $v \in S$. 
Como $S$ es cerrado bajo producto por escalares: $-1v \in S$ 
Y como $-1v = -v$, entonces $-v \in S$.
Y como es cerrado bajo la suma: $v + (-v) = 0_{v} \in S$.

Ahora, sean $\alpha, \beta \in F$ y $v,v' \in S$
Como $S$ es cerrado bajo producto por escalares: $\alpha v$ y $\beta v' \in S$
Y como $S$ es cerrado bajo la suma: $\alpha v + \beta v' \in S$.

>[!todo] $\mathtt{2.} \implies \mathtt{1.}$

Se debe probar que no es vacío. Pero por Hipótesis, $0_{V} \in S$, por lo tanto, no es vacío.

Se debe probar que es cerrado para la suma, pero por hipótesis se tiene que $\alpha v + \beta v' \in S$. Por lo tanto, es cerrado para la suma.

Se debe probar que si tomo un vector en S y cualquier escalar, el producto está en S, pero nuevamente por hipótesis: $\alpha v + \beta v' \in S$.

`\end{proof}`

---


>[!prp] La intersección de cualquier cantidad de subespacios es un subespacio. 
Sea $v$ un $F-e.v.$ y $S_{1}, \dots, S_{k}$ subespacios de $V$.
Entonces $S_{1} \cap \dots \cap S_{k} = \bigcap\limits_{i = 1}^{k} S_{i}$ es subespacio de $V$.

`\begin{proof}`

Hay que mostrar que el vector 0 está ahí. Así como que sea cerrado en la suma y el producto:

$0_{V} \in \bigcap\limits_{i=1}^{k}$ pues $0_{v} \in S_{i} \quad \forall \quad i = 1,\dots,k$.

Sean $\alpha, \beta \in F$ y $v,v' \in \bigcap\limits_{i=1}^{k} S_{i}$ Entonces $v,v' \in S_{i} \quad \forall \quad i = 1, \dots , k$
Como $S_{i}$ es subespacio, $\alpha v + \beta v' \in S_{i} \quad \forall\quad i = 1, \dots, k \implies \alpha v + \beta v' \in \bigcap\limits_{i=1}^{k} S_{i}$ 
`\end{proof}`

> [!tip] Ejemplos
>> a) El subespacio trivial
>> El conjunto $\{ 0_{v} \}$ es subespacio de $V$.
>> Trivialmente, $0_{V} \in \{ 0_{V} \}$
>> Sean $\alpha, \beta \in F$
>> $\alpha 0_{V} + \beta 0_{V} = 0_{V} + 0_{V} = 0_{V}$
>>  Se llama el subespacio cero o subespacio trivial y también se acostumbra a denotarlo como 0.
>>  $S = 0$
>
>> b) Si $V$ es un $F-e.v.$ entonces $V$ es subespacio de $V$.
>
>> c) Sea $V$ un $F-e.v.$ y $v \in V$
>> $\langle v \rangle = \left\{ \lambda v | \lambda \in F \right\}$
>> $\langle v \rangle$ es subespacio de $v$, llamado el subespacio cíclico generado por $v$.
>> `\begin{proof}` 
>> $0_{V} \in \langle v \rangle$ ya que $0_{v} = 0_{F} v$ 
>> Sean $\alpha, \beta \in F$ y $\lambda v, \mu v \in \langle v \rangle$:
>> $\alpha(\lambda v) + \beta(\mu v) = (\alpha \lambda)v + (\beta \mu)v = (\alpha \lambda + \beta \mu) v \in \langle v \rangle$
>> `\end{proof}`

---


# Combinaciones lineales


>[!def] Combinaciones lineales o $F-$lineales
>Sea $V$ un $F-e.v.$, $v_{1},\dots,v_{n} \in V$ y $\lambda_{1}, \dots , \lambda_{n} \in F$ ( no necesariamente distintos).
>El vector $\lambda _{1} v_{1} + \lambda_{2} v_{2} + \dots + \lambda_{n} v_{n} = \sum_{i=1}^{n} \lambda_{i} v_{i}$
>se llama una combinación lineal de $v_{1},\dots,v_{n}$.


>[!def] 
>Sea $V$ in $F-e.v.$
>Sean $v_{1}, \dots v_{n} \in V$ y $w \in V$
>Diremos que $w$ es combinación lineal de $v_{1},\dots, v_{n}$ si existen escalares $\lambda_{1}, \dots , \lambda_{n} \in F$ tales que:
> $w = \lambda_{1} v_{1} + \dots + \lambda_{n} v_{n}$


>[!faq] ¿Es $w$ combinación lineal de $v_{1}$ y $v_{2}$?
>Sea $V = \mathbb{R}^{3}$
>$$
> \begin{align} 
> (-1,0,0) &= v_{1} \\
> (0,2,1) &= v_{2} \\ \\
> (1,1,1) &= w
> \end{align}
>$$
> 

Para responder esto, planteamos la ecuación vectorial:
$$
\begin{align*}
(1,1,1) &=  \lambda (-1,0,0) + \mu (0,2,1)\\
&= (-\lambda,0,0) + (0,2 \mu, \mu)\\
&= (-\lambda, 2\mu, \mu)
\end{align*}
$$
Nos queda el siguiente sistema de ecuaciones:

$$
\begin{cases}
-\lambda  & = 1 \\
2 \mu  & = 1 \\
\mu & = 1
\end{cases}
$$

Por lo tanto, no tiene solución el sistema, y por tanto $w$ no es combinación lineal de $v_{1}$ y $v_{2}$.

---

>[!def] Subespacio generado
>Sea $V$ un $F-e.v.$ y $v_{1}, \dots, v_{n} \in V$
>Sea $\langle v_{1}, \dots , v_{n} \rangle = \{ \lambda_{1}v_{1} + \dots+ \lambda_{n} v_{n} | \lambda_{1}, \dots, \lambda_{n} \in F \}$
>$\langle v_{1}, \dots , v_{n} \rangle$ es un subespacio de $V$ llamado el subespacio generado por $v_{1},\dots,v_{n}$

>[!hint] Ejemplo 1

Consideremos 
$$
V = \mathcal{M}_{ 2 \times 2} (F) = \left\{ 
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix} \quad \Bigg| \quad  a,b,c,d \in F
\right\} 
$$
Sean las matrices canónicas:
$$
E^{11} = 
\begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix}
\qquad
E^{22} =  
\begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} 
$$
¿Quiénes son las matrices generadas por?
$$
\Bigg\langle 
\begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix},
\begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix}
\Bigg\rangle = ?
$$

El subespacio generado es:
$$
\bigg\langle E^{11}, E^{22} \bigg\rangle  = \{ \lambda E^{11} + \mu E^{22} \quad \Big| \quad \lambda,\mu \in F \}
$$
Es decir, una matriz $A = \begin{pmatrix} a &b \\ c & d \end{pmatrix}$ pertenece a $\Big\langle E ^{11}, E^{22} \Big\rangle \Leftrightarrow$ existen $\lambda, \mu \in F$ tales que 
$$
A = \lambda E^{11} + \mu E ^{22}
$$
$$
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
= \lambda 
\begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} + \mu
\begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} = 
\begin{pmatrix}
\lambda  & 0 \\
0 & \mu
\end{pmatrix}
$$
Es decir, una matriz pertenece a ese subespacio si y sólo si dicha matriz es diagonal. 



>[!hint] Ejemplo 2

Consideremos 
$$
V = \mathcal{M}_{ 2 \times 2} (F) = \left\{ 
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix} \quad \Bigg| \quad  a,b,c,d \in F
\right\} 
$$
Sean las matrices canónicas:
$$
E^{12} = 
\begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix}
\qquad
E^{21} =  
\begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix} 
$$
¿Quiénes son las matrices generadas por?
$$
\Bigg\langle 
\begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix},
\begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix}
\Bigg\rangle = ?
$$
Siguiendo los pasos anteriores nos queda:
$$
\begin{pmatrix}
0  & \lambda \\
\mu & 0
\end{pmatrix}
$$
