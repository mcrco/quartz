A linear/matrix transformation is just a function. However, in linear algebra we use the term transformation because a function is like moving a vector.

A linear transformation is a transformation that keeps grid of space straight and origin constant. 

# Matrix of a Transformation

The constants for vector's components in linear combination of basis vectors remain the same for linearly transformed basis vectors.

All of this means that all you need is 4 numbers to represent linear transformation: the terminal point of $\hat{i}$ and the terminal point of $\hat{j}$ after the transformation. Given that $\hat{i}$ lands at $(a,b)$ and $\hat{j}$ lands at $(c,d)$, you can then package the transformation into a 2x2 matrix: 

$$
\begin{align}
\begin{bmatrix}
a & c \\
b & d
\end{bmatrix}
\end{align}
$$

This matrix is called the **standard matrix**.

To transform any vector $(x,y)$,  you can just compute as follows:

$$
x \cdot \begin{bmatrix}
a \\
b
\end{bmatrix}
+ y \cdot \begin{bmatrix}
c \\
d
\end{bmatrix}
$$

Or in matrix-vector multiplication form:

$$
\begin{bmatrix}
a & c \\
b & d
\end{bmatrix}
\begin{bmatrix}
x \\
y
\end{bmatrix}
$$

A good example of a transformation matrix with its columns as the new basis vectors are rotation matrices.

You can use the [[Inverse of a Matrix]] to find the reversing transformation.

# One-to-one Transformation

$T: \mathbb{R}^{n} \to \mathbb{R}^{m}$ is **one-to-one** if each $\vec{b}$ in $\mathbb{R}^{m}$ is the image of at most one $\vec{x}$ in $\mathbb{R}^{n}$. In other words, every $\vec{b}$ in $\mathbb{R}^{m}$ has a preimage in $\mathbb{R}^{n}$ such that $\vec{b} = T(\vec{x})$.

Or equivalently,

$$
\mathbf{A}\vec{x} = 0
$$

has only $\vec{0}$ as the solution.

Given its transformation matrix $\mathbf{A}$, it must satisfy the condition that there are at least as many rows as columns, the columns are linearly independent, and there must be a pivot position in each column.

Also called an [[Single Variable Calculus/Functions#Injection||injective function]].

# Onto Transformations

$T: \mathbb{R}^{n} \to \mathbb{R}^{m}$ is **onto** if each $\vec{b}$ in $\mathbb{R}^{m}$ is the image of at least one $\vec{x}$ in $\mathbb{R}^{n}$. In other words, every $\vec{b}$ in $\mathbb{R}^{m}$ has a preimage in $\mathbb{R}^{n}$ such that $\vec{b} = T(\vec{x})$.

Given its transformation matrix $\mathbf{A}$, we know that the reduced form of $\mathbf{A}$ must have a pivot position in each row so that if you augment matrix $\mathbf{A}$ with a vector $\vec{b}$, there will be no constraints on the possible values of b in the rightmost column.

Also called an [[Single Variable Calculus/Functions#Surjection||onto function]].

# Example Problems for Linear Transformations

## Problem 1

$$
\mathbf{A} = \begin{pmatrix}
1 & -3 \\
3 & 5 \\
-1 & 7
\end{pmatrix}, \,
\vec{u} = \begin{pmatrix}
2 \\
-1
\end{pmatrix}, \,
\vec{b} = \begin{pmatrix}
3 \\
2 \\
-5
\end{pmatrix}, \,
\begin{pmatrix}
3 \\
2 \\
5
\end{pmatrix}
$$

**Calculate $T(\vec{u}) = \mathbf{A}\vec{u}$ 

$$
\mathbf{A} \cdot \vec{u} = \begin{pmatrix}
5 \\
1 \\
-9
\end{pmatrix}
$$

**Is $\vec{b}$ in the range of $T$? If it is, find its preimage $\vec{x}$.**

$$
\begin{align}
\mathbf{A} \cdot \vec{x} &= \vec{b} \\
\begin{pmatrix}
1 & -3 \\
3 & 5 \\
-1 & 7
\end{pmatrix} \cdot \begin{pmatrix}
x_{1} \\
x_{2}
\end{pmatrix} &= 
\begin{pmatrix}
3 \\
2 \\
-5
\end{pmatrix} \\
\end{align}
$$


$$
\begin{pmatrix}
1 & -3 & 3 \\
3 & 5 & 2 \\
-1 & 7 & -5
\end{pmatrix}
$$

$$
\begin{align}
R_{2} = R_{2} - 3R_{1}, R_{3} \to R_{1} + R_{3} &\implies \begin{pmatrix}
1 & -3 & 3 \\
0 & 14 & -7 \\
0 & 4 & -2
\end{pmatrix}  \\
R_{3} \to R_{3} - \frac{2}{7}R_{2}, R_{1} \to R_{1} + \frac{3}{4} R_{3} &\implies \begin{pmatrix}
1 & 0 & \frac{3}{2} \\
0 & 1 & -\frac{1}{2} \\
0 & 0 & 0
\end{pmatrix}
\end{align}
$$

$$
\vec{x} = \begin{pmatrix}
\frac{3}{2} \\
-\frac{1}{2}
\end{pmatrix}
$$

**Is $\vec{c}$ in the range of $T$, and find the preimage if so.**

$$
\begin{align}
\mathbf{A} \cdot \vec{x} &= \vec{c} \\
\begin{pmatrix}
1 & -3 \\
3 & 5 \\
-1 & 7
\end{pmatrix} \cdot \begin{pmatrix}
x_{1} \\
x_{2}
\end{pmatrix} &= 
\begin{pmatrix}
3 \\
2 \\
5
\end{pmatrix} \\
\end{align}
$$

$$
\begin{pmatrix}
1 & -3 & 3 \\
3 & 5 & 2 \\
-1 & 7 & -5
\end{pmatrix}
$$

These 3 equations contradict one another.

# Example Problems for Matrices

## Problem 1

Find the standard matrix A for the dilation transformation $T(\vec{x}) = 3\vec{x}, \, \vec{x} \in \mathbb{R^{2}}$


$$
\begin{align}
\vec{e}_{1} &= \begin{bmatrix}
3 \\
0
\end{bmatrix} \\
\vec{e}_{2} &= \begin{bmatrix}
0 \\
3
\end{bmatrix} \\
\mathbf{A} &= \begin{bmatrix}
3 & 0 \\
0 & 3
\end{bmatrix} \\
\end{align}
$$

## Problem 2

$T(\vec{x})$ rotates points about the origin with an angle of $\theta = \frac{-3\pi}{2}$. 

$$
\begin{align}
T(\vec{e}_{1}) &= \begin{bmatrix}
0 \\
1
\end{bmatrix} \\
T(\vec{e_{2}}) &= \begin{bmatrix}
-1 \\
0
\end{bmatrix} \\
\mathbf{A} &= \begin{bmatrix}
0 & -1 \\
1 & 0
\end{bmatrix}
\end{align}
$$

## Problem 3

Find the standard matrix for the reflection across the plane x + y + z = 1.

### Solution

The transformation can be described as subtracting the normal unit vector of the plane multiplied by 2 times the magnitude of the displacement between the the point (vector) and the plane. To find displacement, we modify the distance formula between a point and a plane to not include the absolute value sign - this gives us the position of the point relative to the plane (above or below).

$$
\begin{align}
D &= \frac{ax + by + cz + d}{\lvert \lvert \vec{n} \rvert \rvert } \\
&= \frac{x + y + z - 1}{\sqrt{ 3 }} \\
\hat{n} &= \frac{<1,1,1>}{\sqrt{ 3 }} \\
\vec{v} &\to \vec{v} - 2D \cdot \hat{n} \\
<x, y, z> &\to <x, y, z> - 2<\frac{x + y + z - 1}{3}, \dots> \\
&\to <\frac{1}{3}x - \frac{2}{3}y - \frac{2}{3}z + \frac{2}{3}, \dots> \\
\mathbf{A} &= \begin{bmatrix}
\frac{1}{3} & -\frac{2}{3} & -\frac{2}{3}  \\
-\frac{2}{3} & \frac{1}{3} & -\frac{2}{3}  \\
-\frac{2}{3} & -\frac{2}{3} & \frac{1}{3}  
\end{bmatrix} \\
\mathbf{b} &= \begin{bmatrix}
\frac{2}{3} \\
\frac{2}{3} \\
\frac{2}{3} \\
\end{bmatrix}
\end{align}
$$




