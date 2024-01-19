# Capacitors

- basic capacitor: two conductive plates that are set a distance apart from each other
- holds charge by creating imbalance of charge in 2 sides
- accumulates charge until voltage difference is equal to that of connected voltage source

![[Pasted image 20230227171723.png]]

# Capacitance

Capacitance is defined as follows:

$$
C = \frac{Q}{V}
$$

Intuitively, this value indicates how much charge a capacitor can store given an electric potential difference to charge it.

## Geometric Formula

Using Gauss's Law and some basic electrostatics formulas, we can derive a geometric formula for the capacitance of a parallel plate capacitor.

First, plugging in the formula $V = Ed$:

$$
\begin{align}
C &= \frac{Q}{V} \\
&= \frac{Q}{Ed}
\end{align}
$$

Then, using Gauss's Law:

$$
\begin{align}
\vec{E}\vec{A} &= \frac{Q}{\epsilon_{0}} \\
\vec{E} &= \frac{Q}{\vec{A}\epsilon_{0}} \\
C &= \frac{\vec{A}\epsilon_{0}}{d}
\end{align}
$$

However, if there is a dielectric, we must multiply by the dielectric constant.

$$
C = \kappa\frac{\vec{A}\epsilon_{0}}{d}
$$

Now, we know that capacitance is 

- **$\propto$ area of a capacitor**
- **$\propto$ permittivity of the dielectric**
- **inversely $\propto$ distance between the conductive plates**.

Here are some examples of what these properties ensue:

- $d \times 2$ ->
	- battery connected -> $V$ stays the same, $C,Q,E$ $\times \frac{1}{2}$
	- battery disconnected -> $Q$ stays the same, $C, V \times \frac{1}{2}$ 
- $\kappa \times 2$
	- battery connected -> $V$ stays the same, $C, Q,E \times 2$ 
	- battery disconnected -> $Q$ stays the same, $C, E \times {2}$, $V \times \frac{1}{2}$
- $A \times 2$
	- battery connected -> $V$ stays the same, $C, Q \times 2$, $E \times \frac{1}{2}$
	- battery disconnected -> $Q$ stays the same, $C \times 2$, $E, V \times \frac{1}{2}$

## Line Integral



## Capacitors in Parallel

![[Pasted image 20230227215818.png]]

To solve for the capacitance of multiple capacitors in parallel, we use the fact that the charges running through the capacitors should add up to the total charge and that the voltage should be the same at both capacitors.

$$
\begin{align}
Q_{tot} &= Q_{1} + Q_{2} \\
\implies C_{tot}V &= C_{1}V + C_{2}V \\
\implies C_{tot} &= C_{1} + C_{2}
\end{align}
$$
## Capacitors in Series

![[Pasted image 20230227220000.png]]

To solve for capacitance in series, we use the fact that the voltages at the two capacitors should add up to the total voltage and that the charge running through both capacitors is the same.

$$
\begin{align}
V_{tot} &= V_{1} + V_{2} \\
\frac{Q}{C_{tot}} &= \frac{Q}{C_{1}} + \frac{Q}{C_{2}} \\
\frac{1}{C_{tot}} &= \frac{1}{C_{1}} + \frac{1}{C_{2}}
\end{align}
$$

## Capacitance of Different Shapes



# Potential Energy

The energy of a battery is 

$$
U_{b} = qV_{b}
$$

It's just the definition. However, the formula is different for a capacitor since the electric potential of the capacitor changes as it gets more charged.

$$
\begin{align}
U_{c} &= \int V \, dq  \\
&= \int_{0}^{Q} \frac{q}{C} \, dq \\
&= \frac{Q^{2}}{2C}  \\
&= \frac{1}{2}CV^{2}
\end{align}
$$
