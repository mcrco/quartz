# Changing Variables in Integrals
$$
\begin{gather}
\int_{a}^{b} f(x) \, dx \\
x = g(u) \implies dx = g'(u)du\\
\int f(g(u)) g'(u) \, du 
\end{gather}
$$
## Definition of Jacobian:
$$
\begin{gather}
\iint f(x, y) \, dx \, dy
\end{gather}
$$
If $x = g(u, v)$ and $y = h(u, v)$ then the Jacobian of $x, y$ with respect to $u, v$ is 
$$
\begin{gather}
J = \frac{ \partial (x, y) }{ \partial (u, v) }  = 
\begin{pmatrix}
\frac{ \partial x }{ \partial u }  & \frac{ \partial y }{ \partial v }  \\
\frac{ \partial y }{ \partial u }  & \frac{ \partial y }{ \partial v } 
\end{pmatrix}
\end{gather}
$$

## Rectangular transformation

$$
\begin{gather}
\iint f(x, y) \, dA \to \iint f(g(u, v), h(u, v)) |J|  \, du dv
\end{gather}
$$

## Polar Transformation

$$
\begin{gather}
x = r\cos \theta, \, y = r\sin \theta \\
J = \begin{pmatrix}
\frac{ \partial x }{ \partial r }  & \frac{ \partial x }{ \partial \theta }  \\
\frac{ \partial y }{ \partial r }  & \frac{ \partial y }{ \partial \theta }  \\
\end{pmatrix} = \begin{pmatrix}
\cos \theta  & -\sin \theta \\
\sin \theta & \cos \theta
\end{pmatrix}
\end{gather}
$$

Basically converting [[Triple Integral for Volume with Cartesian Coordinates]] with [[Triple Integral with Cylindrical and Spherical Coordinates]]!

# Examples

## Example 1

Find the Jacobian and use teh transformation to evaluate $\iint_{R} x^{2} - y^{2} dxdy$ where R is the region bounded by $y = -x + 2, \, y = x - 4, \, y = x + 4, \, y = -x + 4$ given $u = x + y, \,\, v = x -y$

### Change region:
$$
\begin{gather}
y = -x + 2 \implies x + y = 2 \implies u = 2 \\
y = -x - 4 \implies x + y = 4 \implies u = -4 \\
y = x - 4 \implies x - y = 4 \implies v = 4 \\
y = x + 4 \implies x - y = -4 \implies v=  -4\\
f(x, y) = x^{2} - y^{2} \implies f(u, v) = uv\\
u = x + y, v = x - y \implies x = \frac{u + v}{2}, \, y = \frac{u - v}{2}\\
J = \begin{pmatrix}
\frac{1}{2}  & \frac{1}{2} \\
\frac{1}{2}  & -\frac{1}{2}
\end{pmatrix} \implies |J| = \frac{1}{2}
\end{gather}
$$
### Area:
$$
\begin{align}
A &= \int_{u = -4}^{u = 2} \int_{v = -4}^{v = 4} u\cdot v\cdot\frac{1}{2} \, dv  \, du 
\end{align}
$$


## Example 2

FInd $\iint \sqrt{ 1 - \frac{x^{2}}{4} - \frac{y^{2}}{9} } dA$ wehre R is the region bounded by $\frac{x^{2}}{4} + \frac{y^{2}}{9} = 1$

### Change Region

$$
\begin{gather}
u = \frac{x}{2}, \, v = \frac{y}{3} \implies u^{2} + v^{2} = 1 \\
\end{gather}
$$

### Jacobian

$$
\begin{gather}
J = \begin{pmatrix}
2 & 0 \\
0 & 3
\end{pmatrix} \implies |J| = 6
\end{gather}
$$

### Volume

$$
\begin{gather}
\int_{\theta=0}^{\theta=2\pi} \int_{r=0}^{r=1} \sqrt{ 1-r^{2} } \, 6 \cdot r \, dr  \, d\theta 
\end{gather}
$$