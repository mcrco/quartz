In plane $R^{2}$, $\vec{F}(x, y) =  <P(x, y), Q(x, y)> =  P \hat{i} + Q \hat{j}$

In plane $R^{3}$, $\vec{F}(x, y) =  <P(x, y, z), Q(x, y, z), R(x, y, z)> =  P \hat{i} + Q \hat{j} + R \hat{k}$

## Example 1

Sketch a vector field: $\vec{F}(x, y) = y \hat{i} - x \hat{j}$

$$
\begin{align}
\vec{F}(0, 0) &= <0, 0> \\
\vec{F}(1, 0) &= <0, -1> \\
\vec{F}(-1, 0) &= <0, 1> \\
\vec{F}(0, 1) &= <1, 0> \\
\end{align}
$$

It's a rotational field.

## Example 2

Sketch the vector field: $\vec{F} = -x \hat{i} - y \hat{j}$

$$
\begin{align}
\vec{F}(0, 0) = <0, 0>\\
\vec{F}(-1, 0) = <1, 0>\\
\vec{F}(1, 0) = <-1, 0>\\
\vec{F}(1, 1) = <-1, -1>\\
\end{align}
$$

Radial field that points to center.

# Conservative Vector Field

Conservative vector fields are basically graidents.

Given $f(x, y) = x^{2} + y^{2}$, vector field is $\vec{F} = \nabla f(x, y) = <2x, 2y>$

## Definition

A vector field $\vec{F}$  is a conservative vector field if there exists a differential function $f$ such that $\nabla f = \vec{F}$, where $f$ is a potential function

## Example 3

Given $f(x, y) = 3x^{2}y + 4xy^{2}$, find the conservative vector field.

$$
\begin{gather}
\vec{F} = \nabla f = <f_{x}, f_{y}> = <6xy + 4y^{2}, 3x^{2} + 8xy> \\
f_{xy} = 6x + 8y = f_{yx} = 6x + 8y
\end{gather}
$$

## Test for Conservative Vector Field

$\vec{F}(x, y) = P \hat{i} + Q \hat{j}$ is a conservative vector field $\iff$ their cross partial derivatives are equal.
$$
\frac{ \partial P }{ \partial y } = \frac{ \partial Q }{ \partial x } 
$$

## Example 4

Determine whether the following is conservative:

$$
\begin{align}
\vec{F}(x, y) &= 2xy \hat{i} + (2x^{2} - y) \hat{j} \\
\frac{ \partial P }{ \partial y }  &= 2x \\
\frac{ \partial Q }{ \partial x } &= 4x
\end{align}
$$

$2x \neq 4x \implies$ not conservative.

# 3-D vector fields

In $R^{3}$, if $\vec{F}(x, y, z)$ = $<P, Q, R>$ is conservative, then

$$
\begin{gather}
\frac{ \partial P }{ \partial y }  = \frac{ \partial Q }{ \partial x } , \frac{ \partial Q }{ \partial z } = \frac{ \partial R }{ \partial y } , \frac{ \partial R }{ \partial x } = \frac{ \partial P }{ \partial z } 
\end{gather}
$$

# Finding potential functions

## Example 5

Find potential function for $\vec{F}(x, y) = 2xy \hat{i} + (x^{2} - y)\hat{j}$ 

$$
\begin{gather}
\int f_{x} \, dx = \int 2xy \, dx \implies f(x, y) = x^{2}y + g(y) \\
\int f_{y} \, dy = \int x^{2} - y \, dy \implies f(x, y) = x^{2}y - \frac{y^{2}}{2} + h(x) \\
\implies g(y) = \frac{y^{2}}{2}, C = h(x)\\
\implies f(x, y) = x^{2} - \frac{y^{2}}{2} + c \\
\end{gather}
$$

We can also use partial derivative of final answer and see if we get original field to check our answer.

## Example 6

Find potential function of $\vec{F}(x, y) = <4x - y, 6y - x>$

$$
\begin{gather}
\int f_{x} \, dx = \int 4x - y \, dx = 2x^{2} - xy + g(y) \\
\int f_{y} \, dy = \int 6y - x \, dy = 3y^{2} - xy + h(x) \\
\implies g(y) = 3y^{2}, h(x) = 2x^{2} \\
\implies 2x^{2} + 3y^{2} - xy + C
\end{gather}
$$