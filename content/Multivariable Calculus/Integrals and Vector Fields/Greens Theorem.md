Applies to [[Line Integrals]]

# Theorem

Let R be a simply connected region with piecewise smooth curves C, oriented counterclockwise.

$$
\oint M dx + Ndy = \iint \left( \frac{ \partial N }{ \partial x } - \frac{ \partial M }{ \partial y }  \right) dA, M = fx, N = fy
$$

# Examples

## Example 1

Use Green's Theorem to find the line integral

$$
\oint_{C} x^{3}dx + xydy
$$
for C is $(0, 0) \to (1, 0) \to (1, 1)$

### Solution

$$
\begin{align}
S &= \int_{x=0}^{x=1} \int_{y=0}^{y=x} (y - 0) \, dy  \, dx \\
&= \frac{x^{3}}{6} | _{0}^{1}  \\
&= \frac{1}{6}
\end{align}
$$

## Example 2

Use Green's theorem to find line integral  of 

$$
\oint x^{2}y + x^{3}dx + 2xydy
$$
where path is the region bounded by $y=x$, $y=x^{3}$

### Solution

$$
\begin{align}
S &= \int_{x=0}^{x=1} \int_{y=x^{3}}^{y=x} (2y - x^{2}) \, dy  \, dx \\
&= \int_{0}^{1} x^{2}-x^{6}-x^{3}+x^{5} \, dx \\
&= 0.1074
\end{align}
$$

## Example 3

Use Green's theortem to find work done by force $\vec{F}$ on particle moving counterclockwise around the closed path $C: r=2\cos \theta$
$$
\vec{F} = (e^{x} - 3y)\hat{i} + (e^{y}+ 6x)\hat{j}
$$

### Solution

$$
\begin{align}
W &= \oint \vec{F} dr \\ 
&= \iint_{R} f_{yx} - f_{xy} dA \\
&= \int_{\theta=0}^{\theta=\pi} \int_{r=0}^{r=2\cos \theta} (6-(-3)) 
r \, dr  \, d\theta  \\
&= 9\pi
\end{align}
$$