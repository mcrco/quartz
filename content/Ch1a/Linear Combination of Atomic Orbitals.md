Uses [[Quantum Mechanics#Schrodinger's Equation]] and [[Quantum Mechanics#Born-Oppenheimer Approximation]] to find molecular geometry.

To find internuclear distance between 2 $H$ atoms $a$ and $b$ in $H_{2}$, solve

$$
\hat{H} \Psi(R) = E\Psi(R).
$$

This is equivalent to combining wave function/probability distributions of 2 orbitals.

1. Fix $R_{ab}$
2. Simplify with Born-Oppenheimer 

$$
\left[ -\frac{h^{2}}{2m} \frac{d^{2}}{dR^{2}} + V(R)\right]\Psi(R)=E\Psi(R) \implies V(R)\Psi(R)=E\Psi(R)
$$

3. Solve for allowed energy levels, $E$, and $\Psi$ for electrons ($H_{2}$ has 2 electrons with 6 possible coordinates)
4. Repeat at new $R_{ab}$
5. Plot lowest energy as function of $R_{ab}$

![[Pasted image 20231102215543.png]]