Extension of [[Line Integrals]].

Recall $\vec{F}$ is a conservative vector field iff $\vec{F}=\nabla f$ for some function f.

If $\vec{F}$ is a conservative vector field, the path is indpendent -- it doesn't matter which path we move from a to b because the same amount of wokr is done

# Fundamental Theorem of Calculus Part 1

$$
\begin{align}
\int_{a}^{b} f(x) \, dx &= F(x)|_{b}^{a} 
= F(b) - F(a)
\end{align}
$$

For some $f(x, y, z)$

$$
\vec{F} = \nabla f = <f_{x}, f_{y}, f_{z}>
$$

# Fundamental Theorem of Line Integral

$$
\begin{align}
W &= \int_{a}^{b} \vec{F} \, dr = \int_{a}^{b} \nabla f \, dr = f(x, y, z) \mid _{a}^{b} \\
&= f(b) - f(a) 
\end{align}
$$

Note: Line integral of conservative vector field can be done without knowing the path $\vec{r}(t)$

# Examples

## Example 1

Find the work done by the vector field 

$$
\vec{F}(x, y) = <xe^{2y}, x^{2}e^{2y}> \text{from } (0, 0) \to (-1, 1)
$$

### Solution

#### First Option

Test if conservative:
$$
\begin{align}
f_{xy} = 2xe^{2y} \\
f_{yx} = 2xe^{2y}
\end{align}
$$
Find potential function:

$$
\begin{align}
f(x, y) &= \int xe^{2y} \, dx = \frac{x^{2}}{2}e^{2y} + g(y)  \\
&= \int x^{2}e^{2y} \, dy = \frac{x^{2}}{2}e^{2y} + g(x) \\
&\implies f(x, y) = \frac{x^{2}}{2}e^{2y} + C
\end{align}
$$

Apply fundamental theorem of Line Integrals:

$$
\begin{align}
W &= \int \nabla f \, dr  \\
&= f(x, y)|_{(0, 0)}^{(-1, 1)} \\
&= \frac{x^{2}}{2}e^{2y} + C|_{(0, 0)}^{(-1, 1)}  \\
&= \frac{1}{2}e^{2}
\end{align}
$$

#### Second Option

Find the path from $\vec{r}(t)$ from $(0, 0) \to (-1, 1)$:

Since we know it's conservative, we can assume that vector is linear

$$
\begin{align}
\vec{r}(t) &= <-t, t> \\
\vec{r}'(t) &= <-1, 1> \\
W &= \int_{0}^{1} \vec{F}(t) \cdot \vec{r}'(t) \, dt  \\
&= \int_{0}^{1} te^{2t} + t^{2}e^{2t} \, dt \\
&= 3.695 
\end{align}
$$

# Equivalent Condition

iF $\vec{F} = <P, Q, R>$ have first partial derivative on an open connected region $R$, and $C$ is piecewise smoth curve then the following are true:

1. $\vec{F}$ is conservative iff $\nabla f = \vec{F}$ for some $f$
2. $\int _{C} \vec{F}$ is independent path
3. $\int _{C}\vec{F} \, dr = \vec{0}$ for every closed curve C in R