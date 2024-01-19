# Inorganic Nomenclature
## Ionic Compounds

- group 1 or 2
- $Na^{+}$: sodium ion
- multiple oxidation states
	- $Cu^{+}$: copper (I) ion
	- $Cu^{2+}$: copper (II) ion
	- $Fe^{2+}$: iron (II) - ferrous
	- $Fe^{3+}$: iron (III) - ferric
- $NH_{4}^{+}$: ammonium
- $H_{3}O^{+}$: hydronium

### Anions

- monoatomic: add ide to the root
	- $Cl$: Chlorine
	- $Cl^{-}$: chloride
- oxyanions: atom + $O_{x}$
	- $SO_{3}^{2-}$: sulfite (less $O$)
	- $SO_{4}^{2-}$: sulfate (more $O$)
	- $ClO^{-}$: hypochlorite (least)
	- $ClO_{2}^{-}$: chlorite
	- $ClO_{3}^{-}$: chlorate
	- $ClO_{4}^{-}$: perchlorate (most)

## Covalent Compounds

- prefixes to name compounds 
- indicate # of atoms
- $N_{}O$: nitrogen oxide
- $N_{2}O$: dinitrogen oxide
- $N_{2}O_{3}$: dinitrogen trioxide

# Quantum Mechanics

1. energy is quantized
2. particles display wave-like behavior

## Energy Quantization

- Evident through atomic emission spectrum

![[Pasted image 20231024112252.png]]

## Bohr Model

- connected continuous energy to quantized energy of electron
- $e^{-}$ orbits around nucleus
- $E=KE+PE$
- $E=\frac{1}{2}m_{e}v^{2} - \frac{ze^{2}}{4\pi\epsilon_{0}r}$
- $e^{-}$ is accelerating -> should collide with nucleus
- assume $e^{-}$ can only occupy discrete orbits 
	- radius = $r_{n} \implies$ only certain $E_{n}$ allowed
	- $r=\frac{n^{2}}{z}a_{0}$, 
	- $E_{n}=-R_{\infty}\frac{z^{2}}{n^{2}}$, $R_{\infty}$: Rydberg constant
	- can predict IE of H
		- $\Delta E=E_{final}-E_{initial}=E_{n=\infty}-E_{n=1}=0 - R_{\infty}$

## Wavelike Behavior

- wave-particle duality
- photoelectric effect

![[Pasted image 20231102220225.png]]

![[Pasted image 20231102220715.png]]

- light and electrons behave like waves 
	- $A$: amplitude
	- $\lambda$: wavelength
	- $\nu$: frequency

![[Pasted image 20231024113837.png]]

- constructive interference and destructive interference

![[Pasted image 20231024113951.png]]

- light behaves like particle
	- photon
	- $E_{\text{photon}}=h\nu$, $h=$ Planck's constant, $\nu=\frac{c}{\lambda}$
- electrons
	- de Broglie: behave like standing waves
	- $n \frac{\lambda}{2}=L$
		- $n=1,2,3\dots$
		- $L=$ length of string
		- $n=1$: first hamonic
	- behave like circular standing waves
		- $n\lambda=2\pi r$
	- can consider angular momentum L
		- $L=m_{e}vr=n \frac{h}{2\pi}$
	- Heisenberg Uncertainty Principle
		- cannot know position of momentum at any one time

# Quantum Mechanics

1. Energy is quantized
2. Wave-particle duality (light like particles, electrons like waves)

## Schrodinger's Equation

$$
\hat{H}\Psi = E \Psi
$$

- $\Psi$ is the electronic wavefunction
	- $(x,y,z,t)$
- $\hat{H}$: set of mathematical instructions called operator
- $E$: total energy of atom
- when we solve Schrodinger's Equation, many solutions of $\Psi$ are characterized by particular $E$
- orbital = specific $\Psi$ solution
- $\Psi^{2}$: probability of finding an electron = probability distribution
- size of orbital: radius that encloses 90% of electron probability distribution
- each $\Psi$ is characterized by set of quantum numbers
	- uses spherical coordinates
	- $\Psi_{nlm}(r,\theta,\phi)$
- $Y$: angular part of $\Psi$
	- given $n$, $Y_{lm}(\theta,\phi)$ has 2 lobes with + and - phase

![[Pasted image 20231102220800.png]]

$$
\Psi_{nlm}(r,\theta,\phi)=R_{nl}(r)Y_{lm}(\theta,\phi).
$$

## Molecular Orbitals

- quantum picture of a chemical bond
- Morse potential predicts
	- structure
	- vibrations
	- formation

## Born-Oppenheimer Approximation

- electrons move much faster than nuclei
- assume nuclei are fixed in space when solving Schrodinger's equation

$$
2\sigma_{u}^{*}
$$

- 2: integer that tracks relative energies for each symetry type
- $\sigma$: descirbes orientation around internuclear axis
	- $\sigma$: cylindrical symmetry
	- $\pi$: $\Psi$ has nodal plane that contains internuclear axis
- $u$: describes inversion symmetry
	- $u$: ungerade, $g$: gerade
- \*: node on internuclear axis

## Linear Combination of Atomic Orbitals

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

# Hybridization

- atomic orbitals are purely mathematical constructs
- only genuine wavefunction we know is in one electron system
- orbitals in multi-electron systems are approx
	- atomic orbitals = basis set
- hybridization: useful mathematical manipulation of orbitals to describe behavior of the second period
	- 3 types; $sp$, $sp^{2}$, $sp^{3}$
	- $\pi$ represents hybrid orbitals
	- ex1: $BeH_{2}$ has linear geo, use hybridization to understand
		- basis set: 1s, 2s, 2p
		- valence: 2s, 2p
			- $p_{x},p_{y},p_{z}$
	![[Pasted image 20231102112133.png]]
		- mix $2s$ and $2p_{z}$ 
		- $\pi_{1}(r)=C(-2s-2p_{z})$
		- $\pi_{2}(r)=C(-2s+2p_{z})$
	![[Pasted image 20231102112204.png]]
  ![[Pasted image 20231102220838.png]]
	- $BH_{3}$
		- trigonal planar geo
		- basis set: $2s, 2p_{x}, 2p_{y}, 2p_{z}$
		- $\pi_{2}(r)=\left( \frac{1}{3} \right)^{1/2}(-2s)+2(\frac{1}{6})^{1/2}(2p_{x})$
			- $sp^{2}$ orbital
		- $\pi_{1}(r)=\left( \frac{1}{3} \right)^{2}(-2s)-\left( \frac{1}{6} \right)^{1/2}p_{x}+(\frac{1}{2})^{1/2}2p_{y}$
			- need to use x and y because of angle required
		- $\pi_{3}(r)=\left( \frac{1}{3} \right)^{2}(-2s)-\left( \frac{1}{6} \right)^{1/2}p_{x}-(\frac{1}{2})^{1/2}2p_{y}$
  ![[Pasted image 20231102220914.png]]
	- $CH_{4}$
		- tetrahedral geo
		- basis set: $2s, 2p_{x}, 2p_{y},2p_{z}$
			- $\pi_{1}(r)=-\frac{1}{2}(2s+2p_{x}+2p_{y}+2p_{z}) \to$ 109.5 degree angle
  ![[Pasted image 20231102220939.png]]
	- carbon can be described using $sp, sp^{2},sp^{3}$ hybridization
		- $C_{2}H_{4}$
	![[Pasted image 20231102114830.png]]
		- $sp^{2}$ hybridization b/c steric number of 3
		- double bond $\implies$ $\sigma, \pi$ bond together
		- non-hybridized $p$ orbitals bond for $\pi$ bond
  ![[Pasted image 20231102115202.png]]
		- triple bond example: acetylene