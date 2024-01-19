- [[Circuits#Current|electric currents]] create magnetic fields.
- units are **teslas**

# Right Hand Rule

![[Pasted image 20230325192351.png|center]]

# 3 Properties

1. covers all points around current carrying wire
2. vector
3. exerts forces on magnetic poles

# Magnetic Fields from Moving Charges

![[Pasted image 20230325204844.png|center]]

## Biot-Savart Law

- basically Coulomb's law for $\vec{B}$
- $\mu_{0}$ is permeability constant

$$
\vec{B}_{\text{point charge}} = \frac{\mu_{0}qv\sin \theta}{4\pi r^{2}}
$$

# Magnetic Field of a Current

![[Pasted image 20230325205428.png|center]]

## Biot-Savart Law

Using the Biot-Savart Law for a moving charge, we rewrite it in terms of many moving charges (current).

$$
\begin{align}
\vec{B} &= \int \frac{\mu_{0}v\sin \theta}{4\pi r^{2}} \, dq \\
&= \int \frac{\mu_{0}\sin \theta}{4\pi r^{2}}\frac{dl}{dt} \, dq \\
&= \int \frac{\mu_{0}\sin \theta}{4\pi r^{2}}I \, dl   \\
&= \frac{\mu_{0}}{4\pi}I\int \frac{x}{r} \cdot \frac{1}{r^{2}} \, dl  \\
&= \frac{\mu_{0}}{4\pi}I\int \frac{x}{\sqrt{ x^{2}+l^{2} }} \cdot \frac{1}{x^{2}+l^{2}} \, dl \\
&= \frac{\mu_{0}}{4\pi}Ix\int_{-\infty}^{\infty} \frac{1}{(x^{2}+l^{2})^{\frac{3}{2}}} \, dl \\
&= \frac{\mu_{0}Ix}{4\pi}
\end{align}
$$