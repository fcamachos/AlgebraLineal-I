# Matrices elementales

Sean $m,n \in \mathbb{N}$. Para cada $1 \leq i \leq m$ y $1 \leq j \leq n$ definimos la [[matriz|matriz]] $E^{ij}$ de $m \times n$ como la matriz cuya entrada $(i,j)$ es igual a 1 y todas las demás son cero. 

>Ejemplo:

Una matriz de $3 \times 2$:
$$
E^{21} = \begin{pmatrix} 0 &0 \\ 1&0 \\ 0 &0\end{pmatrix}
$$

>[!def] Matrices elementales
Para cada $1 \leq k \leq m$ y $1 \leq l \leq n$ , la entrada $(k,l)$ de la matriz $E^{ij}$ es:
$$E^{i,j} = \begin{cases} 1 & \text{si } & (k,l) = (i,j) \\ 0  & \text{si}  & (k,l) \neq (i,j) \end{cases} $$


# Suma de matrices 


>[!def] Suma de matrices
>Sean $A = (a_{ij})$ y $B=(b_{ij})$ matrices de $m \times n$. 
>Definimos la suma $A + B$ como la matriz de $m \times n$ y cuyas entradas son 
>$(A + B)_{(ij)} := A_{(i,j)}+B_{(i,j)}=a_{ij}+b_{ij}$ 
>para cada $1\leq i \leq m$ y $1 \leq j \leq n$ .

^70b466

> Ejemplo

$$
\begin{pmatrix}
3 & -5 & 6 & \sqrt{ 2 } \\
8 & 7 & 0 & 0
\end{pmatrix} +
\begin{pmatrix}
0 & -1 & 1 & 1 \\
\frac{1}{2} & 2 & 1 & 1
\end{pmatrix} =
\begin{pmatrix}
3 & -6 & 7 & 1+\sqrt{ 2 } \\
\frac{17}{2} & 9 & 1 & 1
\end{pmatrix}
$$

## Propiedades de la suma de matrices

Sean $A =(a_{ij}),B=(b_{ij}),C=(c_{ij})$ matrices de $m \times n$.

> [!proposition|a)] Conmutativa
> $A + B = B + A$

^01625e

>[!prp|b)] Asociativa
> $(A+B)+C = A + (B+C)$

^45ca0b

>[!prp|c)] Neutro aditivo
>La matriz cero es neutro aditivo 
>$A + (0)_{m \times n} = A$

^cbda59

>[!prp|d)] [[inverso aditivo]]
> Para cada matriz $A_{m \times n}$ existe una matriz $A'_{m \times n} \quad| \quad A + A'=(0)_{m \times n}$ 

^5fa02e

`\begin{proof}`@[[Clase 06#^01625e]]

Para probar que $A+B=B+A$ , debemos mostrar que para cada $1 \leq i \leq m$ y $1 \leq j \leq n$:
$$
(A+B)_{(ij)} = (B+A)_{(ij)}
$$
Por [[Clase 06#^70b466]] 

$$
\begin{align}
(A + B)_{(ij)} &= A_{(i,j)}+B_{(i,j)}=a_{ij}+b_{ij} \\
&_{\text{Por conmutatividad de los reales:}} \\
&= b_{ij} + a_{ij} = B_{ij} + A_{ij} = (B+A)_{(ij)}
\end{align}
$$
`\end{proof}`


`\begin{proof}`@[[#^45ca0b]]

Para probar que $A + (B+C) = (A+B)+C$, hay que mostrar que para cada $1 \leq i \leq m$ y $1 \leq j \leq n$:
$$
(A + (B+C))_{(i,j)} = ((A+B)+C)_{(i,j)}
$$
Por [[#^70b466]] :
$$
\begin{align}
(A + (B+C))_{(i,j)} &= A_{(i,j)} + (B+C)_{(i,j)} \\
&= A_{(i,j)} + (B_{(i,j)} + C_{(i,j)}) \\
&= a_{i,j} + (b_{i,j} + c_{i,j}) \\
&_{\text{Por asociatividad de los reales:}} \\
&= (a_{i,j} + b_{i,j}) + c_{i,j} \\
&= (A_{(i,j)} + B_{(i,j)}) + C_{(i,j)} \\
&= ((A+B)_{(i,j)}) + C_{(i,j)} \\
&= ((A+B) + C)_{(i,j)}
\end{align}
$$

`\end{proof}`

`\begin{proof}`@[[#^cbda59]]

Debemos probar que $A + (0) = A$, para esto, hay que mostrar que para cada $1 \leq i \leq m$ y $1 \leq j \leq n$:
$$
(A + 0)_{(i,j)} = A(i,j)
$$

Por [[#^70b466]] tenemos que:
$$
\begin{align}
(A+0)_{(i,j)} = A_{(i,j)} + 0(i,j) &= a_{ij} + 0_{F} \\
&= a_{ij} = A(i,j)
\end{align}
$$

`\end{proof}`

`\begin{proof}`@[[#^5fa02e]] 

Sea $A=a_{ij}$. Queremos encontrar $A' = a'_{ij}$ de $m \times n \quad | \quad A + A' = 0$

Tenemos entonces:
$$
\begin{align}
A + A' &= a_{ij} + a'_{ij} = 0 \\
&_{\text{Por inverso aditivo de los reales tenemos que:}} \\
&a'_{ij} = -a_{ij}
\end{align}
$$
Para cada $1 \leq i \leq m$ y $1 \leq j \leq n$.
`\end{proof}`

