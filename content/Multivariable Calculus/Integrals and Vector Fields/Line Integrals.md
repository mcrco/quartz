# Derivation for 3D Surface Area

![[Pasted image 20221207225239.png]]

The formula for the surface area is

$$
A = \int_{a}^{b} f(x, y) \, dS
$$

We know that 

$$
\begin{align}
dS &= \sqrt{ (dx)^{2} + (dy)^{2} } \\
&= \frac{1}{dt}\sqrt{ (dx)^{2} + (dy)^{2} }dt \\
&= \sqrt{ \left( \frac{dx}{dt} \right)^{2} + \left( \frac{dy}{dt} \right)^{2} }dt
\end{align}
$$

So the final surface area formula becomes

$$
\begin{align}
A &= \int_{a}^{b} f(x, y) \sqrt{ \left( \frac{dx}{dt} \right)^{2} + \left( \frac{dy}{dt} \right)^{2} } \, dt  \\
&= \int_{a}^{b} f(x(t), y(t)) \mid\mid r(t)\mid\mid \, dt 
\end{align}
$$

# Uses

- calculate area of curvy sheet with given height
- measure mass of wire
- work done of particle moving in the force field

# Examples

## Example 1

Evaluate the line intergal $\int _{C} \frac{x + y + z}{5} \, ds$ and C is the curve $\vec{r}(t) = <4t, 8\cos\frac{3}{8}t, 8\sin\frac{3}{8}t, 0 \leq t \leq \frac{8\pi}{3}$

$$
\begin{align}
r'(t) &= <4, -3\sin\frac{3}{8}t, 3\cos\frac{3}{8}t> \\
\mid\mid r'(t)\mid\mid &= 5 \\
I &= \int_{0}^{\frac{8\pi}{3}} + \frac{4t + 8\cos\frac{3}{8}t + 8\sin\frac{3}{8}t}{5}5 \, dt = 183.03  
\end{align}
$$

## Example 2

Find mass of wire that lies along the curve $\vec{r}(t) = (\frac{\sqrt{ 7 }}{2}t^{2} - 4)\hat{i} + 3t\hat{j}, \, 0\leq t\leq 1, \, \rho=4t$ 

$$
\begin{align}
r'(t) &= <\sqrt{ t }, 3> \\
| | r'(t) | | &= \sqrt{ 7t^{2} + 9 } \\
M &= \int_{0}^{1} 4t\sqrt{ 7t^{2}+9 } \, dt = 7.05 
\end{align}
$$

## Example 3

Evaluate $\int _{C} (y+z) \, ds$ where $C = (0, 0, 0) \to (4, 4, 1)$
given $C_{1}: r(t) = 4t^{2}\hat{i} + 4t\hat{j}, 0 \leq t \leq 1$ and $C_{2}: r(t) = 4\hat{i} + 4\hat{j} + (t-1) \hat{k}$

### Path 1

$$
\begin{align}
r'(t) &= <8t, 4> \\
S &= \int_{0}^{1} 4t \sqrt{ 64t^{2} + 16 } \, dt \\
&=  
\end{align}
$$

### Path 2

$$
\begin{align}
r'(t) &= <0, 0, 1> \implies | | r'(t) | | = 1 \\
S &= \int_{1}^{2} (3 + t) 1 \, dt \\
&=  
\end{align}
$$

# Line Integral with Vector Field

## Uses

For $\vec{F}(x, y, z)$ represent a force field on on particle and $\vec{r}(t) = <x(t), y(t), z(t)>$ at $a \leq t \leq b$.

The work done is 

$$
\begin{align}
W &= \int _{C} \vec{F} \cdot \vec{T} \, dr \\
&= \int _{C} \vec{F} \frac{\vec{r}'(t)}{\mid \vec{r}'(t) \mid} |\vec{r}'(t)| \, dt \\
&= \int _{C} \vec{F} \, dr  
\end{align}
$$

# Examples

## Example 4

Find the work done by $\vec{F}$ over the curve in the direction of increasing $t$.
$$
\vec{F} = -8z\hat{i} + 8x\hat{j} + 3y\hat{k}, \, 0 \leq t \leq 1, \, \vec{r}(t) = <t, t, t>
$$
Solution:

$$
\begin{align}
\vec{r}'(t) &= <1, 1, 1> \\
\vec{F}(t) &= <-8t, 8t, 3t> \\
W &= \int_{0}^{1} (-8t + 8t + 3t) \cdot 1 \, dt \\
&= \frac{3}{2}
\end{align}
$$

## Example 5

Find the line integral of $\int _{C} 2xy \, ds$ where $C$ is the segment $(-2, 1)$ to $(1, 3)$

Solution:

Setting arbitrary values for $t$, @ $t=0$ C is @ $(-2, 1)$, @ $t=1$ C @ $(1, 3)$

Using equation of lines:

$$
\begin{align}
x &= a_{1}t - 2 \implies a_{1} = 3\\
y&= a_{2}t+1 \implies a_{2} = 2\\
\vec{r}(t) &= <3t - 2, 2t + 1> \\
S &= \int_{0}^{1} 2(3t-2)(2t+1)\cdot \sqrt{ 13 } \, dt \\
&= -\sqrt{ 13 }
\end{align}
$$

## Example 6

Find the line intergral $\int x^{2} \, ds$ where C is the curve.

$$
$$

Solution:


let $x = t$
$$
\begin{align}
\vec{r}(t) = <t, t^{2}+1>\\

\end{align}
$$