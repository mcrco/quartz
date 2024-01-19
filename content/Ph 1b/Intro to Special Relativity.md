# Reference Frames

- for event at $(x_{0},y_{0},z_{0},t_{0})$
- let $y'=y, z'=z, t'=t, x'=x-vt$ for moving frame denoted by '
- then, we can **relate** stuff like distances ($r,r'$) or forces $F, F'$ using $x',y',t'$ aka relative motion
- reality is same for both observers, just relatively transformed

# Special Relativity Postulates

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"_index":0}] Axiom 1.
> All inertial frames are equally valid - laws of physics are the same, no preferred frame.

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"title":"","label":"","_index":1}] Axiom 2.
> Speed of light $c$ is the same in all frames regardless of relative motion of source and observer.

> [!math|{"type":"remark","number":"auto","setAsNoteMathLink":false,"_index":2}] Remark 3.
> $c$ is the speed at which massless things move - essentially a speed limit of nature. Since we measure events in terms of space and time, $c$ is simply a conversion factor between space and time.

## Significance

- reference frame from [[#Reference Frames]] is broken!
- light moves at same speed for both observers; thus, **relative** motion is broken, realities are different
- $\gamma = \frac{1}{\sqrt{ 1-\frac{v^{2}}{c^{2}} }}$ indicates how impactful relativity is

# Implications

- time dilation
- length contraction
- simultaneity is relative
- intervals: $\Delta r$ and $\Delta t$ are "mixed"
- velocity transformation
- kinematics implications ($E,p,m$)

# Time Dilation

![[Pasted image 20240104115806.png]]

- to the astronaut, the time taken for light to pulse back and forth from the source to the mirror to the receiver is $\frac{2D}{c}$
- to the observer on earth, the light moves at an angle but still at speed $c$; thus, the time taken for light to pulse is $\frac{2s}{c}$
- **time is dilated**

$$
\begin{align}
\Delta t_{\text{between ship's light clock ticks to earth}} &= \frac{2D}{\sqrt{ c^{2}-V^{2} }} \\
\end{align}
$$
$$
t_{\text{moving clock}} = t_{\text{stationary clock}} \sqrt{ 1-V^{2} / c^{2} }
$$

# Length Contraction

![28.3: Length Contraction - Physics LibreTexts](https://phys.libretexts.org/@api/deki/files/3414/Figure_29_03_03a.jpg?revision=1&size=bestfit&width=666&height=436)

- to stationary observers earth and alpha centauri, time runs slower on the spaceship according to time dilation
- to the observer on the spaceship, length contraction occurs because $L=VT=V\cdot \frac{T}{\gamma}<L_{0}$

## Horizontal Light Clock

Imagine a horizontal light clock moving at $v$.

When the light moves forward, clock moves forward:

$$
\Delta T_{1} = \frac{V\Delta T_{1} + \frac{D}{\gamma}}{c}.
$$

When light moves backward, 

$$
\Delta T_{2} = \frac{-V\Delta T_{2} + \frac{D}{\gamma}}{c}.
$$

Full trip:

$$
T = \frac{2D}{c}\gamma
$$

# Simultaneity

If you have two clocks moving together at $v$ and signal is emitted at center, leading clock lags by

$$
\Delta t = \frac{vD}{c^{2}}
$$
