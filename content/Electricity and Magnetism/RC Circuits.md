Summary of: https://phys.libretexts.org/Bookshelves/University_Physics/Book%3A_University_Physics_(OpenStax)/Book%3A_University_Physics_II_-_Thermodynamics_Electricity_and_Magnetism_(OpenStax)/10%3A_Direct-Current_Circuits/10.06%3A_RC_Circuits

RC circuits are circuits with a [[Resistors|resistor]] and a [[Capacitors and Dielectrics|capacitor]].

![[Pasted image 20230305150610.png]]

![[circuit.png]]
# Charging

![[Pasted image 20230305172429.png]]

When battery and capacitor are connected, capacitor charges until 

$$
\epsilon = V_{B} = V_{C}
$$

## Charge vs Time

To find the rate at which the capacitor charges, we can use [[Kirchoff's Circuit Laws|Kirchoff's Voltage Law]], using $\epsilon$ as the emf of the battery, $V_{R}$ as the voltage of the resistor, and $V_{C}$  as the voltage of the capacitor.

$$
\begin{align}
\epsilon - V_{R} - V_{C} &= 0 \\
\epsilon - IR - \frac{q}{C} &= 0 \\
\epsilon - R\frac{dq}{dt} - \frac{q}{C} &= 0 \\
\frac{dq}{dt} &= \frac{\epsilon C - q}{RC} \\
\int_{0}^{q} \frac{dq}{\epsilon C-q} &= \frac{1}{RC} \int_{0}^{t} dt 
\end{align}
$$

Using a u-sub for $u = \epsilon C-q$, we get

$$
\begin{align}
-\int_{0}^{q} \frac{du}{u} &= \frac{1}{RC}\int_{0}^{t}  \, dt \\ 
\ln\left( \frac{\epsilon C-q}{\epsilon C} \right) &= -\frac{t}{RC} \\
\frac{\epsilon C-q}{\epsilon C} &= e^{-\frac{t}{RC}} \\
q &= C\epsilon\left( 1-e^{-\frac{t}{RC}} \right)
\end{align}
$$

Our final formula for charge as a function of time is

$$
\begin{align}
Q &= C\epsilon\left( 1-e^{-\frac{t}{RC}} \right) \\
&= Q_{0}\left( 1-e^{-\frac{t}{\tau}} \right)
\end{align}
$$

where $RC$ is also called the time constant, $\tau$.

## $V_{C}$ vs Time

Since we know that $Q=CV$, $V_{C}\propto Q$, and therefore

$$
\begin{align}
V_{C} = V_{0}\left( 1-e^{-\frac{t}{\tau}} \right)
\end{align}
$$

## Current vs Time

Using the formula for charge as a function of time, we can find the formula for the current running through the resistor as a function of time.

$$
\begin{align}
I &= \frac{dQ}{dt} \\
&= \frac{d}{dt} \left[ C\epsilon\left( 1-e^{-\frac{t}{\tau}} \right) \right] \\
&= C\epsilon\left( \frac{1}{RC} \right)e^{-\frac{t}{\tau}} \\
&= \frac{\epsilon}{R}e^{-\frac{t}{\tau}} \\
&= I_{0}e^{-\frac{t}{\tau}}
\end{align}
$$

Our final formula for current as a function of time is

$$
I = I_{0}e^{-\frac{t}{\tau}}
$$

## $V_{R}$ vs Time

Since we know that $V=IR$ , $V_{R}\propto I$, and therefore 

$$
V_{R} = V_{0}e^{-\frac{t}{\tau}}
$$

## Summary

![[Pasted image 20230305164404.png]]

# Discharging

![[Pasted image 20230305172456.png]]

The capacitor discharges until $V_{C} = 0$.

## Charge vs Time

We can use [[Kirchoff's Circuit Laws|Kirchoff's Voltage Law]] again to find charge vs time.

$$
\begin{align}
-V_{R} - V_{C} &= 0 \\
-IR - \frac{q}{C} &= 0 \\
-\frac{dq}{dt}R -\frac{q}{C} &= 0 \\
\int \frac{dq}{q} &= \int -\frac{dt}{RC} \\
\ln q - \ln Q_{0} &= -\frac{t}{RC} \\
q &= Q_{0}e^{-\frac{t}{RC}}
\end{align}
$$

Rewriting, we get that our formula for charge vs time is

$$
Q = Q_{0}e^{-\frac{t}{\tau}}
$$

Here, $\tau$ is actually the amount of times it takes for the charge to become $\frac{1}{e}$ the amount it was before, kinda like a half-life (but e-life???).

## $V_{C}$ vs Time

$$
V_{C} \propto Q \implies V_{C} = V_{0}e^{-\frac{t}{\tau}}
$$

## Current vs Time

$$
\begin{align}
I &= dQ/dt \\
&= -\frac{Q_{0}}{\tau}e^{-\frac{t}{\tau}}
\end{align}
$$

## $V_{R}$ vs Time

$$
V_{R} \propto I \implies V_{R} = -\frac{V_{0}}{\tau}e^{-\frac{t}{\tau}}
$$

## Summary

![[Pasted image 20230305173928.png]]