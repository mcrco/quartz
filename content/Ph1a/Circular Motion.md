# Earth's Orbit

![['Earth Orbit.jpg]]

Earth has uniform circular motion. We will use the above scenario for all of our derivations below.

# Position

We define the radius vector of Earth relative to the sun


$$
\vec{r}(t) = (x(t), y(t))
$$

or 

$$
\vec{r}(t) = (r\cos\omega t, r\sin\omega t)
$$

where 

$$
\omega t = \theta(t).
$$

The period is

$$
T = \frac{2\pi}{\omega}
$$


# Velocity

To find velocity,

$$
\vec{v} = \frac{d\vec{r}}{dt} = (-r\omega \sin \omega t, r\omega \cos\omega t)
$$

Note that $\vec{v}\cdot \vec{r} = 0$, meaning velocity and radius are perpendicular.

$$
v = \sqrt{ |\vec{v}|^{2} } = \sqrt{ r^{2}\omega^{2}(\cos ^{2}\omega t + \sin ^{2}\omega t) } = \omega r
$$

This means speed, angular frequency, and radius are related independent of time.

# Acceleration

$$
\vec{a} = \frac{d\vec{v}}{dt}=(-r\omega^{2}\cos\omega t, -r\omega^{2}\sin\omega t) = -\omega^{2}\vec{r}
$$

Note that acceleration and radius are antiparallel.

# Force

$$
\vec{F}_{\text{centripetal}} = m\vec{a} = -m\omega^{2}\vec{r}
$$

Let 

$$
\begin{gather}
\vec{r} = r\hat{r} \\
\hat{r} = \frac{\vec{r}}{r}
\end{gather}
$$

$\hat{r}$ is called the unit vector of $\vec{r}$.

We can rewrite 

$$
\vec{F}_{\text{centripetal}} = -(m\omega^{2}r)\hat{r} = -\left( \frac{mv^{2}}{r} \right)\hat{r}.
$$

# Example: Two Masses through Hole in Table

Consider.

![[Pasted image 20231011114206.png]]

Then,

$$
\begin{gather}
m_{2}g=m_{1}\omega^{2}r \\
r = \frac{m_{2}g}{m_{1}}\frac{1}{\omega^{2}} = \frac{m_{2}g}{m_{1}}\left( \frac{T}{2\pi} \right)^{2} \\
\implies r \propto T^{2}.
\end{gather}
$$

This relationship is one of Kepler's Laws.

# Example: Earth (again)

Assuming Earth's orbit ~ uniform circular motion.

$$
\begin{gather}
\vec{F}_{\text{centripetal}} = \vec{F}_{g} \\
-m\omega^{2}r\hat{r} = -\left( \frac{GmM}{r^{2}} \right)\hat{r} \\
r^{3} = \frac{GM}{\omega^{2}} = GM\left( \frac{T}{2\pi} \right)^{2} \\
\implies r^{3} \propto T^{2}.
\end{gather}
$$

also,

$$
T^{2} \propto \frac{r^{3}}{G}
$$

means farther out $\implies$ period longer, weaker gravity $\implies$ period longer. 

If you hypothetically had asteroids parallel to Earth, then they would not move in sync because farther out means slower.

However, there are Lagrange Points, for which asteroids would move in sync to Earth. This is because if asteroid and Earth are aligned with sun, the increased gravity between asteroid and Earth will increase $\vec{F}_{\text{centripetal}}$.

Another conjecture about how Moon formed: some massive body collided with Earth, debris became moon.