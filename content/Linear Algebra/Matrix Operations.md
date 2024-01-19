# Transposition

- mirror matrix across main diagonal (upper left to bottom right)
- $\mathbf{A}^{\top}_{i, j} = \mathbf{A}_{j, i}$
- For vectors, columns -> rows, rows -> columns

# Addition, Multiplication

- works with same shape, just add element-wise

# Broadcasting

- vector is filled to form a matrix of same size
- implicit when adding vector to matrix of same dimension on one side

# Multiplying Matrices and Vectors

- matrix product is just dot product but with each vector
- element-wise product is different
- distributive
- associative
- NOT commutative for matrices, yes for vectorsA
- $(AB)^{\top} = B^{\top}A^{\top}$
- system of linear equations: $\mathbf{A}x = b$, where $x = [x_{1}, x_{2}, \dots, x_{n}]$ is a set of variables we are solving for

$$
\begin{align*}
3x + 2y + 4z = -1 \\
4y + z = 3 \\
2x + 6y + 2z = 4 \\
\end{align*}
$$
becomes 
$$
\begin{gather*}
\begin{bmatrix}
3 & 2 & 4 \\
0 & 4 & 1 \\
2 & 6 & 2
\end{bmatrix}
\begin{bmatrix}
x_{1} \\
x_{2} \\
x_{3}
\end{bmatrix}
= 
\begin{bmatrix}
-1 \\
3 \\
4
\end{bmatrix}
\end{gather*}
$$

