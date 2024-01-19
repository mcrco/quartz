# Dot Product

The dot product or scalar product is the index wise multiplication of two vectors, denoted by the syntax below

$$
\vec{u} \cdot \vec{v}
$$

# Cross Product

The cross product of two vectors produces a third vector that is orthogonal to the originals, and is denoted as shown below

$$
\vec{u} \times \vec{v}
$$

# Angles

With Law of Cosines, we can prove
$$
\vec{u}\cdot \vec{v} = \lvert \vec{u} \rvert \lvert \vec{v} \rvert \cos \theta
$$
Using Law of Sines, we can prove
$$
\lvert \lvert \vec{u} \times \vec{v} \rvert \rvert = \lvert \lvert u \rvert \rvert \lvert \lvert \vec{v} \rvert \rvert \sin \theta
$$

# Component

$$
comp_{\vec{u}}\vec{v} = \frac{\vec{u}\cdot \vec{v} }{\lvert \lvert u \rvert \rvert}
$$

Component is the magnitude of one vector along another, so to find it we can just multiply the magnitude of the projected vector by the sine of the angle between the two vectors. 

$$
\begin{align}
comp_{\vec{u}}\vec{v} &= \lvert \lvert \vec{v} \rvert \rvert \cdot \cos \theta \\
&= \lvert \lvert \vec{v} \rvert \rvert \cdot \frac{\vec{u} \cdot \vec{v}}{\lvert \lvert \vec{u} \rvert \rvert \lvert \lvert \vec{v} \rvert \rvert } \\
&= \frac{\vec{u}\cdot \vec{v}}{\lvert \lvert \vec{u} \rvert \rvert }
\end{align}
$$

# Projection

$$
proj_{\vec{u}}\vec{v} = \vec{u} \frac{\vec{u}\cdot \vec{v}}{\lvert \lvert u \rvert \rvert ^{2}}
$$

Since the projection is like the component (but the vector), we can just multiply the component expression by the unit vector of vector being projected onto.

$$
\begin{align}
proj_{\vec{u}}\vec{v} &= \frac{\vec{u}}{\lvert \lvert \vec{u} \rvert \rvert } \cdot comp_{\vec{u}}\vec{v} \\
&= \vec{u} \frac{\vec{u}\cdot \vec{v}}{\lvert \lvert \vec{u} \rvert \rvert ^{2}}
\end{align}
$$

# Area of Parallelogram

$$
A = \lvert \lvert \vec{u} \times \vec{v} \rvert \rvert
$$

The formula for the area of a parallelogram is 
$$
A = bh
$$

Expressed in terms of the length and width, we get
$$
A = ab\sin \theta
$$
where $\theta$ is the angle between the two sides.

Combining this information with vectors and cross products, we get that for two vectors $\vec{u}$ and $\vec{v}$, the area of the parallelogram formed by them is 
$$
\begin{align}
A &= \lvert \lvert \vec{u} \rvert \rvert \lvert \lvert \vec{v} \rvert \rvert \frac{\lvert \lvert \vec{u}\times \vec{v} \rvert \rvert }{\lvert \lvert \vec{u} \rvert \rvert \lvert \lvert \vec{v} \rvert \rvert }\\
&= \lvert \lvert \vec{u} \times \vec{v} \rvert \rvert
\end{align}
$$

# Volume of Parallelpiped

$$
V = \lvert \lvert (\vec{a} \times \vec{b}) \cdot \vec{c} \rvert \rvert,
$$

where $\vec{a}, \vec{b}, \vec{c}$ form the parallelpiped

We know that the volume of a parallelpiped is the product of the area of the base (formed by $\vec{a}$ and $\vec{b}$) and the height, we can plug in a few values we already know:

$$
V = \lvert \lvert \vec{a} \times \vec{b} \rvert \rvert (\lvert \lvert \vec{c} \rvert \rvert \cos \phi)
$$

where $\phi$ is the angle between vector $\vec{c}$ and the height of the parallelpiped. 

The height of the parallelpiped can also be written as the component of $\vec{c}$ onto the orthogonal vector of $\vec{a}$ and $\vec{b}$, which is $\vec{a} \times \vec{b}$. $\cos \phi$ can also be rewritten in terms of dot products and magnitudes of the vectors.

We can now rewrite the volume again:

$$
\begin{align}
V &= \lvert \lvert \vec{a} \times \vec{b} \rvert \rvert \lvert \lvert \vec{c} \rvert \rvert \frac{(\vec{a} \times \vec{b}) \cdot \vec{c}}{\lvert \lvert \vec{a}\times \vec{b} \rvert \rvert \lvert \lvert \vec{c} \rvert \rvert } \\
&= (\vec{a} \times \vec{b}) \cdot \vec{c}
\end{align}
$$


# Modeling Space

Dot products are cross products are essential to calculations of relationships between vectors/[[Vector Fields]] such as those in [[Flux Integral]], [[Curl and Divergence]], [[Line Integrals]], and more.

## Line

A line can be expressed in parametric form as a point on the line, $P$, a vector $v$, and a scalar $t$.

$$
L = P + t\vec{v}
$$

## Plane

A plane can be expressed as a 