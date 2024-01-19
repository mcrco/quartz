# Cylindrical Volume

$$
\int_{\theta_{1}}^{\theta_{2}} \int_{r_{1}}^{r_{2}} \int_{z_{1}}^{z_{2}} f(r\cos \theta, r\sin \theta, z) \, dz  \, dr  \, d\theta 
$$

## Example 1
Find $\int \int \int y \, dV$ where Q bounded by $z = 4-x^{2}-y^{2}$ in the first octant $x=0, y=0, z=0$

$$
\begin{align}
0 \leq z \leq 4-r^{2} \\
0 \leq r \leq 2 \\
0 \leq \theta \leq \frac{\pi}{2}\\

\int_{0}^{\pi} \int_{0}^{2} \int_{0}^{4-r^{2}} r\sin (\theta) r \, dz  \, dr  \, d\theta &= \int_{0}^{\pi} \int_{0}^{2} \int_{0}^{4-r^{2}} r^{2} sin (\theta) \, dz  \, dr  \, d\theta  \\
&= 4.27

\end{align}
$$

## Example 2
Set up $\int \int xy \,dV$ using cylindrical cordinates where $Q: {x, y, z} | x^{2} + y^{2} \leq 1, x \geq 1, y \leq x, -1 \leq z \leq 1$ 

$$
\begin{align}
\int_{-\frac{\pi}{2}}^{\frac{\pi}{4}} \int_{0}^{1} \int_{-1}^{1} r^{3}\sin \theta\cos \theta \, dz  \, dr  \, d\theta 
\end{align}
$$

# Triple Integral Using Spherical Coordinates

Coordinates: $(\rho, \theta, \phi)$
$$
\begin{gather}
r = \rho \sin \phi \\
x = r\cos \theta = \rho \sin \phi \cos \theta\\
y = r\sin \theta = \rho \sin \phi \sin \theta\\
z = \rho \cos \phi
\end{gather}
$$
Volume:
$$
\begin{gather}
\iiint f(\rho, \theta, \phi) \rho^{2} \sin \phi d\rho d\phi d\theta
\end{gather}
$$

## Example 1

Find $\iiint \sqrt{ x^{2} + y^{2} + z^{2} } dV$, bounded by $x^{2} + y^{2} + z^{2} \leq 1$

$$
\begin{gather}
\rho = x^{2} + y^{2} + z^{2} \implies \rho \leq 1\\
0 \leq \phi \leq \pi \\
0 \leq \theta \leq 2\pi
\end{gather}
$$
$$
\begin{align}
V &= \int_{0}^{2\pi} \int_{\phi = 0}^{\phi = \pi} \int_{\rho = 0}^{\rho = 1} \rho \cdot \rho^{2} \sin \phi \, d\phi  \, d\phi  \, d\theta \\
&= \int_{0}^{2\pi} \int_{\phi = 0}^{\phi = \pi} \int_{\rho = 0}^{\rho = 1} \rho^{3} \sin \phi \, d\rho  \, d\phi  \, d\theta \\
&= \int_{0}^{2\pi} \int_{\phi = 0}^{\phi = \pi} \frac{1}{4} \sin \phi \, \, d\phi  \, d\theta \\
&= \int_{0}^{2\pi} \frac{1}{2}  \, d\theta \\
&= \pi
\end{align}
$$

## Example 2

Use spherical and cylindrical to find the volume of the solid region Q bounded by upper napped of the cone $z^{2} = x^{2} + y^{2}$ above by the sphere $x^{2} + y^{2} + z^{2} = 9$

### Spherical
$$
\begin{gather}
\rho^{2} = 9 \implies \rho = 3\\
x^{2} = z^{2} - y^{2}, x^{2} = 9 - (y^{2} + z^{2}) \implies 2z^{2} = 9 \implies z = \frac{3}{\sqrt{ 2 }} \\
\rho \cos \phi = \frac{3}{\sqrt{ 2 }} \to \phi = \frac{\pi}{4} \\
\end{gather}
$$

Bounds:
$$
\begin{gather}
0 \leq \rho \leq 3 \\
0 \leq \phi \leq \frac{\pi}{4} \\
0 \leq \theta \leq 2\pi
\end{gather}
$$
$$
\begin{align}
V &= \int_{\theta = 0}^{\theta = 2\pi}  \int_{\phi = 0}^{\phi = \pi/4} \int_{\rho = 0}^{\rho = 3} 1 \cdot \rho^{2} \sin \phi \, d\rho  \, d\phi  \, d\theta \\
&= \int_{\theta = 0}^{\theta = 2\pi}  \int_{\phi = 0}^{\phi = \pi/4} 9 \sin \phi \, \, d\phi  \, d\theta \\
&= \int_{\theta = 0}^{\theta = 2\pi}  \left( -\frac{9\sqrt{ 2 }}{2} + 9 \right) \, \, d\theta \\
&= 18\pi - 9\sqrt{ 2\pi }
\end{align}
$$

### Cylindrical

#### Bounds
$$
\begin{gather}
z = \sqrt{ x^{2} +y^{2} } \implies r \leq z \\
z = \sqrt{ 9 - x^{2} -y^{2} } \implies z \leq \sqrt{ 0 - r^{2} }\\
2r^{2} = 9 \implies r = \frac{3}{\sqrt{ 2 }} \\
\end{gather}
$$

#### Volume
$$
\begin{align}
V &= \int_{\theta=0}^{\theta=2\pi} \int_{r=0}^{r=3/\sqrt{ 2 }} \int_{r}^{\sqrt{ 9-r^{2} }} 1\cdot r \, dz  \, dr  \, d\theta   \\
&= 18\pi - 9\sqrt{ 2\pi }
\end{align}
$$

## Example 3

Find the volume of the region outside the cylinder $x^{2} + y^{2} = 1$ and inside the sphere $x^{2} + y^{2} + z^{2} = 4$.

#### Bounds

$$
\begin{gather}
r^{2} = 1, \, \rho^{2} = 4  \implies \frac{1}{\sin \phi} \leq \rho \leq 2\\
r^{2} = 1, \, r^{2} + (\rho \cos \phi)^{2} = 4 \implies \phi = \frac{\pi}{6}, \, \frac{5\pi}{6} \\
0 \leq \theta \leq \frac{5\pi}{6}
\end{gather}
$$

### Volume
$$
\begin{align}
V &= \int_{\theta = 0}^{\theta = 2\pi} \int_{\phi = \pi/6}^{\phi = 5\pi/6} \int_{\rho = \csc \theta}^{\rho = 2} 1 \cdot \rho^{2}\sin \phi \, d\rho  \, d\phi  \, d\theta  \\
&= \int_{\theta = 0}^{\theta = 2\pi} \int_{\phi = \pi/6}^{\phi = 5\pi/6} \frac{8}{3} - \csc^3 \theta \, d\phi  \, d\theta  \\
\end{align}
$$
# Bounds are Bad?

Then change them! [[Changing Bounds for Integrals with the Jacobian]]
