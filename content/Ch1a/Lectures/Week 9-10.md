# Water

- $\rho_{\text{rice}}<\rho_{\text{water}}$
	- hexagonal structure of ice
- 2 phases coexist

# Phase transition

![[Pasted image 20231121113213.png]]

- evaporation
	- surface molecules move fast enough (enough KE) to escape intermolecular forces
 
![[Pasted image 20231121113101.png]] 

- constant volume container
	- $K_{\text{condensation}} = K_{\text{evaporation}} \implies$ equilibrium
	- $K_{\text{cond}}$ increases until vapor pressure is reached
- boiling pt = $T$ @ which vapor pressure = external pressure
- phase diagram shows stable state at some $P$ and $T$

![[Pasted image 20231121113313.png]]

# Electrochemistry

- oxidation: $M\to M^{n+} + ne^{e}$
	- $Cu_{(s)}\to Cu_{(aq)}^{2+}+2e^{-}$ (half rxn)
- reduction: $M + ne^{-} \to M^{n-}$
	- $2Ag_{(aq)}^{+}+2e^{-}\to 2Ag_{(s)}$ (half rxn)
- whole rxn: 
	- $Cu_{(s)}+2Ag^{+}\to Cu^{2+}+2Ag$

## Thermodynamics

- determines if rxn will proceed
- governed by $\Delta G=$ Gibbs free energy ($\frac{J}{mol}$)
	- $\Delta G<0$: **spontaneous**: process occurs w/o addition of external energy
	- $\Delta G = 0$: reversible
	- $\Delta G>0$: non-spontaneous

$$
\Delta G = \Delta H - T\Delta S,
$$

- $\Delta H$: change in enthalpy ($J / mol$)
	- defines change in heat
- $T$: temperature
- $\Delta S$: change in entropy
	- defines change in microstate available
	- **microstate**: combinations of position and momenta

### Galvanic Cell

![[Pasted image 20231128113623.png]]

$$
\Delta E_{\text{cell}} = E_{\text{cathode}} - E_{\text{anode}}
$$

- $\Delta E_{\text{cell}}$: voltage difference/cel potential
	- energy of electron
	- units: $V = \frac{J}{C}$
	- $C$: coulomb (SI unit of charge)
	- $<0 \implies$ spontaneous
- $E_{\text{cathode}}$, $E_{\text{anode}}$: reduction potentials

$$
\Delta G=-nF\Delta E_{\text{cell}}
$$

- $n$: # electrons transferred
- $F$: Faraday's constant $=964585 \frac{C}{mol}$
- $E^{\circ}$: standard reduction potentials
	- $P=1\text{ atm}$
	- $T=298K$
	- concentration: $1M$
 
$$
\begin{align}
Pb^{2+} + 2e^{-} \to Pb &\quad E^{\circ}=-0.1263V \\
Pb \to Pb^{2+} + 2e^{-} &\quad E=0.1263V \\
\end{align}
$$

### Example Rxn

$$
\begin{align}
2Ag^{+} + 2e^{-} \to 2Ag &\quad E^{\circ} = 0.799V \\
Cu \to Cu^{2+} + 2^{-} &\quad E^{\circ}=0.34V \\
\end{align}
$$

Plugging in,

$$
E_{\text{cell}} = 0.799V-(0.344V)=0.46V.
$$

- oxidizing agent: $Ag$ accepts $e^{-}$ to oxidize something else
- reducing agent: $Cu$ releases $e^{-}$ to reduce something else

### Nernst Equation

$$
\Delta E_{\text{cell}}=\Delta E^{\circ}_{\text{cell}} - \frac{RT}{nF}\ln Q
$$

- $\Delta E^{\circ}_{\text{cell}}=\Delta E^{\circ}_{\text{cathode}}-E^{\circ}_{\text{anode}}$
- $Q$: rxn quotient, explained below

If

$$
aA + bB \to cC + dD,
$$

then 

$$
Q = \frac{[C]^{c}[D]^{d}}{[A]^{a}[B]^{b}}.
$$

## Kinetics

- determines how fast rxn proceeds
- current: flow of electrons = $\frac{C}{s}=I$
	- $\frac{C}{s}=A$ (ampere)
- $Q$: charge passed over some time
	- Coulombs $\to$ moles of electrons $\to$ moles of atoms using half reaction formula

$$
W_{\text{elec}}=Q\Delta E_{\text{cell}} = -nF\Delta E_{\text{cell}}
$$

Since we know $Q=It$

$$
n= \frac{It}{QF}.
$$

We can use this formula to figure out how many moles of reactants are consumed and products are formed if we know the current and the charge.