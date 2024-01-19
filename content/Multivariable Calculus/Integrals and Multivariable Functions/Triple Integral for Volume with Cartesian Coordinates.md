# Recap

To find area under curve (2D):
$$
\int_{a}^{b} f(x) \, dx 
$$
To find mass of thin wire (1D):
$$
\int_{a}^{b} \rho(x) \, dx 
$$
To find volume under the surface $f(x, y)$ (3D):
$$
\iint f(x, y) \ dA
$$
Mass of a thin plate (2D):
$$
\iint \rho(x) \ dA
$$
Area of the bounded region (2D):
$$
\iint 1 \ dA
$$
Measurement under $f(x, y, z)$ (4D):
$$
\iiint f(x, y, z) \ dV
$$
Mass of 3D region:
$$
\iiint \rho(x, y, z) \ dV
$$
Volume of bounded region (3D):
$$
\iiint 1 \ dV
$$

# Volume bounded in 3D with functions

$$
\int_{x=a}^{x=b} \int_{y=g_{1}(x)}^{y=g_{2}(x)} \int_{z=f_{1}(x, y)}^{z=f_{2}(x, y)} f(x, y, z) \, dV
$$

## Example 1

Find $\iiint xy \, dV$ where $Q$ is a tetrahedron in the first octant bounded by $2x + 3y + z = 6$.

$$
\begin{align*}
z = 6 - 2x - 3y\\
0 \leq z \leq 6 - 2x - 3y \\
0 \leq x \leq 3\\
0 \leq y \leq -\frac{2}{3}x + 2 \\
\int_{x = 0}^{x = 3} \int_{y}^{y = -2/3 x + 2 } \int_{z = 0}^{z = 6-2x-3y} xy \, dz  \, dy  \, dx  \\
\int_{x = 0}^{x = 3} \int_{y}^{y = -2/3 x + 2 } xy(6-2x-3y) \, dy  \, dx 
\end{align*}
$$

## Example 2

Set up triple integral to find the mass of the $Q$ region: $y = x^{3}, y=x, z \leq 2x, z \geq 0$ and the mass density given as $\rho (x, y, z) = 2z$

$$
\int_{0}^{1} \int_{y = x^{3}}^{y = x} \int_{z = 0}^{z = 2x} 2z \, dz  \, dy  \, dx 
$$

## Example 3

Set up triple integral to find the volume of the region $Q$ bounded by $x - 4-y, x + z = 4, x= 0, z = 0$

$$
\begin{align*}
0 \leq z \leq -x + 4\\
z = 0 \implies x = 4, x = 4-y^{2}, x = 0 \\
-2 \leq y \leq 2\\
0 \leq x \leq 4-y^2\\
\\
\int_{y = -2}^{y = 2} \int_{x = 0}^{x = 4 - y^{2}} \int_{z = 0}^{z = -x + 4}  \, dz  \, dx   \, dy
\end{align*}
$$

## Example 4

Find $\int_{0}^{3} \int_{x=0}^{x=\sqrt{ 9 - y^{2} }} \int_{z=0}^{z=9-x^{2}-y^{2}} 4xye^{x^{2}} \, dz \, dx \, dy$ 

First change the order of integration
$$
\begin{align}
z &= 0 \to z = 9 - x^{2} - y^{2}\\
x &= 0 \to x = \sqrt{ 9 - y^{2} - z^{2} } \\
0 \leq x \leq \sqrt{ 9 - y^{2} - z} \\
0 \leq z \leq \sqrt{ 9 - y^{2} } \\
0 \leq y \leq 3 \\
\end{align}

$$
$$
\begin{align}
\int_{y = 0}^{y = 3} \int_{z = 0}^{z = 9-y^{2}} \int_{x = 0}^{x = \sqrt{ 9-y^{2}-z }} 4xye^{x^{2}} \, dx  \, dz  \, dy \\
&= \int_{y = 0}^{y = 3} \int_{z = 0}^{z = 9-y^{2}} [2ye^{x^{2}}] _{0}^{\sqrt{ 9-x^{2}-z }} \, dz  \, dy \\
&= \int_{y = 0}^{y = 3} \int_{z = 0}^{z = 9-y^{2}} (2ye^{9-x^{2}-z} - 2y) \, dz  \, dy \\
&= \int_{0}^{3} [-2ye^{9-x^{2}-z} - 2yz] _{0}^{9-y^{2}} \, dx  \\
\end{align}
$$
# Cartesian coordinate system is too hard?

Use [[Triple Integral with Cylindrical and Spherical Coordinates]]!