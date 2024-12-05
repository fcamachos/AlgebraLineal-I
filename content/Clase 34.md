---
fecha: 2024-11-12
video: 
tags:
  - contexto/academico
  - tema/algebra-lineal/transformaciones-lineales
  - tipo/estudio
aliases:
  - transformaciones lineales
pdf: "[[20241111 11 de nov.pdf]]"
---

pdf: "[[20241111 11 de nov.pdf]]"

# Transformaciones lineales



Sean 2 espacios vectoriales sobre el mismo campo. Una función es lineal si satisface que:
- $T(v + w) = T(v) + T(w)$ (T es aditiva)
- $T(\alpha v) = \alpha T(v)$ (T es F-lineal)

>[!teorema] 
>Sean $T:V \to W$ una transformación lineal. 
> - $T(O_{V})= 0_{W}$
> - $T(-v) = - T(v) \quad \forall v \in V$

**Dem**
i)
$$
0_{w} + \underset{ \in \mathbb{N} }{ T(0_{V}) } = T (0_{V}) = T (0_{V} + 0_{v}) \dots
$$

ii)
Sea $v \in V$
PD $T(-v) = -T(v)$
Tenemos que $-v = -1 v$, entonces:
$$
T(-v) = T(-1v) \underset{ T \text{es }F-\text{lineal} }{ = } -1 T(v) = -T (v)
$$
$\square$

---
## Ejemplo 
a)
Sea $V$ un $F$-e.v. y $1_{v} = id_{v}:V \to V$ la función identidad. 
$1_{V}$ es una transformación lineal. 
b)
Sea $V_{1} N$ un F-ev. y $0:v\to W$ la función definida como $0(v) = 0_{W} \forall v \in V$ es una transformación lineal llamada la **transformación cero**. 

---

* Probar que es aditiva:
Sean $v,v' \in V$
PD
$0(v + v') = 0 (v) + 0(v')$

$$
\begin{align*}
0(v + v') &=  0_{w}\\
0(v) + 0(v') &= 0_{w} + 0_{w} &= 0_{w}\\
\therefore 0\text{ es aditiva}
\end{align*}
$$

* Probar que...

Sean $v \in V$ y $\alpha \in F$ 
PD 
$0(av) =  \alpha 0(v)$
....

---

c) "La multiplicación por A"
Sean $\mathbb{R}_{3}[x] = \{ f(x) \in \mathbb{R}[x] \setminus f(x) = 0 \text{ ó grado } f(x \leq 3) \}$
$\{ a_{0}+a_{1}x + a_{2}x^{2} + a_{3} x^{3} \} \quad \Big| \quad a_{0}, a_{1}, a_{2}, a_{3} \in \mathbb{R}$
...

Definimos $D:\mathbb{R}_{3}[x] \to \mathbb{R}_{2}[x]$ como: 
$D(a_{0}+a_{1}x +a_{2}x^{2}+a_{3}x^{3}) = a_{1} + 2a_{2}x + 3a_{3}x^{2}$

$D$ es una transformación lineal (derivada)

d) Sea $A = \begin{pmatrix} 2 & -1 & 3 & 4 \\ 0 & 0& 1& 1 \end{pmatrix}_{2 \times4} \in \mathcal{M}_{2 \times 4} (\mathbb{R})$

La  matriz A induce una transformación lineal
$$
\begin{align*}
T_{A}: \mathbb{R}^{4} \to \mathbb{R}^{2}
\end{align*}
$$

Definida como:
$$
T_{A}(x) = Ax = \begin{pmatrix} 2 & -1 & 3 & 4 \\ 0 & 0& 1& 1 \end{pmatrix} \begin{pmatrix}
x_{1}  \\
x_{2} \\
x_{3} \\
x_{4}
\end{pmatrix}
$$
Sean $x,x' \in \mathbb{R} ^{4}$
$T_{A} (x + x') = A (x + x') = Ax + A x' = T_{A} (x) + T_{A} (x')$

Sean $x \in \mathbb{R}^{4}, \alpha \in \mathbb{R}$
$$
T_{A}(\alpha x) = A(\alpha x) = \alpha( Ax) = \alpha T_{A}(x)
$$

e) Sea $A \in M_{m \times n} (F)$, A induce una transformación lineal $T_{A} : F^{n} \to F ^{m}$ dada por $T_{A}(x) = A_{x} \forall x \in F^{n}$

La transformación lineal $T_{A}$ se llama la transformación por A.

---
4)
# Núcleo de una transformación lineal

Sean $T:V \to W$ una transformación lineal. 

Definimos el núcleo o *kernel* de $T$, denotado $Nuc(T) = Ker(T)$, como 
$ker(T) = \{  v \in V \quad \Big| \quad T(v) = 0_{w} \}$

Además el $Ker(T)$ es subespacio de $V$.

**Dem**
- Probar que el vector cero de v está en el núcleo. 
$0_{V} \in Ker(T)$ ya que $T(0_{V}) = 0_{W}$

* Probar que es cerrado bajo la suma
Sean $v,v' \in Ker(T)$ 
PD
$v + v' \in Ker(T)\quad ie. \quad T(v+v') = 0_{W}$
Tenemos que 
$$
T(v + v') = T(v) + T(v') \dots
$$
Sean $v \in Ker(T)$ y $\alpha \in F$
PD $\alpha v \in Ker(T)$
PD $T(\alpha v ) = 0_{W}$

$$
T(\alpha v) = \alpha T(v) = \alpha 0_{W} = 0_{w}
$$

---
5)

Sea $T:V \to W$ una transformación lineal. 

Entonces $T$ es inyectiva si y solo si el núcleo de la transformación sólo tiene al vector cero: $Ker(T) = \{  0_{v} \}$

**Dem**
$\implies$
Sup que $T$ es inyectiva. 

Sea $v \in Ker(T)$ PD $v = 0_{v}$

Como $v \in ker(t)$, $T(v) = 0_{w}$ y por otro lado $T(0_{v}) = 0_{w}$.

Por tanto $T(v) = 0_{w} = T(0_{V})$ 

$f$ es inyectiva si siempre que $f(a) = f(a')$, entonces $a = a'$ 

Como $T$ es inyectiva, $v = 0_{v}$

$\impliedby$
Sup que $Ker(T) = \{ 0_{V} \}$
PD T es inyectiva
Sup que $T(v) = T(v')$ donde $v,v' \in V$
PD $v = v'$

Como $T(V) = T(v')$, sumando el inverso de $T(v')$ obtenemos que $T(v)-T(v') = 0_{w}$

Como $T$ es transformación lineal $-T(v') = T(v')$, así que
$T(v)- T(v') = T(v)\dots$

---
6)
Ejemplos 

a)
Calcular el núcleo de la transformación identidad $1_{v}: V\to V$

$Ker(1_{v}) = \{  v \in V \quad \Big| \quad 1_{v} (v) = 0_{v} \}$
...


b) 

**Núcleo de la Transformación cero**

c) 
**Núcleo de la derivada**

d)

**Núcleo de matriz**

Por tanto
el sistema Ax = 0 tiene solo la solución trivial sii el núcleo de T_A = {0} sii T_A es inyectiva

El sistema Ax = 0 tiene soluciones no triviales sii el núcleo no es el subespacio cero. sii la transformación T_A no es inyectiva. 