---
date: 2024-09-11
video:
  - https://www.youtube.com/watch?v=v4zT62yF3tg
tags:
  - contexto/academico
  - tema/algebra-lineal
---
# Ejercicio 1

Determinar si el sistema tiene solución y en caso afirmativo, encontrar todas las soluciones:

$$
\begin{cases}
2x + y - 2z + 3w &= 1 \\
3x + 2y -z + 3w &= 4 \\
3x + 3y + 3z + 3w &= 5
\end{cases}
$$

Dado un sistema de ecuaciones
$$
\begin{align}
a_{11}x_{1} + \dots + a_{1n}x_{n} &= b_{1} \\
&\vdots \\
a_{m1}x_{1} + \dots + a_{mn}x_{n} &= b_{m}
\end{align}
$$

La matriz aumentada del sistema es 
$$
A|b = \begin{pmatrix}
a_{11}  & \dots & a_{1n}  & \mid & b_{1}\\
 & \vdots  &  & | & \vdots\\
a_{m 1}  & \dots   & a_{mn}  & | & b_{m}
\end{pmatrix}
$$

## Paso 1
Encontrar la matriz aumentada del sistema.

$$
\begin{pmatrix}
2 & 1 & -2 & 3 & | & 1 \\
3 & 2 & -1 & 3 & | & 4 \\
3 & 3 & 3 & 3 & | & 5
\end{pmatrix}
$$

## Paso 2
Obtener la [[Forma Escalonada Reducida por filas]] de $A|b$

$$
\begin{pmatrix}
2 & 1 & -2 & 3 & | & 1 \\
3 & 2 & -1 & 3 & | & 4 \\
3 & 3 & 3 & 3 & | & 5
\end{pmatrix}
\xrightarrow[]{}
\begin{pmatrix}
1 & 0 & -3 & 0 & | & 6 \\
0 & 1 & 4 & 0 & | & -1 \\
0 & 0 & 0 & 1 & | & -\frac{10}{3}
\end{pmatrix}
$$

Como el rango de $A$ y el rango de $b$ coinciden, entonces, el sistema tienen solución. 

## Paso 3
Análisis

$$
\begin{align*}
x - 3z &= 6\\
y + 4z &= -1\\
w &= - \frac{10}{3}
\end{align*}
$$

Por lo que, las soluciones del sistema son 
$$
\left\{ \left( 3z + 6, -1-4z, z, - \frac{10}{3} \right) | z \in \mathbb{R} \right\} 
$$

# Ejercicio 2
Encuentra todos los valores $c$ y $k$ en los números reales tales que el sistema:
$$
\begin{cases}
2x - cy = 8 \\
3x + 9y = k 
\end{cases}
$$

>- No tiene solución
>- Tiene una única solución 
>- Tiene infinidad de soluciones

Aplicamos operaciones elementales por filas para la matriz aumentada del sistema:

$$
\begin{pmatrix}
2  &  - c  & |  & 8  \\
3 & 9 & | & k
\end{pmatrix}
\xrightarrow[]{R_{2} \to -\frac{3}{2} R_{1} + R_{2}}
\begin{pmatrix}
2  &  - c  & |  & 8  \\
0 & - \frac{3}{2}c +9 & | & k-12
\end{pmatrix}
$$
$$
\xrightarrow[]{R_{2} \to 2 R_{2}}
\begin{pmatrix}
2  &  - c  & |  & 8  \\
0 & - 3c + 18 & | & 2k - 24
\end{pmatrix}
$$

Tenemos dos casos:
$3c + 18 = 0$ ó $3c + 18 \neq 0$ 

---

> Si $3c + 18 = 0$, entonces la matriz es:

$$
\begin{pmatrix}
2  &  -c  & |  & 8  \\
0 & 0 & | & 2k - 24
\end{pmatrix}
$$

>> Si $2k = 24$, el rango de $A$ sería igual al rango de $b$ (1), por lo que tendría solución. 

$$
\begin{pmatrix}
2 & -c & | & 8 \\
0 & 0 & | & 0
\end{pmatrix}
$$
Por lo que queda:
$$
2x + 6y = 8
$$

Por lo tanto, si $c = -6$ y $k = 12$, el sistema tiene una infinidad de soluciones.

>> Si $2k -24  \neq 0$

$$
\begin{pmatrix}
2 & -c & | & 8 \\
0 & 0 & | & w
\end{pmatrix}
$$

Como el $rango_{f}R =1$ y el rango $rango_{f}(R|b) =2$, no tiene solución. 


---

> Si $3c + 18 \neq 0$

$$
\begin{pmatrix}
2  &  -c  & |  & 8  \\
0 & 3c + 18 \neq 0 & | & 2k - 24
\end{pmatrix}
\xrightarrow[]{R_{2} \to \frac{1}{3c + 18} R_{2}}
\begin{pmatrix}
2  &  -c  & |  & 8  \\
0 & 1 & | & \frac{2k - 24}{3c+18}
\end{pmatrix}
$$
$$
\xrightarrow[]{R_{1} \to R_{1} + cR_{2}}
\begin{pmatrix}
2  &  0  & |  & 8 + c (\frac{2k - 24}{3c+18})  \\
0 & 1 & | & \frac{2k - 24}{3c+18}
\end{pmatrix}
$$

Como el $rango_{f}R =2$ y el rango $rango_{f}(R|b) =2$,  tiene solución. 

$$
x = \frac{c}{2} \left(\frac{2k - 24}{3c+18}\right)+4
$$
$$
y = \frac{2k - 24}{3c+18}
$$
El sistema tiene una única solución para cualquier $c$ y para cualquier $k$.


[[Tarea 02#Ejercicio 13]]

Sea $Rx = b$ un sistema de $m$ ecuaciones en $n$ variables, supongamos que $(R|b)$ está en la [[Forma Escalonada Reducida por filas]]. 
El sistema tiene solución *sii* el [[rango por filas de R]] es igual al rango por filas de $b$:
$$
rango_{f}(R) = rango_{f}(R|b)
$$

