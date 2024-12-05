---
date: 2024-10-09
video:
  - https://www.youtube.com/watch?v=DjApJpq8nyY
tags:
  - contexto/academico
  - tema/algebra-lineal
  - tipo/estudio
---
# Unicidad del neutro aditivo

>[!prp] El neutro aditivo es único
>Sea $V$ un espacio vectorial sobre $F$. Entonces, existe un único neutro aditivo en $V$.

`\begin{proof}`

Supongamos que $e$ y $e'$ son neutros aditivos de $V$. 

> [!tip] PD
> $e = e'$

Tenemos que:
$$
\begin{align}
e' &= e + e' & \text{porque e es neutro aditivo} \\
&= e & \text{porque e' es neutro aditivo}
\end{align}
$$
`\end{proof}`



# Unicidad del inverso aditivo

>[!prp] El inverso aditivo es único
> Para  $v \in V$ Existe un único inverso aditivo de $v$.


`\begin{proof}`

Supongamos que $v'$ y $v''$ son inversos aditivos de $v$.

>[!hint] PD
>$v' = v''$

Tenemos que

$$
\begin{align*}
v' &= v' + e \\
&= v' + (v + v'')\\
&= (v' + v) + v''\\
&= e + v''\\
&= v''
\end{align*}
$$
`\end{proof}`


## Notación

Denomamos $0 = 0_{V}$ al neutro aditivo de $V$ y lo llamamos el [[vector cero]].

Para cada $v \in V$, denotamos por $-v$ al inverso aditivo de $v$.



# Leyes de cancelación

Sea $V$ un espacio vectorial sobre $F$.

>[!prp]
Si $\cancel{ v } + w = \cancel{ v } + z$, donde $v,w,z \in V$, entonces $w=z$. 

`\begin{proof}`
Tenemos que $v+w = v+z$.
Sumamos $-v$ a ambos lados de la igualdad:
$$
\begin{align*}
-v + (v+w) &=  -v + (v + z)\\
(-v + v) + w &= (-v + v) + z\\
0_{V} + w &= 0_{V} + z\\
w &= z
\end{align*}
$$
`\end{proof}`


>[!prp]
Si $\lambda v = 0_{V}$, entonces $\lambda = 0$  ó $v = 0_{V}$.

`\begin{proof}`

Tenemos que $\lambda v = 0_{V}$

> [!todo] 1 
> Supongamos que $\lambda \neq 0$

>[!hint] PD
>$v = 0_{V}$

Como $\lambda \neq 0$ multiplicamos por $\lambda^{-1}$ la igualdad:
$$
\begin{align*}
\lambda^{-1} (\lambda v) &= \lambda^{-1} 0_{V}\\
(\lambda^{-1} \lambda) v &= 0_{V} & \text{(*)}\\
1_{F} v &= 0_{V}\\
v &= 0_{V}
\end{align*}
$$

$$
\begin{align*}
\lambda^{-1} 0_{V} &= 0_{V} + \lambda^{-1} 0_{V} & *\\
0_{V} + \lambda^{-1} 0_{V} &= \lambda^{-1} (0_{V}+ 0_{V})\\
0_{V} + \cancel{ \lambda^{-1} 0_{V} } &= \lambda^{-1} 0_{V} + \cancel{ \lambda^{-1} 0_{V} }\\
0_{V} &= \lambda^{-1} 0_{V}
\end{align*}
$$

>[!todo] 2
> Supongamos que $v \neq 0_{V}$

> [!hint] PD
> $\lambda = 0$

Si $\lambda \neq 0$, entonces, por lo anterior, $v = 0_{V} \quad \mathcal{!}$ 
$\therefore \lambda = 0$

`\end{proof}`



---

Sea $V$ un $F-e.v.$ ($F$- espacio vectorial). Entonces:

>[!prp]
$\lambda 0_{V} = 0_{V} \qquad \forall \lambda \in F$

`\begin{proof}`

Tenemos que:
$$
\begin{align*}
\lambda 0_{v} &= 0_{V} + \lambda 0_{v}\\
\lambda 0_{v} &= \lambda (0_{V} + 0_{V})\\
\therefore 0_{V} + \lambda 0_{v} &= \lambda (0_{V} + 0_{V})\\
0_{V} + \cancel{ \lambda 0_{v} } &= \lambda 0_{V} + \cancel{ \lambda 0_{V} }\\
0_{V} &= \lambda 0_{V}
\end{align*}
$$
`\end{proof}`


>[!prp]
$0_{F}v = 0_{V} \qquad \forall v \in V$

`\begin{proof}`

Tenemos que:
$$
\begin{align*}
0_{F}v &= (0_{F}+0_{F}) v\\
0_{F}v &= 0_{V} + 0_{F}v\\
\therefore 0_{V} + 0_{F}v &= (0_{F}+0_{F}) v\\
0_{V} + \cancel{ 0_{F}v } &= 0_{F} v+\cancel{ 0_{F} v } & \text{ley de la cancelación de la suma}\\
0_{V} &= 0_{F}v
\end{align*}
$$
 
`\end{proof}`

>[!prp]
$-v = -1 v$

`\begin{proof}`

Por la unicidad del inverso aditivo de $v$, basta probar que $-1v + v = 0_{V}$

Tenemos:
$$
\begin{align*}
-1v + v &=  -1v + 1v\\
&= (-1+1)v &= 0_{F}v &= 0_{V}
\end{align*}
$$

`\end{proof}`


>[!prp]
$-(-v) = v$

`\begin{proof}`
Sea $w = -v$. Debemos demostrar que $v + w = v + (-v) = 0_{V}$.
Esta igualdad se cumple pues $-v$ es el inverso aditivo de $v$.
`\end{proof}`

