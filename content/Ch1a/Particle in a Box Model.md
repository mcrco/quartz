Simple but important model that develops physical understanding of chemical applications of quantum mechanics.

# One-Dimensional Boxes

- simplest model problem for which [[Quantum Mechanics#Schrodinger's Equation]] can be solved
- particle confined by potential energy barriers with infinite potential energy
	- particle only exists in certain region of box
	- one dimension $\implies$ bead slides along wire between barriers at ends of wires
 
![[Pasted image 20231122214950.png]]

- potential energy inside box is $V(x)=0$, thus
- total energy must be $E = T+V > 0$ inside box
- we can use these constraints to solve for all possible energy levels $E$

Since it's impossible to find particle outside of box, 

$$
P(x) = \psi^{2}(x) = 0 \implies \psi(x) = 0.
$$

Inside the box, $V=0$, so Schrodinger's equation becomes

$$
-\frac{h^{2}}{8\pi^{2}m} \frac{d^{2}\psi(x)}{dx^{2}} = E\psi(x).
$$

The LHS is usually simplified with the Hamiltonian operator $\hat{H}$, which gives us the classic

$$
\hat{H}\psi = E\psi.
$$

Back to the previous equation: we can simplify it to become

$$
\frac{d^{2}\psi(x)}{dx^{2}} = -\frac{8\pi^{2}mE}{h^{2}}\psi(x).
$$

^a2e8ff

Since this is a [[Linear Differential Equation]] and our boundary conditions are that $\psi(0)=\psi(L)=0$, we know that 

$$
\psi(x)=A\sin kx.
$$

If $\psi(L)=A\sin kL=0$, then

$$
kL=n\pi \quad n=1,2,3,\dots.
$$

Thus,

$$
\psi(x)=A\sin \left( \frac{n\pi x}{L} \right) \quad n=1,2,3,\dots.
$$

Now, we fulfill the normalized property of the wave function:

$$
\begin{gather}
A^{2}\int_{0}^{L} \sin ^{2}\left( \frac{n\pi x}{L} \right) \, dx = 1 \\
A^{2}\left( \frac{L}{2} \right)=1 \\
A=\sqrt{ \frac{2}{L} }. 
\end{gather}
$$

Thus, the normalized wave function for particle in a box is

$$
\psi_{n}(x)=\sqrt{ \frac{2}{L} }\sin\left( \frac{n\pi x}{L} \right) \quad n=1,2,3,\dots
$$

where $n$ corresponds to a particular solution for [[Quantum Mechanics#Schrodinger's Equation]]. 

Solving for energy using [[#^a2e8ff]], we get 

$$
\frac{d^{2}\psi_{n}(x)}{dx^{2}}=-\left( \frac{n\pi}{L} \right)^{2}\psi_{n}(x)
$$

and 

$$
\begin{gather}
-\frac{8\pi^{2}mE_{n}}{h^{2}}\psi_{n}(x) = \frac{d^{2}\psi_{n}(x)}{dx^{2}} \\
E_{n} = \frac{n^{2}h^{2}}{8mL^{2}}.
\end{gather}
$$

The fact that $E$ corresponds to discrete $n$ ties in with the fact that energy is [[Quantum Mechanics#Energy Quantization]].