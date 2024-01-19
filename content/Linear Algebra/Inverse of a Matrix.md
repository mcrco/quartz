# Definition

A $n\times n$ matrix is invertible if there is an $n\times n$ matrix $\mathbf{C}$  such that $\mathbf{C}\mathbf{A} = \mathbf{I}$ **and** $\mathbf{A}\mathbf{C} = \mathbf{I}$, where $\mathbf{I}$ is a $n\times n$ identity matrix.

# Finding the Inverse

## Row Operations

We can use the product of **elementary matrices** to find the inverse of a matrix. Elementary matrices are matrices that can be derived from the identity matrix with one step.

### Example

Find the inverse of $\mathbf{A}$

$$
\begin{align}
A &= \begin{pmatrix}
4 & 0 & 5 \\
0 & 3 & 0 \\
1 & 0 & 4
\end{pmatrix}  \\
E_{1} = \begin{pmatrix}
\frac{1}{4} & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix} \to
A &= \begin{pmatrix}
1 & 0 & \frac{5}{4} \\
0 & 3 & 0 \\
1 & 0 & 4
\end{pmatrix}  \\
E_{2} = \begin{pmatrix}
1 & 0 & 0 \\
0 & \frac{1}{3} & 0 \\
0 & 0 & 1
\end{pmatrix} \to
A &= \begin{pmatrix}
1 & 0 & \frac{5}{4} \\
0 & 1 & 0 \\
1 & 0 & 4
\end{pmatrix}  \\
E_{3} = \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
-1 & 0 & 1
\end{pmatrix} \to
A &= \begin{pmatrix}
1 & 0 & \frac{5}{4} \\
0 & 1 & 0 \\
0 & 0 & 4
\end{pmatrix}  \\
E_{4} = \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
-1 & 0 & 1
\end{pmatrix} \to
A &= \begin{pmatrix}
1 & 0 & \frac{5}{4} \\
0 & 1 & 0 \\
0 & 0 & \frac{11}{4}
\end{pmatrix} \\
E_{5} = \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & \frac{4}{11}
\end{pmatrix} \to A &= \begin{pmatrix}
1 & 0 & \frac{5}{4} \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix} \\
E_{6} = \begin{pmatrix}
1 & 0 & -\frac{5}{4} \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix} \to A &= \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix} \\
A^{-1} = E_{1}E_{2}E_{3}E_{4}E_{5}E_{6}
\end{align}
$$

## Adjugate Matrix

The inverse of a matrix $\mathbf{A}$ in terms of the [[Determinants|determinant]] and its [[Adjugate Matrix|adjugate matrix]] is

$$
\mathbf{A}^{-1} = \frac{1}{\det \mathbf{A}}adj(\mathbf{A})
$$

### Example

$$
\begin{align}
adj(\mathbf{A}) &= 
\begin{pmatrix}
2 & 1 & 3 \\
1 & -1 & 1 \\
1 & 4 & -2
\end{pmatrix} \\
&= \begin{pmatrix}
-2 & 3 & 5 \\
14 & -7 & -7 \\
4 & 1 & -3
\end{pmatrix} ^{T} \\
&= \begin{pmatrix}
-2 & 14 & 4 \\
3 & -7 & 1 \\
5 & -7 & -3
\end{pmatrix} \\
\det \mathbf{A} &= 2\cdot -2 + 1 \cdot 3 + 3 \cdot 5 \\
&= 14 \\
\mathbf{A}^{-1} &= \frac{1}{14} \begin{pmatrix}
-2 & 14 & 4 \\
3 & -7 & 1 \\
5 & -7 & -3
\end{pmatrix} \\
&= \begin{pmatrix}
-\frac{1}{7} & 1 & \frac{2}{7} \\
\frac{3}{14} & -\frac{1}{2} & \frac{1}{14} \\
\frac{5}{14} & -\frac{1}{2} & -\frac{3}{14}
\end{pmatrix}
\end{align}
$$

# Properties

## Theorem 1

$$
(\mathbf{A}\mathbf{B})^{-1} = \mathbf{B}^{-1} \cdot \mathbf{A}^{-1}
$$


## Theorem 2

Given Theorem 1, we can use an [[Proofs#Proof By Induction|inductive proof]] to show that given that $A_{1}, A_{2}, A_{3} \dots A_{n}$ are invertible matrices,

$$
(A_{1} \cdot A_{2} \cdot A_{3} \dots A_{n}) ^{-1} = A_{n}^{-1} \cdot A_{n - 1}^{-1} \dots A_{1}^{-1}
$$

Base case: n = 2

The theorem literally states this is true

Inductive step: 

Let $A = (A_{1} \cdot A_{2} \dots A_{n})$, $B = A_{n + 1}$

$$
\begin{align}
(A_{1} \cdot A_{2} \dots A_{n+1})^{-1} &= (A \cdot B)^{-1} \\
&= B^{-1} \cdot A^{-1} \\
&= A_{n + 1}^{-1} \cdot A_{n}^{-1} \cdot A_{n - 1}^{-1} \dots A_{1}
\end{align}
$$

$S(n+ 1)$ holds true given $S(n)$ is true.