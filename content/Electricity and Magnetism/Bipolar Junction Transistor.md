- 3 semiconductor layers
	- NPN or PNP
- used as switch or amplifier
- different from just back to back diodes because there is interaction between the layers
- $V_{e}$ is voltage at emitter, $V_{b}$ is voltage at the base, $V_{c}$ is the voltage at the collector

# Layers

- emitter
	- heavily doped (like conductor)
- base 
	- lightly doped (like insulator)
	 - very thin
- collector
	- moderately doped (like semiconductor)

# NPN

## Diagram

![[Pasted image 20230426210642.png]]

## Circuit Symbol

![[Pasted image 20230426211959.png]]

- arrow indicates the direction of current

## Regions of Operation

### Active Region

- $V_{c} > V_{b} > V_{e}$
- emitter is in forward bias
- collector is in reverse bias
- used for amplification

![[Pasted image 20230426211514.png]]

### Cutoff Region

- $V_{c}, V_{e} > V_{b}$
- emitter is in reverse bias
- collector is in reverse bias
- used for switching

![[Pasted image 20230426211550.png]]

### Saturation Region

- $V_{b} > V_{e}, V_{c}$
- emitter is in forward bias
- collector is in forward bias
- used for switching

![[Pasted image 20230426211700.png]]

## Configurations

- different configurations are used for different applications
- 3 types
	- common emitter
		- current + voltage gain
	- common base
		- voltage gain but no current gain
	- common collector
		- current gain but no voltage gain
	- "common" indicates that both of the other non-common component are connected to the common component
		- example: common emitter means that both the base and collector are connected to the emitter
  
## Transistor Working Demonstration

- let's model a a NPN, common emitter BJT transistor working in the active region 
- input is applied between the base and emitter 
- output is measured between the collector and emitter.

![[Pasted image 20230426214448.png]]

- $V_{bb}$ pushes electrons from the emitter to the base
- electrons in base have 2 options:
	- flowing through $R_B$ and the positive terminal of $V_{bb}$ 
	- flowing through $R_C$ and the positive terminal of $V_{cc}$ 
- most electrons flow to collector b/c
	- collector is lightly doped
	- base layer is very thin

In short, we just reiterated the [[#Active Region]] section:

- current flows from emitter to base (emitter is forward biased)
- current flows from emitter to collector (reverse biased) (note that in the diagram in the [[#Active Region]] section, current flows from base to collector because it's a common base config)

Diagram of current:

![[Pasted image 20230426215034.png]]

Now we perform KCL:

$$
\begin{align}
I_{b} + I_{c} &= I_{e} \\
I_{c} &\approx I_{e} \\
\implies I_{c} &= \alpha I_{e} \\
I_{b} + \alpha I_{e} &= I_{e} \\
\implies I_{b} &= I_{e}(1-\alpha) \\
\implies I_{c} &= \frac{\alpha}{1-\alpha}I_{b} \\
I_{c} &= \beta I_{b} \\
\implies I_{e} &= (\beta + 1)I_{b}
\end{align}
$$

Since $I_{b}$ is the input and $I_{c}$ is the output, you can control the output ($I_{c}$) by just changing the base current.

# PNP

## Diagram

![[Pasted image 20230426210705.png]]

## Circuit Symbol

![[Pasted image 20230426212053.png]]

- arrow indicates direction of current