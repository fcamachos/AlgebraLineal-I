---
fecha: 2024-11-14
video: 
tags:
  - tipo/estudio
  - contexto/academico
  - tema/algebra-lineal/transformaciones-lineales
pdf: "[[20241115 Clase 15 de noviembre.pdf]]"
---

pdf: "[[20241115 Clase 15 de noviembre.pdf]]"

Transformación lineal: $\mathbb{R}^{2} \to \mathbb{R}^{3}$

tomo una base de $\mathbb{R}^{2}$, y defino una función lineal que manda la base a $\mathbb{R}^{3}$. 


---

$T: V \to W$ una transformación lineal.
$Im(T) = T (V) = \{ T(v) \quad \Big| \quad v \in V \}$ es subespacio de $V$, además, $T$ es suprayectiva si y solo si $\mathrm{Im} (T) = W$.


1 
Sea $A \in \mathcal{M}_{m \times n}(F)$, y sea $T_{A} : F^{n} \to F^{m}$ la transformación lineal dada por $T_{A}(x) = Ax$, donde $x = \begin{pmatrix} x_{1} \\ \vdots \\x_{n} \end{pmatrix}$.

Ya sabemos que $ker(T_{A})$ es igual al espacio solución del sistema $Ax = 0$.

Vamos a calcular la imagen de $T_{A}$.
Tenemos que: Un vector $b \in F ^{m}$ pertenece a $\mathrm{Im}(T)$ 
si y solo si existe un vector $s \in F ^{n}$ tal que $T(s) = b$ 
si y solo si $T(s) = As =b$ 
si y solo si $s$ es solución del sistema $Ax = b$.

