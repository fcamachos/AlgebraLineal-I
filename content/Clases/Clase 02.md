---
date: 2024-08-09
video: 
tags:
  - contexto/academico
  - tema/algebra-lineal
---


 >[!def] Ley de la cancelación para la suma
 >Sea $F$ un [[campo]]. 
 >Si $a+b = a+c$ donde $a,b,c \in F$. Entonces $b=c$.

> [!def] Ley de la cancelación para el producto
> Si $ab = ac$ donde $a,b,c \in F$ y $a \neq 0_{F}$, entonces $b=c$


> [!prp]
> Sea $F$ un [[campo]], entonces,
> a) $0_{F} \cdot a=0_{F} \forall a \in F$
> b) $-1 \cdot a = -a \forall a \in F$, donde $-1$ es el [[inverso aditivo]] de $1=1_{F}$ 
> c) $-(-a)=a \forall a \in F$
> d) $-(ab)=(-a)b=a(-b)$ 


Dem: 
a)

$$
\begin{align}
0_{F}+0_{F} \cdot a = 0_{F} \cdot a &= (0_{F} + 0_{F})a \\
&= 0_{F} a + 0_{F}a \\
0_{F}+ \cancel{0_{F}a} &= 0_{F}a + \cancel{0_{F}a} \tag{Por ley de cancelación} \\
0_{F} = 0_{F}a
\end{align}
$$



b) 

Probaremos que $-1 \cdot a$ es un [[inverso aditivo]] de $a$ y después probaremos el hecho de que el [[inverso aditivo]] de $a$ es único, para concluir que $-1 \cdot a = -a$.

$$
\begin{align}
-1 \cdot a +a & = (-1 + 1) a \\
&= 0a \\
&= 0
\end{align}
$$

c)

Por la unicidad del [[inverso aditivo]] de $-a$ Probaremos que $a + (-a) = 0$ , es decir, que $a$ es [[inverso aditivo]] de $-a$.

$$
\begin{align}
-a +a &= (-1+1)a   \\
&= 0
\end{align}
$$

d)

Tarea: Probar que $-(ab) = a(-b)$

Probaremos que $-(ab)= (-a)b$ . Por la unicidad del [[inverso aditivo]] de $ab$ basta probar que $ab + (-a)b=0$

$$
\begin{align}
ab + (-a)b & = (a + (-a))b \\
&= (0)b  \\
&= 0 \tag{$ \square$}
\end{align}
$$

> Tarea: 

Probaremos que $-(ab)= a(-b)$. Por la unicidad del [[inverso aditivo]] basta probar que $ab + a(-b)=0$

$$
\begin{align}
ab + a(-b) &= a(b-b) \\
&= a(0) \\
&= 0 \tag{$\square$}
\end{align}
$$

---


> [!prp] [[campo]] mínimo
> Sea $\Gamma = \left\{  a,b \right\}, a\neq b$
> 

Tenemos un mínimo de 2 elementos porque uno de ellos debe ser el neutro aditivo, y el otro, el neutro multiplicativo, no puede ser el mismo que el neutro aditivo. 

Operaciones de suma:

|  +  |  a  |  b  |
| :-: | :-: | :-: |
|  a  |  a  |  b  |
|  b  |  b  |  a  |

Operaciones de multiplicación:

| $\cdot$ |  a  |  b  |
| :-----: | :-: | :-: |
|    a    |  a  |  a  |
|    b    |  a  |  b  |

Revisión de las propiedades:
$$
\begin{align}
(a+b)b = b\cdot b = b \\
ab + b b = a +b = b
\end{align}
$$

 ---



## Racionales

Sea $\mathbb{Q}(\sqrt{ 2 })= \left\{ a + b \sqrt{ 2 } | a,b \in \mathbb{Q} \right\}$, un [[campo]]. 

$\mathbb{Q}(\sqrt{ 2 }) \subseteq \mathbb{R}$

$(a + b \sqrt{ 2 }) + (c+d\sqrt{ 2 }) = a+c + (b+d)\sqrt{ 2 }$ donde $a+c, (b+d) \in \mathbb{Q}$



