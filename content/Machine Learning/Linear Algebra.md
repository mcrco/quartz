# Matrices, Vectors, Scalars, Tensors

## Scalars
- single number
- lowercase character, like $x$

## Vectors
- array
- points in space
- bold lower case, like $\mathbf{x}$

## Matrices
- 2-D array
- bold uppercase, like $\mathbf{X}$

## Tensors
- 3+ dimensions

## Matrix Operations

### Transposition
- mirror matrix across main diagonal (upper left to bottom right)
- $\mathbf{A}^{\top}_{i, j} = \mathbf{A}_{j, i}$
- For vectors, columns -> rows, rows -> columns

### Addition, Multiplication
- works with same shape, just add element-wise

### Broadcasting
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

# Identity and Inverse Matrices

- used to solve for system of linear equations
- identity matrix is square matrix with main diagonal having all 0s
	- multiplying by vector returns original vector
- matrix inverse: $\mathbf{A}^{-1}\mathbf{A} = I_{n}$

Using matrix inverses to solve for $\mathbf{A}x = b$ 
$$
\begin{align*}
\mathbf{A}x &= b\\
\mathbf{A}^{-1}Ax &= \mathbf{A}^{-1}b\\
x &= \mathbf{A}^{-1}b
\end{align*}
$$
$\mathbf{A}^{-1}$ should be used mainly as a theoretical tool, not a computer application.

# Linear Dependence and Span

- $\mathbf{A}x = b$ has exactly one solution => $A^{-1}$ exists 
- 

# Norms

- size of a vector
- $L_{p}$ norm: $| |x| | = \left( \sum_{i} |x_{i}|^{p}\right)^{\frac{1}{p}}$
- conditions
	- $f(x) = 0 \implies x = 0$
	- $f(x+y) \leq f(x) + f(y)$
	- $\forall \alpha \in \mathbb{R}, f(\alpha x) = |\alpha|f(x)$
- $L_{2}$ norm is Euclidean norm
- squared $L_{2}$ is easier to work with b/c derivative is easy to calculate
- $L^{2}$ norm increases slowly near origin -> sometimes undesirable -> use of $L_{1}$ norm
- $L^{\infty} = \text{max}_{i}|x_{i}|$ 

# Eigendecomposition

Prime factorization -> integers as eigendecomposition.
Eigenvector $v$ for matrix $\mathbf{A}$ satisfies $\mathbf{A}\mathbf{v} = \lambda \mathbf{v}$, , $\lambda$ is the eigenvalue.
$s\mathbf{v}$ is also an eigenvector and has the same eigenvalue.
Multiple linearly dependent eigenvectors -> $\mathbf{A}$ is decomposed as follows:
$$
\mathbf{A} = \mathbf{V} diag(\mathbf{\lambda}) \mathbf{V}^{-1}
$$
where $\mathbf{V}$ is the concatenated matrix of all eigenvectors and $\lambda$ is the concatenated vector of all eigenvalues.

