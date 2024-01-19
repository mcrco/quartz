The electric field of a particle with charge $Q$ is

$$
\vec{E} = \frac{kQ}{r^{2}}
$$

because

$$
\vec{F}_{e} = \frac{kqQ}{r^{2}} = q\vec{E} \implies \vec{E} = \frac{kQ}{r^{2}}
$$

# Visualization

Given a positive source and a negative sink, we can visualize the electric field as follows:

![[electric field.png]]

# Electric Flux

Given an electric field around a particle with charge $Q$, the electric flux is calculated with the formula

$$
\phi_{electric} = \frac{Q}{\epsilon_{0}} = \vec{E}dA,
$$

where $\epsilon_{0}$ is the permittivity of the space around the particle (how well space stores electrical energy), $A$ is the surface area. This formula is [[Gauss's Law]].

Since the magnetic field is a sphere, 

$$
\begin{align}
dA &= R^{2} \int_{0}^{\pi} \sin \theta \, d\theta \int_{0}^{2\pi} \phi \, d\phi \\
&= 4\pi R^{2} \\
\vec{E}dA &= \vec{E} \cdot 4\pi R^{2} \\
\implies \vec{E}\cdot 4\pi R^{2} &= \frac{Q}{\epsilon_{0}} \\
\implies \vec{E} &= \frac{kQ}{r^{2}},
\end{align}
$$

deriving $k$ to be $\frac{4\pi}{\epsilon_{0}}$.

# Kinematics/Dynamics

## Velocity

We can apply kinematics to a charged particle in an electric field to find its velocity.

$$
\begin{align}
F = ma &= qE \implies a = \frac{qE}{m} \\
v_{f}^{2} &= v_{i}^{2} + 2ad, \, v_{i} = 0 \\
v_{f} &= \sqrt{ \frac{2qEd}{m} }
\end{align}
$$

## Path of Charged Particles in Field

Diagram: 
![[particle passing through sandwiched field.png | center]]

Kinematics:
$$
$$

## Dipoles

![[dipole torque in electric field.png|center]]

In the above diagram, the charged particles create a torque in the electric field.

$$
\begin{align}
\tau &= \frac{d}{2}qE + \frac{d}{2}qE\\
&= qEd\sin \theta
\end{align}
$$

# Solving Field for Different Shapes

## Rod

![[rod electric field.png|center]]

Since the y components of the electric field cancel out due to vertical symmetry, we only need to solve for 

$$
\begin{align}
E &= \int dE_{x} \\
&= \int \frac{k}{r^{2}} \cos \theta \, dq
\end{align}
$$

Given that 

$$
\begin{align}
r &= \sqrt{ x^{2} + y^{2} } \\
\cos \theta &= \frac{x}{r} = \frac{x}{\sqrt{ x^{2} + y^{2} }} \\
\lambda = \frac{Q}{L} = \frac{dq}{dy} \implies dq &= \frac{Q}{L}dy
\end{align}
$$

We can rewrite our integral for the electric field as

$$
\begin{align}
E &= \int \frac{k}{(\sqrt{ x^{2}+y^{2} })^{2}} \cdot \frac{x}{\sqrt{ x^{2}+y^{2} }} \cdot \frac{Q}{L} \,dy  \\
&= \frac{kQx}{L} \int_{-\frac{L}{2}}^{\frac{L}{2}} \frac{dy}{(x^{2}+y^{2})^{\frac{3}{2}}} \\
&= \frac{kQ}{x\sqrt{ x^{2}+\frac{L^{2}}{4} }} 
\end{align}
$$

We can verify that this answer works by taking the limit of the expression as $L \to 0$.

$$
\lim_{ L \to 0 } \vec{E} = \frac{kQ}{x^{2}}
$$

This makes sense because as the length of a rod approaches 0, it is simply a point, and we have rederived the expression for the electric field of a point charge.

# Electric Field Within Shapes

To solve for electric fields within shapes, we must use [[Gauss's Law]].