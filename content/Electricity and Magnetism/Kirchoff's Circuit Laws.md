# Kirchoff's Voltage Law

The net voltage gain in any closed loop is 0.

$$
V_{gain} = V_{drop}
$$

# Kirchoff's Current Law

The net current entering and exiting a junction/node is 0.

$$
I_{in} = I_{out}
$$

# Example Problem with Single Battery

![[kcl1.png]]

To solve for the currents at each point, we can use KCL and KVL

## KCL

$$
\begin{align}
I_{1} &= I_{2} + I_{3} \\
I_{3} &= I_{4} + I_{5}
\end{align}
$$

## KVL

$$
V = IR
$$

$$
\begin{align}
9V - I_{1}R_{1} - I_{2}R_{2} = 9V - 3I_{1} - 2I_{2} &= 0 \\
9V - I_{1}R_{1} - I_{4}R_{4} - I_{3}R_{3} = 9V - 3I_{1} - 2I_{4} - 3I_{3} &= 0 \\
9V - I_{1}R_{1} - I_{5}R_{5} - I_{3}R_{3} = 9V - 3I_{1} - I_{5} - 3I_{3} &= 0 \\
\end{align}
$$

## Answer

Combining these 5 equations, we can solve for each current.

# Example Problem with Double Batteries

![[kcl2.jpg]]

We can use a similar apporach here.

## KCL

$$
I_{1} = I_{2} + I_{3}
$$

## KVL

$$
\begin{align}
9V - I_{1} - 2I_{2} &= 0 \\
9V - I_{1} - 3I_{3} - 4I_{3} + 9V &= 0
\end{align}
$$

## Solution

Solving for the system of equations, we get 

$$
\begin{align}
I_{1} &= 4.3 \\
I_{2} &= 2.35 \\
I_{3} &= 1.96
\end{align}
$$
