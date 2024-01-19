A wheatstone bridge circuit can be drawn as shown below.

To find $R_{4}$ as a function of the other values, we first find $V_{g}$ as a function of the other values using [[Kirchoff's Circuit Laws|KVL]] on the loop consisting of the positive terminal of the battery, $R_{1}$, the voltmeter, $R_{3}$, and the negative end of the battery and the loop consisting of the positive end of the battery, $R_{1}$, $R_{4}$, and the negative end of the battery.

$$
\begin{cases}
V_{b} - V_{1} - V_{g} - V_{3} = 0 \\
V_{b} - V_{1} - V_{4} = 0 \\
\end{cases} \\
$$

Substituting, we get

$$
V_{g} = V_{4} - V_{3}
$$

Now we want to find $V_{4}$ and $V_{3}$ as a function of the resistances and $V_{b}$ .

$$
\begin{cases}
V_{b} = I_{1}(R_{1} + R_{4}) \\
V_{4} = I_{1}R_{4} \\
V_{b} = I_{2}(R_{2} + R_{3}) \\
V_{3} = I_{2}R_{3}
\end{cases}
$$

Substituting, we get 

$$
\begin{align}
V_{4} &= V_{b} \cdot \frac{R_{4}}{R_{1} + R_{4}} \\
V_{3} &= V_{b} \cdot \frac{R_{3}}{R_{2} + R_{3}}
\end{align}
$$

Our final formula for the reading of the voltmeter is 

$$
V_{g} = V_{b}\left(  \frac{R_{4}}{R_{1} + R_{4}} - \frac{R_{3}}{R_{2} + R_{3}} \right)
$$

Now, solving for $R_{4}$, the "unknown" resistance, we get

$$
\begin{align}
\frac{V_{g}}{V_{b}} &= \frac{R_{4}}{R_{1} + R_{4}} - \frac{R_{3}}{R_{2} + R_{3}} \\
\frac{R_{4}}{R_{1} + R_{4}} &= \frac{V_{g}}{V_{b}} + \frac{R_{3}}{R_{2} + R_{3}} \\
R_{4} &= (R_{1}+R_{4})\left( \frac{V_{g}}{V_{b}} + \frac{R_{3}}{R_{2} + R_{3}} \right) \\
R_{4}\left( 1 - \frac{V_{g}}{V_{b}} - \frac{R_{3}}{R_{2} + R_{3}} \right) &= R_{1} \left( \frac{V_{g}}{V_{b}} + \frac{R_{3}}{R_{2} + R_{3}} \right) \\
R_{4} &= \frac{R_{1} \left( \frac{V_{g}}{V_{b}} + \frac{R_{3}}{R_{2} + R_{3}} \right)}{ 1 - \frac{V_{g}}{V_{b}} - \frac{R_{3}}{R_{2} + R_{3}}} \\
&= \frac{R_{3}V_{b} - R_{2}V - R_{3}V}{R_{2}V_{b} + R_{2}V + R_{3}V}
\end{align}
$$