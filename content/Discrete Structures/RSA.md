# Intro

RSA is an encryption algo used to send a message from one person to another. Each person has a private and public key.

# Procedure

The variables used will be 

$$
p, q, z, n, s
$$

$p$ and $q$ are 2 long primes, but for the demonstration we will use 

$$
\begin{align}
p &= 2 \\
q &= 11 \\
z = pq &= 22
\end{align}
$$

Now we calculate $\phi$ using Euler's totient function

$$
\phi_{z} = (p - 1)(q - 1) = 10
$$

The receiver chooses a number 

$$
n:\text{gcd}(n,\phi) = 1
$$

This is useful for finding 

$$
s:s \in (0, \phi) \land ns \equiv 1 \mod \phi
$$

$n$ is often prime. In our case, we set $n$ to 7 and $s$ to 3.

$$
\begin{align}
n &= 7 \\
s &= 3
\end{align}
$$

$n, z$ are broadcast by the receiver as public keys. The send broadcasts the message encrypted using the formula 

$$
c = a^{n} \mod z
$$

For example, if the sender encrypts and sends the message $5, 13, 8$, they would send $3, 7, 2$. 

Now, the receiver uses his private key $s$ to decode the message.

$$
\begin{align}
3^{3} &\equiv 5 \mod 22 \\
7^{3} &\equiv 13 \mod 22 \\
2^{3} &\equiv 8 \mod 22
\end{align}
$$

