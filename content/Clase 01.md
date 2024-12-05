
## Números racionales: $\mathbb{Q}$

### Propiedades:

- Neutro aditivo: ``0``
- Neutro multiplicativo: ``1``
- Para todo racional distinto de ``0``, se tiene un inverso multiplicativo, es decir, que su producto da ``= 1``. 

### Ley distributiva:

$$
\begin{align*}
\frac{p}{q}\Big( \frac{a}{b} + \frac{c}{d}    \Big) \\
= \frac{p}{q} \frac{a}{b} + \frac{p}{q} \frac{c}{d}  
\end{align*}
$$




## Campos

Un campo consiste en:
- Un conjunto $F$
- Dos funciones
  - Suma (+): $F \times F \rightarrow F$, $(\lambda, \mu) \mapsto \lambda + \mu$
  - Producto ($\cdot$): $F \times F \rightarrow F$, $(\lambda, \mu) \mapsto \lambda \cdot \mu$

Estas funciones satisfacen las siguientes propiedades:

### Propiedades de la suma 

- Conmutatividad: 
    $x + y = y + x \; \forall \; x,y \in F$
- Asociatividad: 
    $x + (y + z) = (x + y) + z \; \forall \; x,y,z \in F$
- Existencia del neutro aditivo: 
    $\exists e \in F | e + x = x \; \forall \; x \in F$
- Existencia de inversos aditivos:
    Sea $e$ el neutro aditivo; $\forall x \in F, \exists x' \in F | x + x' = e$

### Propiedades del producto

- Conmutatividad:
    $xy = yx \; \forall x,y \in F$
- Asociatividad: 
    $x(yz) = (xy)z \; \forall x,y,z \in F$
- Existencia del neutro multiplicativo: 
    $\exists u \in F$ tal que $u$ no es neutro aditivo y $ux = x \; \forall x \in F$
- Existencia del inverso multiplicativo:
    Para cada $x \in F$ que no es el neutro aditivo, $\exists y \in F | xy = u$
- Ley distributiva:
    $x(y+z) = xy + xz \; \forall x,y,z \in F$


>[!note] Proposición:
Sea $F$ un **campo**. Entonces:
> - **a)** $F$ tiene un único neutro aditivo.
> - **b)** $F$ tiene un único neutro multiplicativo.
> - **c)** Dado $x \in F$ existe un único $x' \in F | x +  x' = e$
> - **d)** Dado $x \in F$ existe un único $x' \in F | x \cdot x' = u$

Demostración:
---

> a) 

Suponemos que $e$ y $e'$ son neutros aditivos de $F$.

P.D. que $e=e'$

Como $e'$ es neutro aditivo, entonces se debe cumplir que 

$$
e = e + e' \tag{1}
$$

Por otro lado, tenemos que $e$ es neutro aditivo, entonces se debe cumplir que 

$$
e' = e + e' \tag{2}
$$

Por $(1)$ y $(2)$ tenemos que 

$$e = e' \tag{$\square$}$$ 

> b)

Suponemos que $u$ y $u'$  son neutros multiplicativos de $F$. Entonces:

Como $u'$ es neutro multiplicativo, entonces se debe cumplir que:

$$
u = u \cdot u' \tag{1}
$$
Por otro lado, como $u$ es neutro multiplicativo, entonces se debe cumplir que:

$$
u' = u \cdot u' \tag{2}
$$

Por $(1)$ y $(2)$ tenemos que 
$$u' = u \tag{$\square$}$$


> c)

Supongamos que: 
- $x \in F$ 
- $x'$ y $x''$ son inversos aditivos de $x$

P.D. que $x' = x''$

Sabemos que si 
$$
\begin{align}
a+b = a+c \\
\forall a,b,c \in F
\end{align}
$$ 
entonces:
$$b=c \tag{1}$$

(Demostración de $(1)$):

Sea $a'$ inverso aditivo de $a$, entonces:
$$
\begin{align}
a' + (a +b)  & = a' + (a +c) \\
(a' + a) +b  & = (a' + a) +c \\
e + b  & = e + c  \\
b  & = c
\end{align}
$$

Además, tenemos que

$$x +x' = 0$$
y que 

$$x+x''=0$$

Es decir: 

$$
x + x' = x +x''
$$

Por $(1)$ podemos decir entonces que: 

$$
x' = x'' \tag{$\square$}
$$


> d)

Sea $x \in F | x \neq e$.

Supongamos que $y'$ y $y''$ son inversos multiplicativos de $x$.

P.D. $y'=y''$.

Sabemos que si $a \neq e$
$$
ab = ac
$$

entonces:
$$
b = c \tag{1}
$$

Demostración de $(1)$:

Como $a \neq e$ entonces tiene neutro multiplicativo. 
Sea $a' \in F$ inverso multiplicativo de $a$. 
Entonces: 
$$
\begin{align}
a'(ab)  & = a'(ac) \\
(a'a)b  & = (a'a) c \\
ub & = uc \\
b & =c 
\end{align}
$$

Sabemos que $xy' = u$ y $xy''=u$, es decir: $xy'=xy''$. Por $(1)$ tenemos entonces que:
$$
y' =y'' \tag{$\square$}
$$


### Notación

Si $F$ es un campo, entonces $0_{F} = 0$ es el neutro aditivo  y $1_{F}=1$, es el neutro multiplicativo.

Si $x \in F, -x$ denota su inverso aditivo. 
Si $x\in F$ y $x \neq 0_{F}, x^{-1}= \frac{1}{x}$ denota su inverso multiplicativo.