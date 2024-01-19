Solving for the electric field of a single particle is simple, but solving for the electric field with space is more challenging. To do this, we must enclose the space in a Gaussian shape and then use Gauss's Law.

Gauss's Law states that the [[Flux Integral|electric flux through a closed surface]] $\propto$ the charge enclosed within that surface.

$$
\phi_{E} = \oint \vec{E} d\vec{A} = \frac{Q_{enc}}{\epsilon_{0}}
$$

# Uniform Charge Density

## Electric Field Outside of Object

To demonstrate Gauss's Law in this situation, we take a cylinder with radius $R$, height $L$, and charge $Q$. 

$$
\begin{align}
\phi = \oint \vec{E} d\vec{A} &= \frac{Q_{enc}}{\epsilon_{0}} \\
\implies \vec{E} \cdot 2\pi rL &= \frac{Q}{\epsilon_{0}} \\
\implies \vec{E} &= \frac{Q}{2\pi rL\epsilon_{0}}
\end{align}
$$

This holds true for both conductors and non-conductors.

## Electric Field Inside Object

### Conductors

Conductors have an internal electric field of 0.

### Non-Conductors

For this, we need the density of the charge, $\rho$. 

$$
\begin{align}
\vec{E} \cdot 2\pi rL &= \frac{Q_{enc}}{\epsilon_{0}} \\
\rho &= \frac{Q_{enc}}{V_{enc}} = \frac{Q}{V} \\
\implies \frac{Q}{\pi R^{2}L} 
&= \frac{Q_{enc}}{\pi r^{2}L} \\
\implies Q_{enc} &= \frac{Qr^{2}}{R^{2}} \\
\implies \vec{E} &= \frac{Qr}{2\pi R^{2}L\epsilon_{0}}
\end{align}
$$

# Nonuniform Density

## Electric Field Outside Object

### Conductors and Non-Conductors

Gauss's Law states that 

$$
\vec{E} 2\pi rL = \frac{Q_{enc}}{\epsilon_{0}}
$$

Given the same cylinder dimensions and $\rho = -Cr$, we solve for $Q_{enc}$.

$$
\begin{align}
Q_{enc} &= \int_{0}^{L} \, dz \cdot \int_{0}^{R} -Cr \cdot r \, dr \int_{0}^{2\pi}  \, d\theta  \\
&= 2\pi L \left[ \frac{-Cr^{3}}{r} \right]_{0}^{R} \\
&= -\frac{2C\pi LR^{3}}{3}
\end{align}
$$

Plugging back into Gauss's Law:

$$
\begin{align}
\vec{E}_{out} \cdot 2\pi rL &= -\frac{2C\pi LR^{3}}{3\epsilon_{0}} \\
\implies \vec{E}_{out} &= \frac{-CR^{3}}{3r\epsilon_{0}}\hat{i}
\end{align}
$$

