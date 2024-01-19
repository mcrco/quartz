Solve for

$$
\begin{align}
2x_{1} + 4x_{2} + 6x_{3} &= 18 \\
4x_{1} + 5x_{2} + 6x_{3} &= 24  \\
3x_{1} + x_{2} - 2x_{3} &= 4 \\
\end{align}
$$

Normally, we use algebra:

$$
\begin{align}
2(1) - (2) \implies 3x_{2} + 6x_{3} = 12 \implies x_{2} + 2x_{3} = 4 \\
\frac{3}{2}(1) - (3) \implies 5x_{2} + 11x_{3} = 23 \implies x_{3} = 3,x_{2}=-2, x_{1}=4 \\
\end{align}
$$

But we can also use [[Row Reduction and Echelon Forms|matrices]]. The original equation is

$$
\begin{pmatrix}
2 & 4 & 6 & 18 \\
4 & 5 & 6 & 24 \\
3 & 1 & -2 & 4
\end{pmatrix}
$$

And solving

$$
\begin{align}
R_{1} \to R_{1} + 3R_{3}, R_{2} \to R_{2} + 3R_{3} &\implies 
\begin{pmatrix}
11 & 7 & 0 & 30 \\
13 & 8 & 0 & 36 \\
3 & 1 & -2 & 4
\end{pmatrix} \\
R_{2} \to R_{2} - R_{1} &\implies 
\begin{pmatrix}
11 & 7 & 0 & 30 \\
2 & 1 & 0 & 6 \\
3 & 1 & -2 & 4
\end{pmatrix} \\
R_{2} \to 7R_{2} - R_{1} &\implies 
\begin{pmatrix}
11 & 7 & 0 & 30 \\
3 & 0 & 0 & 12 \\
1 & 0 & -2 & -2
\end{pmatrix} \\
R_{3} \to R_{2} - 3R_{3} &\implies
\begin{pmatrix}
11 & 7 & 0 & 30 \\
3 & 0 & 0 & 12 \\
0 & 0 & 6 & 18
\end{pmatrix} \\
R_{1} \to R_{1} - \frac{11}{3} R_{2} &\implies
\begin{pmatrix}
0 & 7 & 0 & -14 \\
3 & 0 & 0 & 12 \\
0 & 0 & 6 & 18
\end{pmatrix} \\
&\implies 
\begin{pmatrix}
1 & 0 & 0 & 4 \\
0 & 1 & 0 & -2 \\
0 & 0 & 1 & 3
\end{pmatrix} \\
\end{align}
$$

Using the augmented matrix to row echelon form method, we get the same answer.
$$
\begin{align}

\end{align}
$$
# Cramer's Rule

## Theorem

Let $\mathbf{A}$ be an invertible $n\times n$ matrix. For any $\vec{b}$ in $\mathbb{R}^{n}$, the unique solution $\vec{x}$ of $\mathbf{A}\vec{x}=\vec{b}$ has entries given by

$$
x_{i} = \frac{\det \mathbf{A}_{i}(\vec{b})}{\det \mathbf{A}}
$$

## Proof

## Practice

Solve the system of linear equations using Cramer's Rule.

$$
\begin{equation}
\begin{cases}
2x_{1} + 3x_{2} - x_{3} = 5 \\
-x_{1} + 2x_{2} + 3x_{3} = 0 \\
4x_{1} - x_{2} + x_{3} = -1
\end{cases}
\end{equation}
$$

$$
\begin{align}
\mathbf{A} &= \begin{bmatrix}
2 & 3 & -1  \\
-1 & 2 & 3  \\
4 & -1 & 1
\end{bmatrix} \\
\det \mathbf{A} &= 56 \\
\mathbf{A}_{x_{1}} &= \begin{bmatrix}
5 & 3 & -1 \\
0 & 2 & 3 \\
-1 & -1 & 1
\end{bmatrix} \\
\det \mathbf{A_{x_{1}}} &= 14 \\
x_{1} &= \frac{1}{4} \\
\mathbf{A}_{x_{2}} &= \begin{bmatrix}
2 & 5 & -1 &  \\
-1 & 0 & 3 \\
4 & -1 & 1
\end{bmatrix} \\
\det \mathbf{A_{x_{2}}} &= 70 \\
x_{2} &= \frac{5}{4} \\
\mathbf{A}_{x_{3}} &= \begin{bmatrix}
2 & 3 & 5 \\
-1 & 2 & 0 \\
4 & -1 & -1
\end{bmatrix} \\
\det \mathbf{A_{x_{3}}} &= -42 \\
x_{3} &= -\frac{3}{4}
\end{align}
$$