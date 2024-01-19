- $e^{-}$
- $9.11\cdot 10^{-31}\text{ kg}$
- forms cloud around nucleus
- live in orbitals around nucleus
	- orbitals have size, shape, energy
	- orbitals are associated with quantum numbers

# Quantum Numbers

- solution of [[Quantum Mechanics#Schrodinger's Equation]] for one-electron atom when replacing potential energy with Coulomb potential quantizes 3 quantum numbers : $n,l,m$
- electrons with quantum numbers $n,l,m$ (aka every Hartree orbital) are associated with a [[Quantum Mechanics#Interpreting Wave Function|wave function]] $\Psi_{nlm}$, where $\Psi(p)^{2}$ is the probability of finding the electron at position $p$.

$$
\Psi_{nlm}(r,\theta,\phi)=R_{nl}(r)Y_{lm}(\theta,\phi).
$$




## 4 Quantum Numbers

### Principal Quantum Number ($n$)

- indexes energy level 
- comes from quantization of energy

$$
E_{n}=-\frac{Z^{2}e^{4}m_{e}}{8\epsilon_{0}^{2}n^{2}h^{2}} \quad n=1,2,3,\dots
$$

- $n \propto$ energy of electron
- $n \propto r$ (distance from nucleus)

### Angular Momentum Quantum Number ($l$)

- quantization of $L^{2}$ (angular momentum squared)

$$
L^{2}=l(l+1) \frac{h^{2}}{4\pi^{2}} \quad l=0,1,\dots,n-1
$$

- related to shape
- $s=0,p=1,d=2,f=3$ 

### Magnetic Quantum Number ($m_{l}$)

- quantization of angular momentum 

$$
L_{z}=m \frac{h}{2\pi} \quad m=-l, -1+1,\dots,0,\dots l-1,l
$$

- describes how energy of atom shifts in external magnetic field
 
![[Pasted image 20231023214319.png]]

### Electron Spin Quantum Number ($m_{s}$)

- orientation of the magnetic moment of the electron is quantized according to Stern-Gerlach experiment
- $+\frac{1}{2}, -\frac{1}{2}$
- 2 electrons live in orbital described by first 3 quantum numbers

![[Pasted image 20231006144917.png]]

## Rules 

Basically, electrons ALWAYS go for LOWER ENERGY. This summarizes all of chemistry.

### Aufbau Principle

- describes ground state electron configuration of atom
	- ground state: lowest energy state of atom
- built up by arranging the Hartree atomic orbitals in order of increasing energy
- electrons always fill lower energy orbitals before higher energy orbitals
	- [[Periodic Table]] spdf categorization is based on this
		- start with $s$ on left, end with $p$ on right

![[Pasted image 20231023213717.png]]

- **exceptions** starting in period 4
	- transition metals
	- energy of $4s$ and $3d$ subshells are very similar
	- $\epsilon_{3d}< \epsilon_{4s}$
		- $K:[Ar]3d^{0}4s_{1}$
		- $Ca:[Ar]3d^{0}4s^{2}$
	- $\epsilon_{4s} < \epsilon_{3d}$
		- when putting >3 electrons into 3d orbitals, there is electrostatic repulsion energy ($\epsilon_{\text{er}}$)
		- $\epsilon_{\text{er d-orbital}} \gg \epsilon_{\text{er s-orbital}}$ because localized vs diffused
		- $\epsilon_{\text{er d}} > |\epsilon_{3d} - \epsilon_{4s}|$
	- half filled + fully filled shells -> lower energy -> $4s$ electrons sometimes go to $3d$ to fill last spot for fully filled/half filled subshell
		- $Cu: [Ar]3d^{10}4s ^{1}$
		- $Cr: [Ar]3d^{5}4s ^{1}$

### Pauli's Exclusion Principle

- no 2 atoms can have same 4 qn

### Hund's Rules

- when electrons are added to Hartree orbitals of equal energy, all orbitals will be singly occupied before any is doubly occupied
	- lowest electron config has parallel spins

## Electron Configurations

- Example configurations:
	- H: $1s ^{1}$
	- He: $1s^{2}$
	- Li: $1s^{2}, 2s ^{1}$
	- B: $1s^{2}, 2s^{2}, 2p^{1}$
	- C: $1s^{2}, 2s^{2}, 2p^{2}$

# Ionization Energy

$$
\text{X} + \text{IE} \to \text{X}^{+} + \text{e}^{-}
$$

- energy required to remove electron from orbitals to vacuum (0 energy)
- farther away from nucleus -> shielding lower effective nuclear charge -> higher energy -> lower ionization energy
- higher ionization energy -> more stable
- measured by **photoelectron spectroscopy**
	- shots photon at electron with certain energy
	- produces graph with peaks in energy that represents atomic subshells
 
![[Pasted image 20231006145107.png]]

- energy level differences $\to$ **valence** vs **core** electrons

![[Pasted image 20231006144850.png]]

- **valence electrons**
	- outermost shells
	- participate in bonding
- **core electrons**
	- all the others
	- cause shielding
	- (Ry) rydberg energy: $2.18\cdot {10}^{-18}$ J
		- boundary between valence and core electrons
		- $|e_{a}-e_{b}| < \text{Ry} \implies$ $e_{a}$ is valence electron if $e_{b}$ is valence electorn and vice versa

# Electron Affinity

$$
\text{X}^{-} + \text{EA} \to \text{X} + \text{e}^{-}
$$

- energy required to detach electron from anion to yield neutral atom
	- energy released when atom gains an electron

# Electronegativity

- tendency of an atom to attract share $e^{-}$
	- bonds
	- relative
- atomic radius $\propto$ 1/EN
- nuclear charge $\propto$ EN
- shielding $\propto$ 1/EN
- example: Cl and Na
	- electron from Na will go to Cl because Cl more stable
	- $Na^{+}Cl^{-}$
- causes dipoles in [[Bonds#Ionic Bond|ionic bonds]]

There are two scales:

### Mulliken

$$
EN=\frac{1}{2}C(1E_{1}+EA),
$$

$C$ is a proportionality constant.

### Pauling

$$
EN=\pi
$$

- $\pi$ related to bond dissocation
- A-A
	- perfectly covalent
	- $\Delta E_{AA}$ = bond dissociation E
- B-B
	- $\Delta E_{BB}$ = bond dissociation E
- consider A-B
	- covalent character of A-B = $\sqrt{ \Delta E_{A A} \Delta E_{B B} }$
	- ionic character = $\Delta$ (excess bond energy)
		- $\Delta=\Delta E_{AB}-\sqrt{ \Delta E_{A A} \Delta E_{B B} }$
	- define $\pi$ in terms of $\Delta$
		- $\pi_{A}-\pi_{B}=0.102\Delta^{1/2}$
	- EN diff > 2 = ionic bond
	- EN diff = 0 = covalent bond