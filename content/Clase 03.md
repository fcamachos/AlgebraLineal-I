

> [!def] Propiedades de los inversos multiplicativos
> Sea $F$ un [[campo]] y $x,x_{1},\dots,x_{n} \in F$, elementos distintos de cero, entonces:
  a) $xy\neq 0_{F}=0;(xy)^{-1} = x^{-1}y^{-1}$
  b) $(x_{1},x_{2},\dots x_{n})^{-1} = x_{1}^{-1} x_{2}^{-1} \dots x_{n}^{-1}$
  c) $(x ^{-1})^{-1} = x$
  d) $1_{F}^{-1}=1_{F}, (-1_{F})^{-1} = -1_{F},(-1_{F})^{2}=1_{F}$



`\begin{proof}`
a) $xy\neq 0_{F}=0;(xy)^{-1} = x^{-1}y^{-1}$

Suponemos que $xy =0_{F}$, entonces
$$
xy=0_{F} = x0_{F}
$$
por hipótesis $x\neq 0_{f}$ y $y \neq 0_{F}$

Por la ley de la cancelación para el producto: $y = 0_{F}$, lo cual es una contradicción ya que $y \neq 0_{f}$

Para mostrar que $(xy)^{-1} = x^{-1}y^{-1}$ basta probar que $x^{-1}y^{-1}$ es inverso multiplicativo de $xy$.
$$
\begin{align}
(xy)(x^{-1}y^{-1})  & = (yx)(x^{-1}y^{-1}) \\
 & = y(xx ^{-1})y^{-1} \\
 & = y \cdot 1_{F} y^{-1}  \\
 & = yy^{-1}  \\
 & = 1_{F}
\end{align}
$$
`\end{proof}`

`\begin{proof}`

b) $(x_{1},x_{2},\dots x_{n})^{-1} = x_{1}^{-1} x_{2}^{-1} \dots x_{n}^{-1}$

Procedemos por inducción a partir de $n \geq 2$:
$n = 2$ es el inciso a) 

H.I.
Supongamos cierto para $n-1$, es decir que $(x_{1},x_{2},\dots x_{n-1})^{-1} = x_{1}^{-1} x_{2}^{-1} \dots x_{n-1}^{-1}$

P.D. $(x_{1},x_{2},\dots x_{n})^{-1} = x_{1}^{-1} x_{2}^{-1} \dots x_{n}^{-1}$

Sea $y = x_{1}x_{2}\dots x_{n-1}$
entonces, $(x_{1}x_{2}\dots x_{n-1}x_{n})^{-1} =(yx_{n})^{-1}$
$= y ^{-1} x_{n}^{-1} = (x_{1} x_{2} \dots x_{n-1})^{-1} x_{n}^{-1}$
Por H.I.
$= x_{1}^{-1}x_{2}^{-1}\dots x_{n-1}^{-1}x_{n}^{-1}$

`\end{proof}`

`\begin{proof}`
c) $(x ^{-1})^{-1} = x$

Queremos que el inverso multiplicativo de $x ^{-1}$ sea $x$. 
Esto es cierto, pues $x x^{-1} = 1$
Por unicidad del inverso multiplicativo de $x ^{-1}$:
$$
x = (x^{-1})^{-1}
$$
`\end{proof}`

`\begin{proof}`
d) $1_{F}^{-1}=1_{F}, (-1_{F})^{-1} = -1_{F},(-1_{F})^{2}=1_{F}$

$1_{F}^{-1} = 1_{F}$ es cierto pues $1_{F} \cdot 1_{F} = 1_{F}$ y por unicidad del inverso multiplicativo de $1_{F}$

$(-1_{F})^{-1} = -1_{F}$ es cierto por unicidad y que $(-1)(-1)=1$

$(-1_{F})^{2} =1_{F}$  es cierto porque $(-1)(-1) =1$ 
`\end{proof}`

---


Sea $p$ un primo.
Sea $\mathbb{Q}(\sqrt{ p }) = \left\{  a + b \sqrt{ p } | a,b \in \mathbb{Q} \right\}$ es un subconjunto propio de los números reales. 

$$
+: \mathbb{Q}(\sqrt{ p }) \times \mathbb{Q}(\sqrt{ p }) \to \mathbb{Q}(\sqrt{ p })
$$
Operación cerrada en los números reales
$$
 \begin{align}
a_{1} + b_{1} \sqrt{ p }, a_{2} + b_{2} \sqrt{ p } \in \mathbb{Q}(\sqrt{ p }) \\
(a_{1} + b_{1} \sqrt{ p }) + (a_{2} + b_{2} \sqrt{ p }) = (a_{1} + a_{2}) + (b_{1} + b_{2}) \sqrt{ p } \in \mathbb{Q}(\sqrt{ p })
\end{align}
$$

$$
\cdot : \mathbb{Q}(\sqrt{ p }) \times \mathbb{Q}(\sqrt{ p }) \to \mathbb{Q}(\sqrt{ p })
$$

Operación cerrada en los números reales

$$
 \begin{align}
a_{1} + b_{1} \sqrt{ p }, a_{2} + b_{2} \sqrt{ p } \in \mathbb{Q}(\sqrt{ p }) \\
(a_{1} + b_{1} \sqrt{ p })  (a_{2} + b_{2} \sqrt{ p })  
 & = a_{1}a_{2}+a_{1}b_{2}\sqrt{ p }+b_{1}a_{2}\sqrt{ p } + b_{1}b_{2}p  \\
 & = (a_{2}a_{2} + b_{1}b_{2}p) + (a_{1}b_{2}+b_{1}a_{2})\sqrt{ p }
\end{align}
$$


Sobre el 0:
$0 \in \mathbb{Q}(\sqrt{ p })$ pues $0=0+0\sqrt{ p }$
Inverso aditivo de $a + b\sqrt{ p }$ es $-a-b\sqrt{ p } \in \mathbb{Q}(\sqrt{ p })$

> [!cor] El inverso aditivo de $a+b \sqrt{ p }$ es:
> $-a -b \sqrt{ p } \in \mathbb{Q}(\sqrt{ p })$

^4110b2



Por lo que es cerrado en inversos aditivos.

Sobre el 1:
$1= 1 + 0\sqrt{ p } \in \mathbb{Q}(\sqrt{ p })$

Inversos multiplicativos:

> [!cor] Inverso multiplicativo:
Si $a+b \sqrt{ p } \neq 0$
$(a+b\sqrt{ p })^{-1} \in \mathbb{Q}(\sqrt{ p })$
$$ \frac{a}{a^{2}+b^{2}p} -\sqrt{ p } \frac{b}{a^{2}+b^{2}p} $$

^1aa756

