# Question 1

Let $a,b \in \mathbb{Z}$. Show that $4|a^{2}-b^{2}$ if and only if $a$ and $b$ are of the same parity.

## Proof

We will prove the biconditional statement by proving two conditional statements: if $a$ and $b$ are of the same parity then $4|a^{2}-b^{2}$ and if $4|a^{2}-b^{2}$ then $a$ and $b$ are of the same parity

For the first conditional statement, assume that $a$ and $b$ are of the same parity. We will now do casework on whether both are odd or even. If both $a$ and $b$ are even, we can let $a=2m$ and $b=2n$. Plugging in $2m$ for $a$ and $2n$ for $b$,

$$
\begin{align}
a^{2}-b^{2}&=(2m)^{2}-(2n)^{2} \\
&= 4m^{2}-4n^{2} \\
&=4(m^{2}-n^{2})
\end{align}
$$

Since we can rewrite $a^{2}-b^{2}$ as $4$ multiplied by another integer (we know this because $\mathbb{Z}$ is closed under addition and subtraction), $4|a^{2}-b^{2}$ if $a$ and $b$ are both even. Now, if $a$ and $b$ are both odd, we can plug in $a=2m+1$ and $b=2n+1$:

$$
\begin{align}
a^{2}-b^{2}&=(a+b)(a-b) \\
&=(2m+1+2n+1)(2m+1-[2n+1]) \\
&= (2m+2n+2)(2m-2n) \\
&= [2(m+n+1)][2(m-n)] \\
&= 4(m+n+1)(m-n).
\end{align}
$$

Since we can once again write $a^{2}-b^{2}$ as an integer multiple of $4$, if $a$ and $b$ are both odd, $4|a^{2}-b^{2}$. Since we have proven that $4|a^{2}-b^{2}$ if $a$ and $b$ are both odd and both even, we can conclude that if $a$ and $b$ are the same parity, $4|a^{2}-b^{2}$.

For the second conditional statement, we will prove it by proving its contrapositive: if $a$ and $b$ are not of the same parity, then $4|a^{2}-b^{2}$ is false. We will now do casework on whether $a$ is even and $b$ is odd or vice versa. If $a$ is even and $b$ is odd, we can let $a=2m$ and $b=2n+1$, where $m$ and $n$ are also integers. Then,

$$
\begin{align}
a^{2}-b^{2}&=(2m)^{2}-(2n+1)^{2} \\
&= 4m^{2}-4n^{2}-4n-1 \\
&= 4(m^{2}-n^{2}-n)-1.
\end{align}
$$

We can conclude that if $a$ is even and $b$ is odd, then $a^{2}-b^{2}$ is not divisible by $4$ since it always $1$ less than a multiple of $4$. If $a$ is odd and $b$ is even, we can let $a=2m+1$ and $b=2n$. Then,

$$
\begin{align}
a^{2}-b^{2}&=(2m+1)^{2}-(2n)^{2} \\
&=4m^{2}+4m+1-4n^{2} \\
&=4(m^{2}+m-n^{2}) + 1
\end{align}
$$

Since $a^{2}-b^{2}$ is always going to be $1$ less than a multiple of $4$, we can conclude that if $a$ is odd and $b$ is even, then $4|a^{2}-b^{2}$ is false. By proving that if $a$ and $b$ are different parities, then $4 |a^{2}-b^{2}$ is false for both cases, we have proven that if $4|a^{2}-b^{2}$, then $a$ and $b$ are of the same parity by proving its contrapositive.

Since we have proven both conditional statements, we have proven that $4|a^{2}-b^{2}$ if and only if $a$ and $b$ are the same parity.

# Question 2

a. Let $a \in \mathbb{Z}$. Show that $3|a$ if and only if $3|a^{2}$.

## Proof

We will prove the biconditional statement by proving its two conditional statements: 

1. if $3|a$, then $3|a^{2}$.
2. if $3|a^{2}$, then $3|a$.

To prove the first conditional statement, assume $3|a$. Thus, we can let $a=3k$ for some $k \in \mathbb{Z}$. Substituting $3k$ for $a$, we get $a^{2}=(3k)^{2}=9k^{2}=3(3k^{2})$. Since $k \in \mathbb{Z}$, $3k^{2} \in \mathbb{Z}$, we can conclude $a^{2}$ is an integer multiple of $3$ and $3|a^{2}$.

For the second conditional statement, we will prove its contrapositive: if $3$ does not divide $a$, then $3$ does not divide $a^{2}$. Assume $3$ does not divide $a$. There are 2 cases in which this is true: when $a=3k+1$ for some $k \in \mathbb{Z}$ and when $a=3k+2$ for some $k \in \mathbb{Z}$. 

In the first case, $a^{2}=(3k+1)^{2}=9k^{2}+6k+1=3(3k^{2}+2k)+1$. Since $k \in \mathbb{Z}$, $3k^{2} \in \mathbb{Z}$ and $2k \in \mathbb{Z}$. Thus, $a^{2}$ is $1$ greater than an integer multiple of $3$ and $3|a^{2}$ cannot be true. 

In the second case, $a^{2}=(3k+2)^{2} = 9k^{2}+12k+4 = 3(3k^{2}+4k+1)+1$. Since $k \in \mathbb{Z}$, $3k^{2},4k \in \mathbb{Z}$. Thus, $a^{2}$ is always $1$ greater than an integer multiple of $3$ and $3|a^{2}$ cannot be true.

Since we have proven that $3|a^{2}$ cannot be true in both cases if $3|a$ is false, we have proven that if $3|a^{2}$, then $3|a$ by its contrapositive.

By proving both conditional statements, we have proven that $3|a$ if and only if $3|a^{2}$.

b. Use (a) to show that $\sqrt{ 3 }$ is irrational.

## Proof

We will use a proof by contradiction. Assume $\sqrt{ 3 }$ is rational. Then, $\sqrt{ 3 } = \frac{m}{n}$ for some $m,n \in \mathbb{Z}$. With some algebraic manipulation,

$$
\begin{gather}
\sqrt{ 3 } = \frac{m}{n} \\
(\sqrt{ 3 })^{2} = \left( \frac{m}{n} \right)^{2} \\
3 = \frac{m^{2}}{n^{2}}. \\
\end{gather}
$$

We see that $\frac{m^{2}}{n^{2}}=3$, implying that $3|\frac{m^{2}}{n^{2}}$ is true since every number divides itself. However, from (a), we know that if $3|\frac{m^{2}}{n^{2}}$ is true, then $3|\sqrt{ \frac{m^{2}}{n^{2}} }$ should be true, but that can't be true since we know $\frac{m^{2}}{n^{2}}$ isn't even an integer from $\sqrt{ \frac{m^{2}}{n^{2}} }=\frac{m}{n}=\sqrt{ 3 }$. Thus, $\sqrt{ 3 }$ cannot be expressed as a ratio of 2 integers $m$ and $n$.

# Question 3

Let $a,b \in \mathbb{R}$. Show that if $a+b$ is rational, then $a$ is irrational or $b$ is rational.

## Proof

We will prove the conditional statement by proving its contrapositive: If $a$ is irrational or $b$ is rational is false, then $a+b$ is irrational. DeMorgan's Logic Laws state that $\neg(p\lor q) \equiv \neg p \land \neg q$, so we can rewrite the contrapositve as if $a$ is rational and $b$ is irrational, then $a+b$ is irrational.

Assume $a$ is rational and $b$ is irrational. We will do a proof by contradiction. Assume $a+b$ is rational. Let $a = \frac{m}{n}$ and $a+b=\frac{p}{q}$ for $m,n,p,q \in \mathbb{Z}$. Then,

$$
\begin{gather}
a+b=a+b \\
\frac{m}{n} + b = \frac{p}{q} \\
b = \frac{p}{q} - \frac{m}{n} \\
b = \frac{pn-mq}{nq}
\end{gather}
$$

However, we know this is impossible since $b$ is an irrational number. Thus, if $a$ is rational and $b$ is irrational, $a+b$ is irrational. By proving the contrapositive, we have proven original statement: if $a+b$ is rational, then $a$ is irrational or $b$ is rational.