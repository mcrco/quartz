A null space, or kernel, of a $\mathbf{A}$ is the set of solutions to 

$$
\mathbf{A}\vec{x} = \vec{0}
$$

For example, for

$$
\mathbf{A} = \begin{pmatrix}
-3 & 6 & -1 & 1 & -7  \\
1 & -2 & 2 & 3 & -1 \\
2 & -4 & 5 & 8 & -4
\end{pmatrix}
$$

Solving 

$$
\mathbf{A}\vec{x} = \vec{0} \implies \text{rref}\begin{pmatrix}
-3 & 6 & -1 & 1 & -7 & 0 \\
1 & -2 & 2 & 3 & -1 & 0 \\
2 & -4 & 5 & 8 & -4 & 0
\end{pmatrix}
$$

gives us 

$$
\begin{cases}
x_{1} - 2x_{2} - x_{4} + 3x_{5} = 0 \\
x_{3} + 2x_{4} - 2x_{5} = 0 \\
\end{cases}
$$

The general form of $\vec{x}$ must be

$$
\vec{x} = x_{2}\begin{pmatrix}
2 \\
1 \\
0 \\
0 \\
0
\end{pmatrix} + x_{4} \begin{pmatrix}
1 \\
0 \\
-2 \\
0 \\
0
\end{pmatrix} + x_{5} \begin{pmatrix}
-3 \\
0 \\
2 \\
0 \\
0
\end{pmatrix}
$$

So 

$$
\text{Nul}\mathbf{A} = \text{span}\{ \vec{x_{2}} \vec{x_{3}}, \vec{x_{4}}\}
$$

# [[Linear Transformations]] for Vector Spaces

1. $T(\vec{u} + \vec{v}) = T(\vec{u}) + T(\vec{v})$
2. $T(c\vec{u}) = cT(\vec{u})$

The kernel of $T$ is the set of all $\vec{u} \in V : T(\vec{u}) = \vec{0}$.

