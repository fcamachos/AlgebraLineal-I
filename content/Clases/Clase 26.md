---
date: 2024-10-21
video:
  - https://www.youtube.com/watch?v=Ow6w0QeFk5w
tags:
  - contexto/academico
  - tema/algebra-lineal
---

1 teo
Sea $V$ un $F-e.v.$ finítamente generado y sean $v_{1} , \dots, v_{n}$ vectores en $V$. 
Son equivalentes:
i) $\{ v_{1} , \dots, v_{n} \}$ es un conjunto mínimo de generadores. 
ii) $\{ v_{1} , \dots, v_{n} \}$ es un conjunto máximo linealmente independiente.
iii) $\{ v_{1} , \dots, v_{n} \}$ es un conjunto base de $V$.

`\begin{proof}`
$i \implies iii$

Como $\{ v_{1} , \dots, v_{n} \}$ genera por hipótesis, basta probar que $\{ v_{1} , \dots, v_{n} \}$  es linealmente independiente. 

Supongamos que $0_{v} = \alpha_{1} v_{1} + \dots + \alpha_{n} v_{n} = \sum_{i=1}^{n} \alpha _{i}v_{i}$

PD  $\alpha_{i} = 0 \forall i = 1, \dots ,n$

Sup que para algún $j, 1 \leq i \leq n \quad \alpha_{j} \neq 0$
Renumerando podemos suponer sin pérdida de generalidad que $\alpha_{1} = 0$

Tenemos 
 $0_{v} = \alpha_{1} v_{1} + \dots + \alpha_{n} v_{n}$ 
 multiplicamos por $\alpha_{1}^{-1}$ la igualdad
$$
\begin{align*}
0_{V} &= \alpha_{1}^{-1}0_{v} = \alpha_{1}^{-1} (\alpha_{1} v_{1} + \dots + \alpha_{n} v_{n})\\
&= v_{1} + \alpha_{1}^{-1}\alpha_{2} v_{2} + \dots + \alpha_{1}^{-1}\alpha_{n} v_{n}
\end{align*}
$$
Sumamos $-v_{1}$ a la igualdad:
$$
\begin{align*}
-v_{1} &= 0_{V} + (-v_{1}) &= \alpha_{1}^{-1}\alpha_{2} v_{2} + \dots + \alpha_{1}^{-1}\alpha_{n} v_{n}\\
v_{1} &= - \alpha_{1}^{-1}\alpha_{2} v_{2} - \dots - \alpha_{1}^{-1}\alpha_{n} v_{n}
\end{align*}
$$
Por lo tanto $v_{1}$ es generado por los demás.
Probemos que $\{ v_{2},\dots,v_{n} \}$ genera a $V$.

Sea $w\in V$, como $\{ v_{1} , \dots, v_{n} \}$ genera a $V$, existen $\beta_{1} , \dots, \beta_{n} \in F$ tales que 
$$
\begin{align*}
w &= \beta_{1}v_{1} + \beta_{2}v_{2}  \dots + \beta_{n}v_{n}\\
w &= \beta (- \alpha_{1}^{-1}\alpha_{2} v_{2} - \dots - \alpha_{1}^{-1}\alpha_{n} v_{n}) + \beta_{2}v_{2}  \dots + \beta_{n}v_{n} \\
&= (-\beta_{1} \alpha_{1}^{-1}\alpha_{2}v_{2} + \beta_{2})v_{2} + \dots + (-\beta_{1} \alpha_{1}^{-1}\alpha_{n}v_{n} + \beta_{n})v_{n}
\end{align*}
$$
Como ya no está $v_{1}$, significa que el conjunto se puede generar con $\{ v_{2},\dots,v_{n} \}$ , lo cual es una contradicción, porque estamos suponiendo que $\{ v_{1} , \dots, v_{n} \}$ es un conjunto mínimo de generadores. 

Por lo tanto $\{ v_{1} , \dots, v_{n} \}$ es un conjunto linealmente independiente.  `\end{proof}`


`\begin{proof}`
$iii \implies ii$

Sup que $\{ v_{1} , \dots, v_{n} \}$ es base de $V$.

PD $\{ v_{1} , \dots, v_{n} \}$ es máximo linealmente independiente

Como $\{ v_{1} , \dots, v_{n} \}$ es base, basta probar que para cada $w \in V, w \neq v_{i} \quad 1 \leq i \leq n$ se cumple que $\{ v_{1} , \dots, v_{n}, w \}$ es linealmente dependiente.

Como $\{ v_{1} , \dots, v_{n} \}$ genera a $V$ (por ser base), entonces existen $\beta_{1} , \dots, \beta_{n} \in F$ tales que 
$w = \beta_{1} v_{1} + \dots + \beta_{n} v_{n}$
Por lo tanto se puede escribir el vector cero como:
$0_{v} = -1 w + \beta_{1} v_{1} + \dots + \beta_{n} v_{n}$
Y como uno de los escalares es distinto de cero (-1), entonces es linealmente dependiente. `\end{proof}`

`\begin{proof}`
$ii \implies i$

Sup que $\{ v_{1} , \dots, v_{n} \}$ es un conjunto máximo linealmente independiente.

PD $\{ v_{1} , \dots, v_{n} \}$ es mínimo de generadores. 

Primero probemos que $\{ v_{1} , \dots, v_{n} \}$ genera a  $V$.

Sea $w \in V$. 
Si $w = v_{i}$ para $1 \leq i \leq n$, entonces 
$v_{i} = 0v_{1} + \dots + 0 v_{i-1} + 1 v_{i}+0v_{i+1} + \dots + 0v_{n}$

Si $w \neq v_{i}$ para $1 \leq i \leq n$, entonces ${} \{ v_{1} , \dots, v_{n}, w \} {}$ es linealmente dependiente ya que  $\{ v_{1} , \dots, v_{n} \}$  es máximo linealmente independiente (por hipótesis).

Como  $\{ v_{1} , \dots, v_{n},w \}$  es linealmente dependiente, existen $\alpha_{1} , \dots, \alpha_{n}, \beta \in F$ no todos iguales a cero y tales que:
$0_{V} = \alpha_{1}v_{1}+\dots + \alpha_{n} v_{n} + \beta w$
Probemos que forzosamente $\beta = 0$
Si $\beta = 0$, entonces alguno de $\alpha_{1} , \dots, \alpha_{n}$ es distinto de cero. 
Renumerando si es necesario, podemos suponer [[SPG]] que $\alpha_{1} \neq 0$

Tenemos
$$
\begin{align*}
0_{V} &=  \alpha_{1} v_{1} + \dots + \alpha_{n} v_{n} + 0 w\\
&= \alpha_{1} v_{1} + \dots + \alpha_{n} v_{n} & \text{y } \alpha_{1}\neq 0\\
\implies \{ v_{1} , \dots, v_{n}  \} \text{ es linealmente dependiente }  \bot!
\end{align*}
$$

Por lo tanto $\beta \neq 0$. Esto implica que $\beta w = -\alpha_{1} v_{1} - \dots - \alpha_{n}v_{n}$ 
$\implies w = \beta^{-1} \beta w = -\beta^{-1}\alpha_{1}v_{1} - \dots \beta^{-1}\alpha_{n}v_{n}$
$\therefore \{ v_{1} , \dots, v_{n} \}$ genera a $V$.

Falta probar que $\{ v_{1} , \dots, v_{n} \}$ es mínimo de generadores. Es decir que para cada $1 \leq i \leq n$ $\{ v_{1} , \dots, v_{n} \} \setminus \{  v_{i} \}$ ya no genera a $V$.

[[SPG]] podemos suponer $i = 1$.

Supongamos que $\{ v_{1} , \dots, v_{n} \} \setminus \{  v_{i} \}$  sí genera a $V$.
En particular $v_{1}$ es combinación lineal de $\{ v_{2} , \dots, v_{n} \}$
$\implies v_{1} = \alpha_{2} v_{2} + \dots + \alpha_{n} v_{n},\alpha_{i} \in F$
$\implies 0_{V} = (-1)v_{1} + \alpha_{2}v_{2}+\dots+\alpha_{n}v_{n}$
$\implies \{ v_{1}, v_{2} , \dots, v_{n} \} \setminus \{  v_{i} \}$ es linealmente dependiente, lo cual es una contradicción con nuestra hipótesis $\bot!$

Por lo tanto, el conjunto $\{ v_{1} , \dots, v_{n} \}$  es mínimo.  `\end{proof}`


