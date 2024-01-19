# Definition of Divergence
$$
\begin{align}
\text{div} \vec{F} &= \nabla \vec{F}\\
&= <\frac{ \partial  }{ \partial x }, \frac{ \partial  }{ \partial y }  > \cdot <P, Q> \\
&= \frac{ \partial P }{ \partial x } + \frac{ \partial Q }{ \partial y } 
\end{align}
$$

If $\text{div}\vec{F} = 0$, $\vec{F}$ is divergence free.

In fluid motion, divergence free vector fields are "incompressible."

In E&M, divergence free vector field is called "solenoidal."

# Definition of Curl

$$
\begin{align}
\vec{F} &= <P, Q, R> \\
\text{curl}\vec{F} &= \nabla \vec{F} \\
&= \begin{vmatrix}
\frac{ \partial  }{ \partial x }  & \frac{ \partial  }{ \partial y }  & \frac{ \partial  }{ \partial z }  \\
P & Q & R
\end{vmatrix}
\end{align}
$$

## Example 1

$\vec{F} = e^{x} \hat{i} + yz\hat{j} - yz^{2} \hat{k}$

a. Find divergence of $\vec{F}$ at (0, 2, -1)

$$
\begin{align}
\text{div} F &= \frac{ \partial }{ \partial x } [e^{x}] + \frac{ \partial }{ \partial y } yz + \frac{ \partial }{ \partial z } [-yz^{2}]  \\ \\
\text{div} \vec{F}(0, 2, -1) &= e^{0} - 1 - 2(2)(-1) = 4 \\
&= 4
\end{align}
$$

b. Find the curl of $\vec{F}$

$$
\begin{align}
\text{curl} \vec{F} &= \begin{vmatrix}
\hat{i} & \hat{j} & \hat{k} \\
\frac{ \partial  }{ \partial x }  & \frac{ \partial }{ \partial y }  & \frac{ \partial }{ \partial z }  \\
e^{x}  & yz & -yz^{2}
\end{vmatrix} \\
&= (-z^{2}-y)\hat{i}  \\
&\neq 0 \\
\end{align}
$$

## Example 2

Find potential function of $\vec{F} = <e^{z}y, \, e^{z}x, \, e^{z}>$

$$
\begin{align}
\text{curl}\vec{F} &= \begin{vmatrix}
\hat{i} & \hat{j} & \hat{k} \\
\frac{ \partial }{ \partial x }  & \frac{ \partial }{ \partial y }  & \frac{ \partial }{ \partial z }  \\
e^{z}y & e^{z}x & e^{z}
\end{vmatrix} \\
&= <-e^{z}x, e^{z}y, 0> \\
&\neq \vec{0}
\end{align}
$$

F is not conservative.

## Example 3

Find the potential function of $\vec{F}(x, y, z) = <\frac{1}{y}, -\frac{x}{y^{2}}, i$

$$
\begin{align}
f(x, y, z) &= \int \frac{1}{y} \, dx = \frac{x}{y} + g(y, z) \\
&= \int \frac{-x}{y^{2}} \, dy = \frac{x}{y} + h(x, z)  \\
&= \int 2z \, d
\end{align}
$$