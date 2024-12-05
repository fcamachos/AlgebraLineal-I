---
date: 2024-10-16
video:
  - https://www.youtube.com/watch?v=0OChshsai7c
tags:
  - contexto/academico
  - tema/algebra-lineal
  - tipo/estudio
---
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/0OChshsai7c?si=prDOuo0Om070WpaV" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


# Ejemplo de subespacios


Sea...
$$
\begin{cases}
a_{11} x_{1} + \dots a_{1n}x_{n} = 0 \\
\vdots \\
a_{i1} x_{1} + \dots a_{in}x_{n} = 0 \\
\vdots \\
a_{m1} x_{1} + \dots a_{mn}x_{n} = 0
\end{cases}
$$
... un sistema homogéneo de ecuaciones de $m \times n$.

Una solución del sistema es un vector 
$$
S = (s_{1}, \dots s_{n}) \in F^{n}
$$
tal que para cada $i = 1, \dots, m$:
$$
\begin{align*}
a_{i_{1}}s_{1} + \dots+ a_{i n} s_{n} &=  0\\
&= \sum_{i=1}^{n}  a_{i}s_{i}
\end{align*}
$$

Sea $A$ la matriz de coeficientes del sistema y $W = \{ s \in F ^{n} \quad \Big| \quad s \text{ es solución del sistema } Ax = 0 \}$ 
$W$ es un subconjunto de $F ^{n}$.

$W$ es un subespacio de $F ^{n}$ llamado el espacio solución del sistema $Ax = 0$

Para probar que $W$ es subespacio debemos asegurar que el 0 está incluido, lo cual es cierto, pues existe la solución trivial al ser un sistema homogéneo. Y la suma y el producto por escalar está dentro de la solución del sistema: 

`\begin{proof}[Demostración de la suma]`

$0_{F^{n}} \in W$ pues el vector cero es solución del sistema $Ax= 0$

Sean $s= (s_{1}, \dots s_{n})$ y $t=(t_{1},\dots,t_{n})$ soluciones de $Ax = 0$

>PD
>$s + t$ es solución de $Ax = 0$. Es decir que para cada $i=1,\dots,m$
>$$\sum_{j=1}^{n} a_{ij} (s_{j}+ t_{j}) = 0$$

Como $s$ y $t$ son soluciones, tenemos que para cada $i=1, \dots, m$ 
$\sum_{j=1}^{n}  a_{ij} s_{i} = 0$ y $\sum_{j=1}^{n} a_{ij}t_{j} =0$

Por lo tanto:
$$
\sum_{j=1}^{n}  a_{ij} s_{i} + \sum_{j=1}^{n}  a_{ij} t_{i} = \sum_{j=1}^{n} a_{ij}(s_{j}+ t_{j}) = 0
$$
Es decir, la suma de dos soluciones, es solución.
`\end{proof}`


`\begin{proof}[Demostración del producto por escalar.]`

Sea $\alpha \in F$ y $s = (s_{1}, \dots, s_{n}) \in W$

>PD
>Para cada $i = 1, \dots,m$
>$$\sum_{j=1}^{n} a_{ij} (\alpha s_{j}) = 0 $$

$$
\begin{align*}
\sum_{j=1}^{n} a_{ij} (\alpha s_{j}) &=  \alpha \sum_{j=1}^{n} a_{ij} s_{j} \\
&= \alpha 0 \\
&= 0
\end{align*}
$$

`\end{proof}`

Por lo tanto el conjunto de soluciones de un sistema homogéneo de ecuaciones es subespacio de $F^{n}$.

---

## Matrices diagonales

Consideremos el espacio de matrices $M_{n \times n}(F)$

Sea $D_{n} = \{ A \in M _{ n \times n} (F)  \quad \Big| \quad A \text{ es diagonal} \}$ 
Entonces $D_{n}$ es subespacio de $M_{ n \times n}(F)$.

>[!hint]
La matriz 0 es diagonal. 
Si yo sumo 2 matrices diagonales, tengo una matriz diagonal.
Si multiplico una matriz diagonal por un escalar, obtengo una matriz diagonal. 

## Matrices triangulares

Sea $T^{n} = \{  A \in M_{ n\times n} (F) \quad \Big| \quad A \text{ es triangular superior} \}$
$T^{n}$ es subespacio de $M_{ n \times n} (F)$.

Sea ${} T_{n} = \{  A \in M_{ n\times n} (F) \quad \Big| \quad A \text{ es triangular inferior} \} {}$
$T^{n}$ es subespacio de $M_{ n \times n} (F)$.

>[!hint]
>Se debe mostrar que la matriz 0 es triangular. Y que la suma y el producto por escalar es triangular.

---

## Subespacio generado por los vectores v1 hasta vm

Sea $V$ un $F-e.v.$  y ${} v_{1}, \dots, v_{m} {}$ vectores en $V$.
Sea $\langle  v_1 , \dots, v_{m \rangle}= \{ \sum_{i=1}^{m} \alpha _{i} v_{i} \quad \Big| \quad \alpha_1 , \dots, \alpha_{m} \in F \}$ 
Entonces $\langle  v_1 , \dots, v_{m \rangle}$ es subespacio de $V$, llamado el subespacio generado por $v_1 , \dots, v_m$.

`\begin{proof}`

a)
$0_{V} \in \langle v_1 , \dots, v_m \rangle$ ya que 
$0_{V} = 0_{F} V_{1} + 0_{F}V_{2} + \dots + 0_{F}V_{m}$
$=0 V_{1} + 0V_{2} + \dots + 0V_{m}$

b)
Sean $\sum_{i=1}^{m} \alpha_{i} v_{i}$ y $\sum_{i=1}^{m} \beta_{i} v_{i}$ vectores en $\langle v_1 , \dots, v_m \rangle$, entonces,
$$\sum_{i=1}^{m} \alpha_{i}v_{i} + \sum_{i=1}^{m} \beta_{i} v_{i} = \sum_{i=1}^{m}(\alpha_{i} + \beta_{i}) v_{i} \in \langle v_1 , \dots, v_m \rangle$$

c)
Sea $\lambda \in F$ y $\sum_{i=1}^{m} \alpha_{i}v_{i} \in \langle v_1 , \dots, v_m \rangle$
Entonces 
$$ 
\begin{align*}
\lambda \left(\sum_{i=1}^{m} \alpha_{i}v_{i}\right) &=  \sum_{i=1}^{m} \lambda(\alpha_{i}v_{i})\\
&= \sum_{i=1}^{m} ( \lambda \alpha_{i})v_{i} \in \langle v_1 , \dots, v_m \rangle
\end{align*}
$$

`\end{proof}`

---

## El espacio renglón y el espacio columna de una matriz

![](https://youtu.be/0OChshsai7c?si=lbCRaUNrT79ocSTA&t=1878)

>[!warning]
>En general la unión de 2 subespacios no es un subespacio. 


>[!hint]
Por convención: $\langle \emptyset \rangle = \{  0_{V} \}$ 

>[!hint]
>$\mathcal{L}$ es subespacio de $\mathbb{R}^{2} \Leftrightarrow \mathcal{L} = \{ 0_{\mathbb{R}^{2}} \}$ ó $\mathcal{L} = \mathbb{R}^{2}$ ó $\mathcal{L}$ es una recta que pasa por $(0,0)$

>[!hint]
>Las matrices invertibles no son subespacios vectoriales

