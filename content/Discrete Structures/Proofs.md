All reasoning is based on assumptions, called **axioms** and **postulates**, and definitions. 

Sometimes we have undefined terms: ideas we agree on but can't prove. 

# Proven Statements

- theorem: a truth established through a proof
- lemma: proven statement used in proof of theorem
- corollary: proven statement easily derived from theorem

# Counterexamples

A counterexample is a way to disprove a statement by giving an instance where the statement is false.

# Types of Proofs

## Direct Proofs

- most often
- start and beginning, progress to end
- "makes sense"
- often very hard

### Example Direct Proofs

#### Preliminary Ideas:

1. Definition of even and odd
2. $x > y, \, z > t \implies x + z > y + t$ 
3. $a > 0,\, b > 0 \implies ab > 0$
4. $x > y > 0, \, z > t > 0 \implies xz > yt$ 
5. The sum, difference, and product of integers is another integer

#### Proof 1

##### Claim

If a > 0, b > 0, a > b, then $a^{2} > b^{2}$.

##### Lemma

If $x > 0$, $y > 0$, then $x + y > 0$

###### Proof of Lemma

By PI2:

$$
x > y, z > t \implies x + z > y + t \implies a + b > 0
$$

##### Proof of Claim 

$$
a > b \implies a - b > 0
$$

Combining the above equation with the lemma, we use PI3 to get:

$$
\begin{align}
(a + b)(a - b) &> 0 \cdot 0 \\
a^{2} - b^{2} &> 0 \\
a^{2} &> b^{2}
\end{align}
$$

#### Proof 2

##### Claim

If $n$ is odd, then $n^{2}$ is odd.

##### Proof of Claim 

$n$ is odd. By PI1,

$$
n = 2k + 1
$$

for some integer $k$.

Then 

$$
\begin{align}
n^{2} = (2k + 1)^{2} &= 4k^{2} + 4k + 1 \\
&= 2(2k^{2} + 2k) + 1 \\
\end{align}
$$

By PI5 (multiple times) and PI1, we get that $n^{2}$ is odd number as well.

## Indirect Proofs

- used when direct proof isn't possible
- starts by assuming our claim is false
- derive a contradiction
- also called **proof by contradiction**

### Example Proofs

#### Proof 1

##### Claim

If $n^{2}$ is even, then $n$ is even.

##### Lemma

Our previous proof for $n^{2}$ is odd if $n$ is odd will come in handy.

##### Indirect Proof of Claim

Assume $n^{2}$ is even, but $n$ is odd.

By our lemma, $n^{2}$ should then be odd, but that contradicts our assumption. 

#### Proof 2

##### Claim

$\sqrt{ 2 }$ is irrational.

##### Preliminary Ideas

Rational numbers can be expressed as $\frac{m}{n}$, where $m$ and $n$ are relatively prime integers.

##### Proof of Claim

Assume $\sqrt{ 2 }$ is rational.

$$
\begin{align}
\sqrt{ 2 } &= \frac{m}{n} \\
2 &= \frac{m^{2}}{n^{2}} \\
2n^{2} &= m^{2} \\
\implies m &= 4p^{2} \\
\implies n^{2} &= 2p^{2}
\end{align}
$$

That means $m$ and $n$ share a prime factor, 2, but they are supposed to be relatively prime.

## Proof by Contrapositive

In a proof by contrapositive, you claim the contrapositive and prove it because it's logically equivalent to the original claim.

### Example Proof 1

#### Claim

If $n^{2}$ is even, then $n$ is even.

#### Proof

**Contrapositive**: If $n$ is not even, then $n^{2}$ is not even. OR, If $n$ is odd, then $n^{2}$ is odd.

$$
\begin{align}
n^{2} &= (2k+1)^{2} \\
&= 4k^{2} + 4k + 1 \\
&= 2(2k^{2} + 2k ) + 1
\end{align}
$$

Since we proved that $n^{2}$ is odd if $n = (2k+1)$ by the definition of an odd number, we have proved the original claim.

### Example Proof 2

#### Claim

If a product of 2 positive real numbers is greater than 100, then at least one of the numbers is greater than 10.

If $x > 0$, $y > 0$, $xy > 100$, then $x > 10$ or y > 10.

#### Proof

**Contrapositve**: If $x \leq 10$ and $y \leq 10$, then $x \leq 0$ and $y \leq 0$ or $xy \leq 100$

Given that $10 \geq x \geq 0$ and $10 \geq y \geq 0$, by PI4 from earlier, 

$$
xy \leq 100
$$

Since we've proved the contrapositive, the original claim must be true.

## Proof by Cases

Break something up into cases and prove each case.

### Example Proof 1

#### Claim

If $n$ is not divisible by 3, $n^{2}$ has a remainder of 1 when divided by 3.

#### Proof

**Case 1**: $n \equiv 1 \pmod 3$

$$
\begin{align}
n &= 3q + 1 \\
n^{2} &= (3q + 1)^{2} \\
&= 9q^{2} + 6q + 1 \\
&= 3(3q^{2} + 2q) + 1
\end{align}
$$


**Case 2**: $n \equiv 2 \pmod 3$

$$
\begin{align}
n &= 3q + 1 \\
n^{2} &= (3q + 2)^{2} \\
&= 9q^{2} + 12q + 4 \\
&= 3(3q^{2} + 4q + 1) + 1
\end{align}
$$

## Proof By Induction

- can only prove something true for a counting-type subset of integers
- like a row of dominoes
	- prove for first item, first item proves second item, second proves third and so on

### Formal Template

#### Claim

$S(n)$ is true for $n = 1,2,3,\dots$

#### Proof

1. Prove base step $S(1)$
2. Prove $S(n) \implies S(n + 1)$
3. Conclude $S(n)$ is true for all positive integers $n$

### Example Proof 1

#### Claim

Sum of the first $n$ odd numbersr is $n^{2}$.

#### Proof

$S(1)$ is true because $1 = 1^{2}$.

Given that $S(2)$ is $(n - 1)^{2} + (2n - 1)$,

$$
\begin{align}
S(n) &= (n - 1)^{2} + (2n - 1) \\
&= n^{2} - 2n + 1 + 2n - 1 \\
&= n^{2}
\end{align}
$$

Now, we know that $S(n - 1) \implies S(n)$, and since $S(1)$ is true, $S(2)$ must be true and $S(n)$ must be true for all positive integers.

### Example Proof 2

#### Claim

$2n + 1 \leq 2^{n}$ for $n \in \mathbb{Z^{+}}, n\geq 3$ 

#### Proof

**Base Step**: $n = 3$

$$
\begin{align}
S(3): 2 \cdot 3 + 1 &\leq 2^{3} \\
7 &\leq 8 \\
\end{align}
$$

**Inductive Step**

Assume $2n + 1 \leq 2^{n}$.

$$
\begin{align}
2(n + 1) + 1  &= 2n + 3 \\
&= (2n + 1) + 2 \\
&\leq 2^{n} + 2
\end{align}
$$

Now, we prove the lemma $2 < 2^{n}$ for $n \geq 3$

$$
\begin{align}
2 &\leq 2^{n} \\
1 &\leq 2^{n - 1}
\end{align}
$$

The above is always true given $n \geq 3$.

Applying the lemma, we get

$$
\begin{align}
2(n + 1) + 1 \leq 2^{n} + 2^{n} \\
2(n + 1) + 1 \leq 2^{n + 1}
\end{align}
$$

