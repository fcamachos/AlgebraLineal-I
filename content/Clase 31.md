---
fecha: 2024-11-05
video: 
tags:
  - contexto/academico
  - tema/algebra-lineal
  - tipo/estudio
pdf: "[[20241105 Clase 4 de noviembre parte 2.pdf]]"
---

pdf: "[[20241105 Clase 4 de noviembre parte 2.pdf]]"

1

Sea $V$ un $F-e.v.$  de dimensión finita $n$ y $S,T$ subespacios de $V$.

Teorema de las dimensiones:
$dim(S+T) = dim(S) + dim(T) - dim(S \cap T)$

`\begin{proof}`
Si $S \cap T = \{ 0_{V} \}$ entonces $dim_{F}(S \cap T) = 0$
en ese caso la suma de s y t es directa y pro lo anterior la dimensión de s + t es la dim de s más la dim de t


Supongamos ahora que la intersección no es el vector trivial. Tomemos una base de esa intersección de k elementos. Por lo que la dimensión de la intersección s y t es k.

Tenemos que $S \cap T$ es subespacio de $S$ y también es subespacio de $V$. 

$\{ v_{1} , \dots, v_{k} \} \subseteq S$ que es linealmente independiente. extendemos $\{ v_{1} , \dots, v_{k} \}$ a una base de $S$:
$\{ v_{1} , \dots, v_{k}, w_{1},\dots,w_{t} \}$

Hacemos lo mismo con $T$, es decir, tenemos que $\{ v_{1} , \dots, v_{k} \} \subseteq T$ y es linealmente independiente.
Lo extendemos a una base de $T$, $\{ v_{1} , \dots, v_{k}, z_{1},\dots,z_{r} \}$

Entonces tenemos que la dimensión de S es k+t, mientras que la dimensión de T es k + r. 
La dimensión de la intersección es k...

Vamos a probar que el conjunto de vectores $\{ v_{1} , \dots, v_{k}, w_{1},\dots,w_{t},z_{1},\dots,z_{r} \}$ es base de $S + T$

Tenemos que probar lo siguiente:
i) $v_{1} , \dots, v_{k}, w_{1},\dots,w_{t},z_{1},\dots,z_{r}$ pertenecen a $S+T$
ii) $\{ v_{1} , \dots, v_{k}, w_{1},\dots,w_{t},z_{1},\dots,z_{r} \}$ genera a $S+T$
iii) $\{  v_{1} , \dots, v_{k}, w_{1},\dots,w_{t},z_{1},\dots,z_{r} \}$ es linealmente independiente. 

con esto podríamos concluir que es base de $S+T$.

i) Para cada $1 \leq i \leq k$, $v_{i} \in S \cap T$ así que podemos escribir a $v_{i}$ como $v_{i} = v_{i} + 0_{V} = 0_{V} + v_{i}$ de modo que puedo ver a $v_{i} \in S + T$.

Ahora para cada $1 \leq j \leq t, w_{j} \in S + T$ ya que $w_{j}\in S$ y podemos escribir a $w_{j}$ como $w_{j} = w_{j} + 0 \in S + T$.

Para cada $1 \leq l \leq r, z_{l} \in S + T$ ya que $z_{l} \in T$ y $z_{l} = 0 + z_{l} \in S+T$

ii)
Ahora probemos que $\{  v_{1} , \dots, v_{k}, w_{1},\dots,w_{t},z_{1},\dots,z_{r} \}$ genera a $S + T$

Sea $x + y \in S + T$, tenemos que $x \in S, y \in T$.

Como $\{ v_{1} , \dots, v_{k}, w_{1},\dots,w_{t} \}$ es base de $S$, entonces $x$ se expresa como $x = \alpha_{1}v_{1} + \dots + \alpha_{k}v_{k} + \beta_{1}w_{1} + \dots + \beta_{t}w_{t}$ donde las alfas y betas son escalares. 

Como $\{ v_{1} , \dots, v_{k},z_{1},\dots,z_{r} \}$ es base de $T$, y $y \in T$, $y$ se expresa como:
$y = \epsilon_{1} v_{1} + \dots + \epsilon_{k} v_{k} + \gamma_{1}z_{1} + \dots + \gamma_{r}z_{r}$ donde epsilones y gammas son escalares. 
Entonces 
$x+y = \alpha_{1}v_{1} + \dots + \alpha_{k}v_{k} + \beta_{1}w_{1} + \dots + \beta_{t}w_{t} + \epsilon_{1} v_{1} + \dots + \epsilon_{k} v_{k} + \delta_{1}z_{1} + \dots + \delta_{r}z_{r}$
...


iii)
Ahora probamos que $\{ v_{1} , \dots, v_{k}, w_{1} , \dots, w_{t}, z_{1} , \dots, z_{r} \}$ es linealmente independiente.

Supongamos que $0_{V}= \alpha_{1}v_{1} + \dots + \beta_{1}w_{1} +\dots+ \gamma_{1}z_{1}+ \dots$
Sumando inversos aditivos tenemos que:
$\underset{ \in T }{ \gamma_{1}z_{1} + \dots } = \underset{ \in S }{ -\alpha_{1}v_{1}-\dots -\beta_{1}w_{1}-\dots }$

Esto implica  que $\gamma_{1}z_{1} + \dots$ está en $S \cap T$.
Como $\{  v_{1} , \dots, v_{k} \}$ es base de $S \cap T$, entonces el vector $\gamma_{1}z_{1} + \dots + \gamma_{r}z_{r} = \delta_{1}v_{1} + \dots + \delta_{k}v_{k}$
$\implies 0_{V} = \delta_{1}v_{1}+\dots+\delta_{k}v_{k} - \gamma_{1}z_{1}-\dots-\gamma_{r}z_{r}$.

Esto es una combinación lineal igual al vector cero de los vectores $v_{1},\dots,v_{k},z_{1},\dots,z_{r}$
Como ... es base de $T$ es linealmente independiente.
Por lo que $\delta_{1} = \dots = \delta_{k} = 0 = \gamma_{1} = \dots = \gamma_{r}$

...


Por lo tanto,  $\{ v_{1} , \dots, v_{k}, w_{1} , \dots, w_{t}, z_{1} , \dots, z_{r} \}$ es base de $S + T$. En particular:
$dim_{F}(S+T) = k +  t + r$
$dim_{F}(S) + dim(T) - dim(S \cap T) = (k+t) + (k + r) - k = k + t + r$ 

`\end{proof}`




Entrega de tarea 3: 18 de noviembre. **Cuenta como examen.** 


