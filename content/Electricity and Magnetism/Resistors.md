Resistors are any module in a circuit that hinders the passing of current.

There are 2 measures for resistors: resistivity and resistance.

Resistivity measures how poorly a material conducts electricity. It is defined as follows

$$
\rho = \frac{\vec{E}}{\vec{J}} = \rho_{293k}(1+\alpha(T-T_{293k})) = \frac{\Delta V}{dJ} = \frac{\Delta VA}{dI} \propto \frac{1}{\sigma}
$$

On the other hand, resistance measures how poorly a wire/resistor conducts electricty.

$$
R = \frac{\Delta V}{I} = \frac{L\rho}{A}
$$

The formula above is called Ohm's Law.

# Series

![[Pasted image 20230228100429.png]]

Since we know that the current doesn't change from each resistor but voltage adds up, we can solve to find the total resistance of resistors in series.

$$
\begin{align}
V &= IR \\
V_{tot} &= V_{1} + V_{2} + V_{3} \\
IR_{tot} &= IR_{1} + IR_{2} + IR_{3} \\
R_{tot} &= R_{1} + R_{2} + R_{3}
\end{align}
$$

# Parallel

![[Pasted image 20230228100501.png]]

Since we know that the current splits and adds up but the voltage stays the same, we can solve for the total resistance of resistors in parallel.

$$
\begin{align}
I &= \frac{V}{R} \\
I_{tot} &= I_{1} + I_{2} + I_{3} \\
\frac{V}{R_{tot}} &= \frac{V}{R_{1}} + \frac{V}{R_{2}} + \frac{V}{R_{3}}
\end{align}
$$

