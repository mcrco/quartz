# Materials

- voltage source
- 5 resistors
	- 8.2k, 1.5k, 1.2k, 1k, emitter resistor
- 5 capacitors
	- 2 x 1$\mu f$ (bypass)
	- 4.7nf
	- 47nf
	- 1 emitter bypass resistor
-  1 indcutor
	- 1mh
 - oscilloscope (or radio)\

# Derivation

## LC

We want 150 khz

$$
\begin{align}
f &= \frac{1}{2\pi \sqrt{ LC }} \\
150000 &= \frac{1}{2\pi \sqrt{ LC_{total} }} \\
\implies C_{total} &= \frac{1}{9\cdot 10^{10}\pi^{2}L} \\
\implies \frac{C_{1}C_{2}}{C_{1} + C_{2}} &= \frac{1}{9\cdot 10^{10}\pi^{2}L} \\
\end{align}
$$

We want feedback ratio to roughly be 1/3

$$
C_{1}/
$$