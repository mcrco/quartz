# Integral Formulas Recap

**Mass of a straight wire**:  
$$
\int f(x) \, dx
$$

**Mass of a curvy wire**: 
$$
\int f(x, y) \, dS 
$$

**Mass of planar lamina**: 
$$
\iint f(x,y) dA
$$

**Surface Integral**:
$$
\iint f(x, y, z) dS
$$

# Evaluating a Surface Integral

Let $S$ be a surface given by $z=g(x, y)$ and let $R$ be it sprojection onto the xy-plane. If $g,g_{x}, g_{y}$ are continuous on $R$ and $f$ is continuous on $S$, then the surface integral of $f$ over $S$ is 

$$
\iint_{S} f(x, y, z) dS = \iint_{R} f(x, y, g(x, y))\sqrt{ 1+[g_{x}(x, y)]^{2} + [g_{y}(x, y)]^{2}} dA
$$

Relationship holds true for $y=g(x, z)$ and $x = g(y, z)$, just substitute variables as needed.

# Applications

- mass of shell
- moment of inertia
- center of mass
- pressure and gravitation
- electrical charge
- [[Gauss's Law]]

# Examples

## Example 1

Evaluate the surface integral $\iint_{S} f(x, y, z) \, dS$ where S is the parabolic cylinder $y=3x^{2}$, $0 \leq x \leq 4, \, 0 \leq z \leq 4$

### Solution

Surface is in xz-plane.

$$
y= g(x, z) = 3x^{2} \\
$$
$$
\begin{align}
\iint f(x, y, z) \, dS &= \iint f(x, y, z) \cdot \sqrt{ 1 + g_{x}^{2} + g_{z}^{2} } dS \\
&= \int_{x=0}^{x=4} \int_{z=0}^{z=4} 3x \cdot \sqrt{ 1 + (6x)^{2} + 0 } \, dz  \, dx \\
&= 1539.89
\end{align}
$$

## Example 2

Evaluate $\iint_{S} (x-2y+z) dS$ where $S: z=2, \, x^{2}+ y^{2} \leq 1$

### Solution

$$
z = 2
$$
$$
\begin{align}
\iint _{S} f(x, y, z) dS &= \iint f(x, y, z) \cdot \sqrt{ 1 + g_{x}^{2} + g_{y}^{2}} \\
&= \int_{x=-1}^{x=-1} \int_{y=-\sqrt{ 1-x^{2} }}^{y=\sqrt{ 1-x^{2} }}  
(x - 2y + 2) \cdot \sqrt{ 1 + 0 + 0 } \, dy  \, dx \\
\end{align}
$$

OR

$$
\begin{align}
\iint _{S} f(x, y, z) dS &= \iint f(x, y, z) \cdot \sqrt{ 1 + g_{x}^{2} + g_{y}^{2}} \\
&= \int_{\theta=0}^{\theta=2\pi} \int_{r=0}^{r=1} (r\cos \theta - 2r\sin \theta + 2) r \, dr  \, d\theta  \\
&= 2\pi
\end{align}
$$

## Example 3

Evaluate $\iint f(x, y, z) dS$ where $f(x, y, z)=\frac{xy}{z}$, $S: z=x^{2} + y^{2}, \, 4\leq x^{2} + y^{2} \leq 16$  in Quadrant 1

### Solution

$$
\begin{align}
\iint f(x,y,z) \cdot \sqrt{ 1 + g_{x}^{2} + g_{y}^{2} } dS  
&= \int_{0}^{\frac{\pi}{2}} \int_{r=2}^{r=4} \frac{\cos \theta + \sin \theta}{r} \sqrt{ 1 + 4x^{2} + 4y^{2} } \, dr  \, d\theta  \\
&= \int_{0}^{\frac{\pi}{2}} \int_{2}^{4} \sin \theta \cos \theta \sqrt{ 1 + 4r^{2} }\, dr  \, d\theta 
&= 18.91 
\end{align}
$$

# Parameter Surface Integral

## Parametric Equation

$$
\begin{gather}
x = x(u, v) \\
y = y(u, v) \\
z = z(u, v) \\
\vec{r}(u, v) = <x(u, v), y(u, v), z(u, v)>
\end{gather}
$$

## Surface Integral w/ Parametric Surface

If S is a surface given as $\vec{r}(u,v) = <x(u,v), y(u,v), z(u,v)$ over region $D$ in the uv plane, then the surface integral of $f(x,y,z)$ over $S$ is

$$
\iint_{S} f(x,y,z) dS = \iint_{D} f(x(u, v), y(u,v), z(u,v)) \lvert \vec{r}_{u} \times \vec{r}_{v} \rvert dA
$$

# Examples

## Example 4

Use parametric surface to evaluate

$$
\iint_{S} f(x,y,z) dS, \, S: y=3x^{2}, \, 0 \leq x \leq 4, \, 0\leq z\leq 4, \, f(x,y,z) = 3x
$$

### Solution

$$
\begin{align}
x&=u \\
y&=3u^{2} \\
z&=v \\
\vec{r}(u, v)&= <u, 3u^{2}, v> \\
\end{align}
$$

$$
\begin{gather}
0 \leq u \leq 4 \\
0 \leq v \leq 4 \\
\end{gather}
$$

$$
\begin{align}
\int_{u=0}^{u=4} \int_{v=0}^{v=4} 3u | |<1, 6u, 0> \times <0, 0, 1>| | \, dv  \, du &= \int_{0}^{4} \int_{0}^{4} 3u\sqrt{ 1+36u^{2} } \, du  \, dv  \\
&= 1539.89
\end{align}
$$

## Example 5

Find $\iint_{S}(y=5)dS$ where $\vec{r}(u,v) = <u,v,2v>$, $0 \leq u \leq 1$, $0\leq v\leq u$

### Solution

$$
\begin{align}
\int_{u=0}^{u=} \int_{v=0}^{v=u} (v+5) \sqrt{ 5 } \, dv  \, du &= \frac{8\sqrt{ 5 }}{3}
\end{align}
$$