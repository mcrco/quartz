**Eigenvectors** of a matrix are vectors that remain within their original [[Linear Combinations and Span|span]] after the [[Linear Transformations|linear transformation]] represented by the matrix. **Eigenvalues** are the factors by which the eigenvectors are scaled.

One example use case is finding the eigenvector of a 3-D rotation, which is the axis of rotation. 

# Representation

The representation of eigenvectors and eigenvalues are as shown below

$$
\mathbf{A}\vec{v} = \lambda \vec{v},
$$

where $\mathbf{A}$ is the transformation, $\vec{v}$ is the eigenvector, and $\lambda$ is the eigenvalue. This should intuitively make sense: after applying a linear transformation to an eigenvector using matrix vector multiplication, the resulting vector should be a scalar multiple of the eigenvector, by a factor of the eigenvalue.

# Computation

To solve for the above, we must first convert both sides to matrix vector multiplication. We can multiply the right hand side by the identity matrix and then equate as follows

$$
(\mathbf{A} - \lambda \mathbf{I})\vec{v} = 0
$$

Since the eigenvector is non-zero, we must have the whole product equal to 0. The only time this happens is in a matrix vector multiplication, which can also be viewed as a [[Linear Transformations|linear transformation]], is when the [[Determinants|determinant]] of the matrix/linear transformation is 0. Solving as said,

$$
\begin{align}
\det \left( \mathbf{A} - \lambda \mathbf{I} \right) &= 0 \\
\det \left( \begin{bmatrix}
a - \lambda & b \\
c & d - \lambda
\end{bmatrix} \right) &= 0 \\
(a - \lambda)(d - \lambda) - bc &= 0
\end{align}
$$

We can then solve for the eigenvalue as a normal quadratic polynomial.

# Eigenbasis

When the basis vectors are eigenvectors of a transformation, the corresponding matrix is a diagonal matrix of the eigenvectors. 

Diagonal matrices are easy to work with - applying the same transformation n times is just scaling each coordinate by the eigenvalue to the power of n. That's why you should try to convert matrices into an eigenbasis system before taking its power.