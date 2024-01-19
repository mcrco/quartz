For a particle moving counterclockwise around the closed path f $\vec{F}$ is a vector field containing surface S, then $\vec{F}$ describes the velocity of the flow or fluid at any point across the surface.

The volume of fluid (amount of flow) crossing the surface S per unit of time is called flux of F across S.

**Flux:**
$$
\iint_{S} \vec{F}\cdot \vec{N}dS
$$

where $\vec{F}= <P,Q,R>$ and $\vec{N}$ is unit normal across $S$.

If a fluid has mass density $\rho(x,y,z)$ at a point then flux is`

$$
\iint_{S}\rho \cdot \vec{F}\cdot \vec{N}dS
$$

For $\vec{F} = <P, Q, R>$  and $S$ be surface $z=g(x,y)$, $R$ is its projection on xy plane.

Flux: $\iint\vec{F}\cdot\vec{N} dS = \vec{F}$ 

$z = g(x,y)$

upward oriented: $z - g(x,y) = 0$ => Level curve $G(x,y,z)$
$$
\begin{align}
\vec{N} = \nabla G = <-g_{x}, -g_{y}, 1> \\
\iint\vec{F} \cdot \frac{<-g_{x}, -g_{y}, 1>}{\sqrt{ g_{x}^2 + g_{y}^{2} + 1}} \cdot \sqrt{ g_{x}^{2} + g_{y}^{2} + 1} \, dA &= \iint \vec{F} \cdot <-g_{x}, -g_{y}, 1> dA
\end{align}
$$


downward oriented: $z - g(x,y) = 0$ => Level curve $G(x,y,z)$
$$
\begin{align}
\vec{N} = \nabla G = <-g_{x}, -g_{y}, -1> \\
\iint\vec{F} \cdot \frac{<-g_{x}, -g_{y}, -1>}{\sqrt{ g_{x}^2 + g_{y}^{2} + 1}} \cdot \sqrt{ g_{x}^{2} + g_{y}^{2} + 1} \, dA &= \iint \vec{F} \cdot <-g_{x}, -g_{y}, -1> dA
\end{align}
$$

# Examples

## Example 1

Find the flux of $\vec{F}$ across S where $\vec{N}$ is upward-oriented.

$$
\begin{gather}
\vec{F} = <x, 2y> \\
s: z = 6 - 3x - y
\end{gather}
$$

### Solution

$$
\begin{align}
\iint \vec{F} \cdot <-g_{x}, -g_{y}, 1> dA &= \iint <x, 2y> \cdot <3, 1, 1> \, dx \, dy \\
y = 6 - 3x &\implies 0 \leq x \leq 2, \, 0 \leq y \leq 6 - 3x \\
&= \int_{x=0}^{x=2} \int_{y=0}^{y-6-3x} 3x + 2y \, dy  \, dx \\
&= 36 
\end{align}
$$