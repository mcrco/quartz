# Question 1

Let $r\neq 1$ be a real number. Use mathematical induction to show that

$$
\sum_{j=0}^{n}r^{j} = \frac{1-r^{n+1}}{1-r}
$$

## Proof

Consider the statement $S(n)$ given by 

$$
\sum_{j=0}^{n}r^{j} = \frac{1-r^{n+1}}{1-r}.
$$

We will use mathematical induction to show that $S(n)$ is true for all $n\geq 0$.

First, we confirm the base case $S(0)$ is true. Computing, we have

$$
\sum_{j=0}^{n}r^{j} = r^{0} = 1 = \frac{1-r^{0+1}}{1-r}.
$$

Thus, $S(0)$ is indeed true.

Next, we perform the inductive step. We assume that $S(k)$ is true for $k\geq 0$. So, we assume

$$
\sum_{j=0}^{k} r^{j} = \frac{1-r^{k+1}}{1-r}.
$$

We will use this to prove that $S(k+1)$ is true by showing that 

$$
\sum_{j=0}^{k+1} r^{j} = \frac{1-r^{(k+1)+1}}{1-r} = \frac{1-r^{k+2}}{1-r}.
$$

Starting with the LHS of $S(k+1)$ and using our inductive assumption, we have that

$$
\begin{align}
\sum_{j=0}^{k+1}r^{j} &= \sum_{j=0}^{k} r^{j} + r^{k+1} \\
&= \frac{1-r^{k+1}}{1-r} + r^{k+1} \\
&= \frac{1-r^{k+1} + (1-r)r^{k+1}}{1-r} \\
&= 1 - r^{k+1} + r^{k+1} -r^{k+2} \\
&= \frac{1-r^{k+2}}{1-r}.
\end{align}
$$

Thus, using our inductive assumption, we have shown $S(k+1)$ is true.

By induction, we know that the statement $S(n)$ given by $\sum_{j=0}^{n}=\frac{1-r^{n+1}}{1-r}$ is true for all $n \geq 0$.

# Question 2

Consider the function $f(x)=\frac{1}{1-x}$.

a. Compute the first several derivatives of $f$ and use them to conjecture a pattern for $f^{(n)}(x)$.

$$
\begin{align}
f^{0}(x) &= \frac{1}{1-x} = (1-x)^{-1}\\
f^{1}(x) &= (-1)(1-x)^{-2} \\
f^{2}(x) &= (-1)^{2}(1-x)^{-3} \\
f^{3}(x) &= (-1)^{3}(1-x)^{-4}
\end{align}
$$

From this pattern, we see that the pattern for $f^{(n)}(x)$ seems to be 

$$
f^{(n)}(x) = (-1)^{n}(1-x)^{-n-1}.
$$

b. Prove the above pattern using induction.

Consider the statement $S(n)$ given by 

$$
f^{(n)}(x) = (-1)^{n}(1-x)^{-n-1},
$$

where $f(x)$ is the function $f(x)=\frac{1}{1-x}$.

We will use mathematical induction to show that $S(n)$ is true for $n\geq 0$.

First, we confirm that the base case $S(0)$ is true. Computing we have

$$
f^{0}(x) = \frac{1}{1-x} = (-1)^{0}(1-x)^{-0-1}.
$$

Thus, $S(1)$ is indeed true.

Next, we perform the inductive step. Thus, we assume that $S(k)$ is true for some $k\geq 0$. So, we assume that

$$
f^{k}(x) = (-1)^{k}(1-x)^{-k-1}.
$$

We will use this to prove that $S(1)$ is true by showing that 

$$
f^{k+1}(x) = (-1)^{k+1}(1-x)^{-(k+1)-1} = (-1)^{k+1}(1-x)^{-k-2}.
$$

Beginning with the LHS of $S(1)$ and using our assumption, we get

$$
\begin{align}
f^{k+1}(x) &= \frac{d}{dx}f^{k}(x) \\
&= \frac{d}{dx} [(-1)^{k}(1-x)^{-k-1}] \\
&= (-1)^{k}(1-x)^{-k-1-1}(-1) \\ \\
&= (-1)^{k+1}(1-x)^{-k-2}.
\end{align}
$$

Thus, using our inductive assumption, we have show that $S(k+1)$ is true.

By induction, we know that the statement $S(n)$ given by $f^{(n)}(x)=(-1)^{n}(1-n)^{-n-1}$ where $f(x)=\frac{1}{1-x}$ is true for all $n \geq 0$.

# Question 3

Let $x > -1$. Use mathematical induction to prove that 

$$
(1+x)^{n}\geq 1+nx.
$$

## Proof

Consider the statement $S(n)$ given by $(1+x)^{n}\geq 1+nx$. We will use mathematical induction to show that $S(n)$ is true for all integers $n\geq 1$.

First, we confirm the base case $S(1)$ is true. Computing, we have

$$
\begin{gather}
(1+x)^{1} \geq 1+1(x) \\
1+x \geq 1+x.
\end{gather}
$$

Thus, $S(1)$ is true.

Next, we perform the inductive step. We assume $S(k)$ is true for some $k \geq 1$. So, we assume that 

$$
(1+x)^{k} \geq 1+kx.
$$

We will use this to prove that $S(k+1)$ is true by showing that 

$$
(1+x)^{k+1} \geq 1+(k+1)x.
$$

Beginning with the LHS and using our inductive assumption, we have that

$$
\begin{gather}
(1+x)^{k+1} = (1+x)^{k}(1+x) \geq (1+kx)(1+x) \\
(1+kx)(1+x) = 1 + x + kx + kx^{2} = 1 + (k+1)x + kx^{2}\\
x > -1 \implies kx^{2} \geq 0 \implies 1 + (k+1)x + kx^{2} \geq 1+(k+1)x \\
(1+x)^{k+1} \geq 1 + (k+1)x.
\end{gather}
$$

Thus, using our inductive assumption, we have shown that $S(k+1)$ is true.

By induction, we know that the statement $S(n)$ given by $(1+x)^{n} \geq 1 + nx$ given that $x > -1$ is true for all integers $n\geq 1.$