---
date: 2024-09-13
video:
  - https://www.youtube.com/watch?v=ifMIn3tnZ2s
  - https://www.youtube.com/watch?v=IkXi0IHRBdE
tags:
  - contexto/academico
  - tema/algebra-lineal
pdf:
---
# Ejercicios 

## 1
> Obtener la [[Forma Escalonada Reducida por filas]] de:

$$
\begin{pmatrix}
i & -(1+i)  & 0 \\
1 & -2 & 1 \\
1 & 2i & -1
\end{pmatrix}
$$

$$
\begin{pmatrix}
i & -(1+i)  & 0 \\
1 & -2 & 1 \\
1 & 2i & -1
\end{pmatrix}
\xrightarrow[]{A_{1} \to A_{2}}
\begin{pmatrix}
1 & -2 & 1 \\
i & -(1+i)  & 0 \\
1 & 2i & -1
\end{pmatrix}
\xrightarrow[A_{2} \to A_{2} - A_{1}]{A_{2} \to A_{2} - i A_{1}}
\begin{pmatrix}
1 & -2 & 1 \\
0 & i-1  & -i \\
0 & 2+2i & -2
\end{pmatrix}
$$
$$
\xrightarrow[]{A_{3} \to \frac{1}{2}A_{3}}
\begin{pmatrix}
1 & -2 & 1 \\
i & i-1  & -i \\
0 & 1+i & -1
\end{pmatrix}
\xrightarrow[]{A_{2} \to \frac{1}{i-1}A_{2}}
\begin{pmatrix}
1 & -2 & 1 \\
0 & 1  & -\frac{i}{i-1} \\
0 & 1+i & -1
\end{pmatrix}
$$
$$
\xrightarrow[]{A_{1} \to A_{1}+ 2A_{2}}
\begin{pmatrix}
1 & 0 & 2\left( \frac{i}{i-1} \right) +1\\
0 & 1  & -\frac{i}{i-1} \\
0 & 1+i & -1
\end{pmatrix}
\xrightarrow[]{A_{3} \to A_{3} - (1+i) A_{2}}
\begin{pmatrix}
1 & 0 & \left( \frac{2i}{i-1} \right) +1\\
0 & 1  & -\frac{i}{i-1} \\
0 & 0 & \frac{(1+i)i}{i-1} -1
\end{pmatrix}
$$

Resolviendo:
$$
\frac{2i}{i-1} \left( \frac{-1-i}{-1-i} \right) +1 = \frac{-2i-2i^{2}}{1-i^{2}} +1 = \frac{2-2i}{2} + 1= 1-i +1 = 2-i
$$
$$
\begin{pmatrix}
1 & 0 & 2-i\\
0 & 1  & -\frac{i}{i-1} \\
0 & 0 & \frac{(1+i)i}{i-1} -1
\end{pmatrix}
$$
Resolviendo: 
$$
-\frac{i}{i-1} \left( \frac{-1-i}{-1-i} \right)=- \frac{-i-i^{2}}{1-i^{2}} = - \left( \frac{1-i}{2} \right) = \frac{-1+i}{2}
$$

$$
\begin{pmatrix}
1 & 0 & 2-i\\
0 & 1  & \frac{-1+i}{2} \\
0 & 0 & \frac{(1+i)i}{i-1} -1
\end{pmatrix}
$$
Resolviendo:
$$
\frac{(1+i)i}{i-1}-1 = \frac{i+i^{2}}{i-1} -1 = \frac{-1 + i}{i-1} -1 = \frac{-1 + i}{i-1} \left( \frac{-1-i}{-1-i} \right) -1
$$
$$
= \frac{1+i-i-i^{2}}{-i^{2}+1} -1= \frac{2}{2} -1 = 0
$$

Por lo que queda la matriz:
$$
\begin{pmatrix}
1 & 0 & 2-i\\
0 & 1  & \frac{-1+i}{2} \\
0 & 0 & 0
\end{pmatrix}
$$

---

# Soluciones no triviales
En sistemas homogéneos

Sea $R$ una matriz de $m \times n$ que está en la [[Forma Escalonada Reducida por filas]]. 
El sistema de ecuaciones $Rx = 0$ tiene solución no trivial *sii* $n - rango_{f}(R) > 0$. Es decir, si el número de columnas menos el rango de $R$ es mayor a cero. 


`\begin{proof}`

Supongamos que el sistema $Rx = 0$ tiene solución no trivial. 

Supongamos que el $rango_{f}(R) =r$ y que el pivote del renglón $R_{i}$ se encuentra en la columna $k_{i}$ para cada $1 \leq i \leq r$.

El sistema de ecuaciones en la forma
$$
x_{k_{i}} + \sum_{k=1}^{n-r} c_{kj} u_{j} 
$$

Donde $u_{1}, \dots, u_{n-r}$ son las variables dependientes

Si $n = r$, entonces, todas las columnas de $R$ son columnas pivote.
Por lo que la matriz sería una matriz identidad, por lo que la solución es trivial:
$$
(0,0,\dots,0)
$$

Por hipótesis, el sistema tiene solución no trivial, por lo que $n-r > 0$

Si $n-r > 0$, hay columnas de $R$ que no son columnas pivote.

Sea $u_{1}, \dots,u_{n-r}$ las variables independientes. 
Cada variable dependiente se obtiene un valor para ella una vez asignamos valores a las variables independientes. 
`\end{proof}`

---

# Soluciones no triviales
En sistemas no homogéneos.

Sea $(R|c)$ una matriz de $m \times (n+1)$ que está en la [[Forma Escalonada Reducida por filas]].
El sistema $Rx = c$ tiene solución $sii$ el rango por filas de $R$ es igual al rango por filas de $(R|c)$.
Además, si el sistema tiene solución, entonces tenemos las siguientes posibilidades:
- $m <n$ 
- $n < m$
- $m = n$

> Si $m <n$

Entonces el sistema tiene infinidad de soluciones. 

> Si $n < m$

Tenemos dos posibilidades:
>> $r<n$

Hay un número infinito de soluciones

>> $r = n$

Hay una única solución. 

> $m = n$

Entonces $r \leq n$ y en este caso:
>> $r<n$ 

Número infinito de soluciones.

>> $r = n$

Hay una única solución. 

---

