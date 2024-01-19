# Question 1

Use the Euler equation to show

$$
\begin{gather}
\sin(\alpha+\beta) = \sin\alpha \cos\beta + \sin\beta \cos\alpha; \\
\cos(\alpha+\beta) = \cos\alpha \cos\beta -\sin\alpha \sin\beta
\end{gather}
$$

## Proof

Consider $e^{i(\alpha+\beta)}$. We can rewrite it as $e^{i\alpha} \cdot e^{i\beta}$. Expanding each factor, we get

$$
\begin{gather}
e^{i\alpha} = \cos\alpha + i\sin \alpha \\
e^{i\beta} = \cos\beta + i\sin\beta .
\end{gather}
$$

Now, multiplying the two factors,

$$
\begin{align}
e^{i\alpha} \cdot e^{i\beta} &= (\cos \alpha + i\sin \alpha)(\cos\beta + i\sin\beta) \\
&= \cos \alpha \cos\beta + i\sin\beta \cos\alpha + i\sin\alpha \cos\beta + i^{2}\sin \alpha \sin\beta \\
&= (\cos\alpha \cos\beta-\sin\alpha \sin\beta) + i(\sin\alpha \sin\beta+\sin\beta \sin\alpha)
\end{align}
$$

Since we know $e^{i(\alpha+\beta)}$ is also $\cos(\alpha+\beta) + i\sin(\alpha+\beta)$, we can equate

$$
\cos(\alpha+\beta) + i\sin(\alpha+\beta) = (\cos\alpha \cos\beta-\sin\alpha \sin\beta) + i(\sin\alpha \sin\beta+\sin\beta \sin\alpha).
$$

Equating the coefficients of the real and imaginary parts, we get

$$
\begin{gather}
\cos(\alpha+\beta) = \cos\alpha \cos\beta - \sin\alpha \sin\beta \\
\sin(\alpha+\beta) = \sin\alpha \sin\beta + \sin\beta \sin\alpha.
\end{gather}
$$

# Question 2

a. Show that $|z|=\text{Re}(z)$ iff $z$ is a non-negative real number.

## Proof

To prove that $|z|=\text{Re}(z)$ if and only if $z$ is a non-negative real number, we will prove the following 2 conditional statements:

1. If $z$ is a non-negative real number, then $|z|=\text{Re}(z)$ .
2. If $|z|=\text{Re}(z)$, $z$ is a non-negative real number. 

To prove the first statement, assume, $z$ is a non-negative real number. Thus $|z|=\sqrt{ z^{2}+0^{2} }=\sqrt{ z^{2} }$ since there is no complex part. $\sqrt{ z^{2} }$ is the absolute value of $z$, which is equal to $z$ when $z$ is non-negative. Because $z$ is the modulus and its own real part, if $z$ is non-negative real number, then $|z|=\text{Re}(z)$.

To prove the second statement, let $z=a+bi$. Thus, 

$$
\begin{gather*}
|z|=\sqrt{ a^{2}+b^{2} }=\text{Re}(z)=a \\
\sqrt{ a^{2}+b^{2} }=a \\
a^{2}+b^{2}=a^{2} \\
b^{2}=0 \\
b=0.
\end{gather*}
$$

Thus, $z=a+0i=a$ and $z$ is real. Since, $a=\text{Re(z)}=|z|\geq 0$, we know $a\geq 0$ and $z\geq 0$. Thus, if $|z|=\text{Re}(z)$, $z$ is a non-negative real number.

b.  Show that $(\bar{z})^{2}=z^{2}$ if and only if $z$ is purely real or purely imaginary.

## Proof

To prove the biconditional statement, we will prove the 2 conditional statements:

1. If $z$ is purely real or purely imaginary, then $(\bar{z})^{2}=z^{2}$.
2. If $(\bar{z})^{2}=z^{2}$, then $z$ is purely real or purely imaginary.

To prove the first statement, we split the "or" part into 2 cases: when $z$ is purely real and when $z$ is purely imaginary.

In the case that $z$ is purely real, let $z=a+0i$, $a \in \mathbb{R}$. Then,

$$
(\bar{z})^{2}=(\overline{a+0i})^{2} = (a-0i)^{2}=a^{2}=z^{2}.
$$

Thus, $(\bar{z})^{2}=z^{2}$.

In the case that $z$ is purely imaginary, let $z=0+bi$. Then,

$$
(\bar{z})^{2}=(\overline{0+bi})^{2}=(-bi)^{2}=b^{2}i^{2}=z^{2}.
$$

Thus, $(\bar{z})^{2}=z^{2}$ in the second case, too.

Since we have proven that $(\bar{z})^{2}=z^{2}$ in both cases, the first conditional statement is true.

For the second statement, we will do a proof by contrapositive. That is, if $z$ is purely real or purely imaginary is false, then $(\bar{z})^{2}=z^{2}$ is false. Using DeMorgan's Law, we can rewrite the contrapositive as if $z$ is not purely real and $z$ is not purely imaginary, then $(\bar{z})^{2}=z^{2}$ is false. To prove this new statement, we assume that $z$ is not purely real and not purely imaginary. Thus, $z$ must have a real and imaginary component, and and we can let $z=a+bi$, $a,b \neq 0$. We will now prove the contrapositive with a proof by contradiction. Suppose that $(\bar{z})^{2}=z^{2}$. Then,

$$
\begin{gather*}
(\bar{z})^{2}=z^{2} \\
(a-bi)^{2}=(a+bi)^{2} \\
a^{2}-2abi+b^{2}i^{2}=a^{2}+2abi+b^{2}i^{2} \\
-2abi=2abi \\
4abi=0 \\
\end{gather*}
$$

For the above equation to be true, either $a=0$ or $b=0$. However, we know this is not true since $z=a+bi$, $a,b\neq 0$. Thus, if $z$ is purely real or purely imaginary is false, $(\bar{z})^{2}=z^{2}$ is false. By proving the contrapositive, we have proven that if $(\bar{z}^{2})=z^{2}$ if $z$ is purely real or $z$ is purely imaginary.

Since we have proven both conditional statements, the original biconditional statement must be true.

# Question 3

Show that 

$$
|z\cdot w|=|z|\cdot|w|
$$

a. using Cartesian form.

## Proof

Let $z=a+bi$ and $w=c+di$. Plugging in these values into $|z\cdot w|$, we get

$$
\begin{align*}
|(a+bi)(c+di)| &= |ac + adi + bci + bdi^{2}| \\
&= |ac - bd + (ad + bc)i| \\
&= \sqrt{ (ac-bd)^{2} + (ad+bc)^{2} } \\
&= \sqrt{ (ac)^{2} - 2abcd + (bd)^{2} + (ad)^{2} + 2abcd + (bc)^{2} } \\
&= \sqrt{ a^{2}c^{2}+a^{2}d^{2}+b^{2}d^{2}+b^{2}c^{2} } \\
&= \sqrt{ (a^{2}+b^{2})(c^{2}+d^{2}) } \\
&= \sqrt{ a^{2}+b^{2} }\sqrt{ c^{2}+d^{2} }  \\
&= |z|\cdot |w|.
\end{align*}
$$

Thus, $|z\cdot w|=|z|\cdot|w|$.

b. using polar form
## Proof

Let $z=r_{1}e^{i\theta_{1}}$ and $w=r_{2}e^{i\theta_{2}}$. Plugging in, we get

$$
\begin{align*}
|z\cdot w|&=|r_{1}e^{i\theta_{1}}\cdot r_{2}e^{i\theta_{2}}| \\
&= |r_{1}r_{2}e^{i(\theta_{1}+\theta_{2})}| \\
&= r_{1}r_{2} \\
&= r_{1}\cdot r_{2} \\
&= |z|\cdot|w|.
\end{align*}$$

Thus, $|z\cdot w|=|z|\cdot|w|$.

# Question 4

a. Show that $\overline{z+w}=\bar{z}+\bar{w}$.

## Proof

Let $z=a+bi$ and $w=c+di$. Then,

$$
\begin{align*}
\overline{z+w}&=\overline{a+bi+c+di} \\
&= \overline{(a+c)+(b+d)i} \\
&= (a+c)-(b+d)i \\
&= a-bi+c-di \\
&= \bar{z}+\bar{w}.
\end{align*}
$$


Thus, $\overline{z+w}=\bar{z}+\bar{w}.$

b. Show that $\overline{z\cdot w}=\bar{z} \cdot \bar{w}$.

## Proof

Let $z=a+bi$ and $w=c+di$. Then,

$$
\begin{align*}
\overline{z\cdot w} &= \overline{(a+bi)(c+di)} \\
&= \overline{ac+adi+bci+bdi^{2}} \\
&= \overline{ac-bd+(ad+bc)i} \\
&= ac-bd-(ad+bc)i \\
&= ac-adi-bd-bci \\
&= ac-adi-bdi^{2}-bci \\
&= (a-bi)(c-di) \\
&= \bar{z}\cdot \bar{w}.
\end{align*}
$$

Thus, $\overline{z\cdot w}=\bar{z}\cdot \bar{w}$.

c. Use (b) to show that $\overline{z^{n}}=(\bar{z})^{n}$ for any natural number $n\in\mathbb{N}.$

## Proof

We will perform a proof by induction. Consider the statement $S(n)$ given by 

$$
\overline{z^{n}}=(\bar{z})^{n}.
$$

We will use induction to prove that $S(n)$ is true for $n\in\mathbb{N}$.

We start by verifying the base case $S(n).$

$$
\overline{z^{1}}=\bar{z}=(\bar{z})^{1}
$$

Thus, we have proven the base case.

Now, we perform the inductive step. Assume $S(k)$ is true for $k \geq 1, k, \in \mathbb{N}$. That is, we assume

$$
\overline{z^{k}}=(\bar{z})^{k}.
$$

We will use this to prove $S(k+1)$, or

$$
\overline{z^{k+1}}=(\bar{z})^{k+1}.
$$

We start with the LHS of the above equation. 

$$
\begin{align*}
\overline{z^{k+1}}&=\overline{z^{k}\cdot z} \\
&= \overline{z^{k}}\cdot \bar{z} \\
&= (\bar{z})^{k}\cdot \bar{z} \\
&= (\bar{z})^{k+1}.
\end{align*}
$$

Thus, we have proven $S(k+1)$ using $S(k)$ and part b. 

By induction, we know that the statement $S(n)$ given by $\overline{z^{n}}=(\bar{z})^{n}$ is true for $n \in \mathbb{N}$.

d. Use a-c to prove that for 

$$
p(z)=a_{n}z^{n}+a_{n-1}z^{n-1}+\dots+a_{1}z+a_{0},
$$

if $p(w)=0$ for $w \in \mathbb{C}$, then $p(\bar{w})=0$.

## Proof

Assume that $p(w)=a_{n}w^{n}+\dots+a_{0}=0$. Taking the conjugate, we get

$$
\overline{p(w)}=\overline{a_{n}w^{n}+a_{n-1}w^{n-1}+\dots+a_{1}w+a_{0}}.
$$

By the theorem we proved in part a, we can write

$$
\begin{align*}
\overline{p(w)}&=\overline{a_{n}w^{n}+a_{n-1}w^{n-1}+\dots+a_{1}w+a_{0}} \\
&= \overline{a_{n}w^{n}}+\overline{a_{n-1}w^{n-1}}+\dots+\overline{a_{1}w}+\overline{a_{0}}.
\end{align*}
$$

Then, using the theorem we proved in part b, we can write


$$
\begin{align*}
\overline{p(w)}&=\overline{a_{n}w^{n}}+\overline{a_{n-1}w^{n-1}}+\dots+\overline{a_{1}w}+\overline{a_{0}} \\
&= \overline{a_{n}}\cdot \overline{w^{n}}+\overline{a_{n-1}}\overline{w^{n-1}}+\dots+\overline{a_{1}}\cdot \bar{w}+\overline{a_{0}} .
\end{align*}
$$

Since the conjugate of a real number is the real number itself,

$$
\overline{p(w)}= a_{n}\cdot \overline{w^{n}}+a_{n-1}\overline{w^{n-1}}+\dots+a_{1}\cdot \bar{w}+a_{0}.
$$

Then, using the theorem in part c, we can write

$$
\begin{align*}
\overline{p(w)}&= a_{n}\cdot \overline{w^{n}}+a_{n-1}\overline{w^{n-1}}+\dots+a_{1}\cdot \bar{w}+a_{0} \\
&= a_{n}\cdot \bar{w}^{n}+a_{n-1}\bar{w}^{n-1}+\dots+a_{1}\cdot \bar{w}+a_{0}. 
\end{align*}
$$

Notice that this is equal to $p(\bar{w}).$ Thus, we have proved

$$
\overline{p(w)}=\bar{0}=0=p(\bar{w}).
$$