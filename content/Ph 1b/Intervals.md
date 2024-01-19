- $(ct,x,y,z)$: location in spacetime (event)

$$
\Delta s^{2}=-(c\Delta t)^{2}+(\Delta x)^{2}+(\Delta y)^{2}+(\Delta z)^{2}
$$

- if only $x$, can visualize events $A,B,C,D,E$ as

![[Pasted image 20240111115723.png]]

- $C-D$: $\Delta s^{2}=0 \implies$ null
- $A-B$: $\Delta s^{2}>0 \implies$ time-like
- $C-D$: $\Delta s^{2}<0 \implies$ space-like

- insert cone diagram

# 4-vector

- can represent event as

$$
\tilde{x} = (ct,x,y,z)=(x_{0},x_{1},x_{2},x_{3})
$$

- or

$$
x_{\mu}, \, u=\{ 0,1,2,3 \}
$$

- or 

$$
A_{\mu}=(A_{0},A_{1},A_{2},A_{3})
$$
- the magnitude is invariant

$$
|\tilde{A}|^{2}=-A_{0}^{2} + A_{1}^{2} + A_{2}^{2} + A_{3}^{2} \to \text{invariant}
$$

- and so is the dot product

$$
\tilde{A} \cdot \tilde{B}.
$$

## Scalars in Special Relativity

- mass
- proper time $\tau$
- velocity
	- $\frac{d}{dt}\tilde{x}$ is frame dependent because of $dt$
	- so instead

$$
\frac{\Delta \tilde{x}}{\Delta \tau} \to \lim_{ \Delta \tau \to 0 } \frac{\Delta \tilde{x}}{\Delta \tau} \to \frac{d\tilde{x}}{d\tau}=\tilde{v}
$$

- so

$$
\tilde{v}=\left( c \frac{dt}{d\tau}, \frac{dx}{d\tau},\dots \right)
$$

- since $\frac{dt}{d\tau}=\gamma$,

$$
\tilde{v}=(c\gamma, v_{x}\gamma, \dots)
$$

- what is $|\tilde{v}|$?
- value is invariant, so we can choose the moving object's frame
- $\implies$ $v_{x}=v_{y}=v_{z}=0 \implies \gamma=1$
- $\tilde{v}=(c,0,0,0) \to |\tilde{v}|^{2}=-c^{2}$
- $\implies$ always moving through spacetime at $c$; if at rest, moving through spacetime at $c$, if moving spatially, move through time slower and space faster.

# 4-momentum

$$
\tilde{p}=m\tilde{v}
$$

- $m$ is rest mass of object

$$
\begin{align}
\vec{p}&=(p_{1},p_{2},p_{3}) \\
&= m\tilde{v} \\
&= m\vec{v}\gamma
\end{align}
$$

- $p_{0}=mc\gamma$
- $E_{0}=p_{0}c=mc^{2}\gamma$
- $KE=E_{0}-mc^{2}=mc^{2}(\gamma-1)$
	- limit $v \ll c$, $\beta\ll 1$
	- so
- $KE \approx mc^{2}(\frac{1}{\sqrt{ 1-\beta^{2} }}-1)=\frac{1}{2}mc^{2}\beta^{2}$
- if $v\to c$, $|\vec{p}|,E_{0}\to \infty$
- we know $\tilde{p}=(mc\gamma,mv_{x}\mathbf{\gamma},\dots)$
- so

$$
\begin{align}
|\tilde{p}|^{2}&=-(mc\gamma)^{2} + (m\vec{v}\gamma)^{2} \\
&= -(mc)^{2}\gamma^{2} + m^{2}|\vec{v}|^{2}\gamma^{2} \\
&= -m^{2}g^{2}(c^{2}+1) \\
&= \frac{|\tilde{p}|^{2}}{c^{2}}=-m^{2} \\
\implies E^{2} &= p^{2} + m^{2}
\end{align}
$$