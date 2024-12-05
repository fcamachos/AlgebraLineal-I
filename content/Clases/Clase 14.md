---
date: 2024-09-09
video:
  - https://www.youtube.com/watch?v=GSaRdpBRqLU
tags:
  - contexto/academico
  - tema/algebra-lineal
relación: "[[Ayudantía 09]]"
---

# Variables dependientes e independientes

Sea $R$ una matriz de $m \times n$ con entradas en un campo y que está en [[Forma Escalonada Reducida por filas]], y supongamos que el [[rango por filas de R]] es $r$.
Observemos que $r \leq m$. 
$$
Rx = 0
$$
Si el renglón $i$ es no nulo y el pivote del renglón $i$ se encuentra en la columna $k_{i}$, las variables $x_{k_{1}},\dots, x_{k_{r}}$ son las *variables dependientes* y las restantes $n-r$ las llamamos *variables independientes*.

$$
\begin{align} 
x_{k_{1}} \quad x_{k_{2}} \quad x_{k_{r}} \quad \\
k_{1} \quad k_{2} \qquad k_{r} \quad \\
R=
\begin{pmatrix}
0  &  \dots & 1 & 0 & \dots & 0 \\
0 & \dots & 0 & 1 & \dots & 0 \\
\vdots \\
0 & \dots & 0 & 0 & \dots & 1
\end{pmatrix}
\end{align}
$$

Denotemos por $u_{1}, \dots, u_{n-r}$ a las variables independientes. 
Entonces:
$$
\begin{align*}
Rx &= 0\\
R &= (c_{lr})
\end{align*}
$$$$
\begin{align*}
x_{k_{1}} + \sum_{j=1}^{n-r} c_{1j} u_{j} &= 0\\
x_{k_{2}} + \sum_{j=1}^{n-r} c_{2j} u_{j} &= 0\\
x_{k_{r}} + \sum_{j=1}^{r} c_{rj} u_{j} &= 0
\end{align*}
$$
Hay variables independientes si $n-r > 0$ y en este caso, cada vez que se asigna un valor a cada variable independiente se obtienen valores para las variables dependientes. 

> Ejemplo 1

Sea 
$$
\begin{cases}
3x -12y + 2z &= 0\\
-x + y + z &= 0\\
y - z &= 0\\
x + y + z &= 0
\end{cases}
$$

> a) La matriz de coeficientes:

$$
\begin{pmatrix}
3 & -2 & 2 \\
-1 & 1 & 1 \\
0 & 1 & -1 \\
1 & 1 & 1
\end{pmatrix}
$$
> b) La [[Forma Escalonada Reducida por filas]]

$$
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
0 & 0 & 0
\end{pmatrix}
$$
> c) Conclusión 

$$
\begin{align*}
x &= 0 \\
y &= 0 \\
z &= 0 \\
\end{align*}
$$

No hay variables independientes.

> Ejemplo 2

$$
\begin{align}
-x -y -z = 0 \\
x + 5z = 0
\end{align}
$$
> a) 

$$
\begin{pmatrix}
-1 & -1 & -1 \\
1 & 0 & 5
\end{pmatrix}
$$
> b) 

$$
\begin{pmatrix}
1 & 0  & 5 \\
0 & 1 & -4
\end{pmatrix}
$$
> c) 

$x,y$ son variables dependientes. $z$ es la variable independiente ($n-r$)
$$
\begin{align*}
x + 5z &= 0\\
y -4z &= 0
\end{align*}
$$
Por lo que se dice que tiene infinitas soluciones. 

> [Más ejemplos](https://youtu.be/GSaRdpBRqLU?si=0tfr7BjvH5sMPMwb&t=2930)

