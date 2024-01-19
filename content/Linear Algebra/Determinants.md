# Geometric Intuition

One good way of measuring [[Linear Transformations|linear transformations]] is with how the area of a given region changes. You can think of the determinant of a matrix as a measure of the linear transformation the matrix represents.

When a linear transformation is applied to the space, every region in the space changes area by the same factor, called the **determinant**. For example, if a transformation increases every area by 3, its determinant 3

If a [[Linear Transformations|linear transformation]] transforms the area of a region into 0, then the determinant must be 0. This is a special case and has applications, such as when calculating [[Eigenvectors and Eigenvalues|eigenvectors and eigenvalues]]. We can visualize this linear transformation as squishing a grid into a lower dimension

If the orientation of space is inverted, then determinant is negative. You can use RH/LH rule to verify change in orientation.

Above properties are for 2-D but apply to 3D as well. 

# Calculation

The determinant of a $2\times 2$ matrix is calculated as follows:

$$
\det \left( \begin{bmatrix}
a & b \\
c & d
\end{bmatrix} \right)
= ad - bc
$$

## Laplace's Expansion

For larger matrices, such as 

$$
A = \begin{pmatrix}
2 & 0 & 0 & 1 & 3 \\
0 & 4 & 0 & 5 & 0 \\
1 & 0 & -1 & 0 & 0 \\
0 & 0 & 0 & 2 & 1 \\
4 & 1 & 0 & 0 & -2
\end{pmatrix}
$$

we use Laplace's Expansion. Laplace's Expansion states that the definition of the determinant of a matrix is 

$$
\det A = \sum_{i=1}^{n} (-1)^{i + 1}a_{i_{1}}
$$

$$
\begin{align}
\det(A) &= 1 \cdot \det(\begin{pmatrix}
0 & 0 & 1 & 3 \\
4 & 0 & 5 & 0 \\
0 & 0 & 2 & 1 \\
1 & 0 & 0 & -2
\end{pmatrix}) -1\cdot \det(\begin{pmatrix}
2 & 0 & 1 & 3 \\
0 & 4 & 5 & 0 \\
0 & 0 & 2 & 1 \\
4 & 1 & 0 & -2
\end{pmatrix}) \\
&= 0 - 2\det \begin{pmatrix}
2 & 0 & 3 \\
0 & 4 & 0 \\
4 & 1 & -2
\end{pmatrix} + \det \begin{pmatrix}
2 & 0 & 1 \\
0 & 4 & 5 \\
4 & 1 & 0
\end{pmatrix} \\
&= -2 \cdot 4\det \begin{pmatrix}
2 & 3 \\
4 & -2
\end{pmatrix} + 2\det \begin{pmatrix}
4 & 5 \\
1 & 0
\end{pmatrix} + \det \begin{pmatrix}
0 & 4 \\
4 & 1
\end{pmatrix} \\
&= 128 -10+-16 \\
&= 102
\end{align}
$$

## Triangle Method

If we have a matrix with an upper or lower triangle (upper triangle shown below)

$$
A \to \begin{pmatrix}
2 & 0 & 0 & 1 & 3 \\
0 & 4 & 0 & 5 & 0 \\
0 & 0 & -1 & -\frac{1}{2} & -\frac{3}{2} \\
0 & 0 & 0 & 2 & 1 \\
0 & 0 & 0 & 0 & -\frac{51}{8}
\end{pmatrix}
$$

Then, multiplying along the diagonal and by the determinants of any elementary matrices used in converting to row echelon form: 

$$
\det A = 102
$$

This is just an extension of Laplace's Expansion.

# Determinant of Matrix Product

The determinant the product of two matrices is just the product of their determinants.

$$
\det(AB) = \det A \cdot \det B
$$

## Proof

To prove it, we must start with proving the above property for elementary matrices.

### Row Swapping

The formula for the determinant of a row-swapping elementary matrix $\mathbf{E}$ by a matrix $\mathbf{A}$ is 

$$
-\det \mathbf{A}
$$

Our lord and savior Chris Ge provides both an informal and formal proof. Since I hate collared shirts, the informal proof is as follows:

1. Swapping adjacent rows -> determinant is multiplied by -1 (Laplace's Expansion)
2. Swapping two non-adjacent rows $i$ and $j$ is the same as making $2(j - i) - 1$ swaps -> determinant is multiplied by -1.

### Row Multiplication

Given an elementary matrix $\mathbf{E}$ that multiplies a row of a matrix $\mathbf{A}$ by a factor $c$, the determinant of $\mathbf{EA}$ is 

$$
c\det \mathbf{A}
$$

or equivalently

$$
\det \mathbf{C}\det \mathbf{A}
$$

We know that the determinant of $\mathbf{C}$ is just $c$ by the [[#Triangle Method]].

The proof for this formula is pretty intuitive; if you use Laplace's Expansion along the row of $\mathbf{A}$ that was scaled by the factor $c$, then the determinant is naturally going to be multiplied by $\frac{1}{c}$.

### Row Addition/Subtraction

Given an elementary matrix $\mathbf{E}$ that performs row addition within a matrix $\mathbf{A}$, the determinant of $\mathbf{EA}$ is just 

$$
\det \mathbf{A}
$$

or equivalently

$$
\det \mathbf{E} \det \mathbf{A}
$$

This is because the determinant, according to Laplace's Expansion, is a linear function of the rows and columns of the matrix. Therefore, adding rows to each other means that they cancel out eventually. 

Here's an example. Let 

$$
\mathbf{A} = \begin{bmatrix}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33}
\end{bmatrix}
$$

The determinant is 

$$
\det \mathbf{A} = a_{11}(a_{22}a_{33} - a_{23}a_{32}) - a_{12}(a_{21}a_{33} - a_{23}a_{31}) + a_{13}(a_{21}a_{32} - a_{22}a_{31})
$$

Now, if we add two of $R_{1}$ to $R_{2}$, 

$$
\mathbf{A} = \begin{bmatrix}
a_{11} & a_{12} & a_{13} \\
a_{21} + 2a_{11} & a_{22} + 2a_{12} & a_{23} + 2a_{13} \\
a_{31} & a_{32} & a_{33}
\end{bmatrix}
$$

The determinant is 

$$
\begin{align}
\det \mathbf{A} &= a_{11}((a_{22} + 2a_{12})a_{33} - (a_{23} + 2a_{13})a_{32}) \\
&- a_{12}((a_{21} + 2a_{11})a_{33} - (a_{23} + 2a_{13})a_{31})  \\
&+ a_{13}((a_{21} + 2a_{11})a_{32} - (a_{22}+2a_{13})a_{31}) \\
&= a_{11}(a_{22}a_{33} - a_{23}a_{32}) - a_{12}(a_{21}a_{33} - a_{23}a_{31}) + a_{13}(a_{21}a_{32} - a_{22}a_{31})
\end{align}
$$

Thus ending our proof.

### Combining Elementary Matrices

Now that we have our above lemmas, we can just combine them all to say that for any matrices $\mathbf{A}$ and $\mathbf{B}$, as long as one of them are [[Inverse of a Matrix|invertible]], 

$$
\det \mathbf{AB} = \det \mathbf{A}\det \mathbf{B}
$$

This is because invertible matrices can be written as the product of a series of elementary matrices, allowing us to expand out the determinant of the product as a product of many determinants of elementary matrices.

$$
\begin{align}
\det \mathbf{AB} &= \det(\mathbf{E}_{1}\mathbf{E}_{2}\dots \mathbf{E}_{n}\mathbf{B}) \\
&= \det \mathbf{E}_{1}\det \mathbf{E}_{2}\dots \det \mathbf{E}_{n}\det \mathbf{B}
\end{align}
$$

# Properties


1. If $A$ is invertible
$$
\det A^{-1} = \frac{1}{\det A}
$$

2. If one row of $A$ is a multiple of another row, then

$$
\det A = 0
$$

3. If A has a row or column of all zeroes, then

$$
\det A = 0
$$

4. If $\det A = 0$, then $A$ is not invertible



