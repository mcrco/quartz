# Question 1

Let $m\neq 0$ and $b$ be real numbers. Show that there exists a unique real number $x$ such that $mx+b=0$.

## Discussion

We will assume: $m\neq 0$ and $m,b \in \mathbb{R}$.

We will show: $\exists!x: mx+b=0$. 

What we will do: We will solve the equation for $x$ and show there is one unique value.

## Proof

Consider the number $-\frac{b}{m}$. We know this number must be real since both $m$ and $b$ are real, $m$ is not $0$, and the ratio between 2 real numbers is always another real number. Notice that $m(-\frac{b}{m}) + b = -b + b = 0$. Thus, there exists at least one real number such that $mx+b=0$. 

To show that $x$ is unique, we will assume that both $x$ and $y$ satisfy $mx+b=0$ and show that $x=y$. If $mx+b=0$ and $my+b=0$, then $mx+b=0=my+b$. So, $mx+b=my+b$, and $mx=my$. Dividing both sides by $m$ (once again, we can do this since $m \neq 0$ is given), we get $x=y$. Thus, there exists a unique $x$ such that $mx+b=0$ given that $m\neq 0$ and $m,b \in \mathbb{R}$. 

# Question 2

Prove the following biconditional statement.

Let $x$ be a real number. $-1\leq x\leq 1$ if and only if $x^{2}\leq 1$.

## Discussion

We will break up the biconditional statements into two conditional statements:

1. $-1\leq x\leq 1 \implies x^{2}\leq 1$
2. $x^{2}\leq 1 \implies -1\leq x\leq 1$

We can prove the first part by further breaking it down into 2 cases: when $-1\leq x\leq 0$ and when $0 < x \leq 1$. We multiply both inequalities by themselves to prove. We should use proof by contrapositive for the second statement since $x^{2}\leq 1$ is a hard starting point, and $x < -1$ or $x > 1$ is much easier to work with.
## Proof

We will prove the biconditional statement by proving its 2 conditional statements.

We will first prove "If $-1\leq x\leq 1$, then $x^{2}\leq 1$" with casework: when $-1\leq x\leq 0$ and when $0 < x \leq 1$. In the first case, we can multiply $-1\leq x$ by itself to get that $(-1)^{2} \geq x^{2}$ and $x^{2} \geq 1$ since we are multiplying both sides by a negative number. In the second case, we can multiply $x\leq 1$ by itself to once again get $x^{2}\leq 1^{2}$, or $x^{2} \leq 1$. Since both cases point to $x^{2}\leq 1$, we get that $-1\leq x\leq 1 \implies x^{2}\leq 1$.

For the second statement, "If $x^{2}\leq 1$ then $-1\leq x\leq 1$", we will do a proof by the contrapositive. The contrapositive is "If $x < -1$ or $x > 1$, then $x^{2} > 1$." We can prove this statement with casework as well. When $x<-1$, we can multiply the inequality by itself to get that $x^{2}>(-1)^{2}$ and thus $x^{2} > 1$. We flip the sign because we are multiplying both sides by a negative value since $x < -1 < 0$. For $x > 1$, we multiply the inequality by itself to get that $x^{2} > 1^{2}$ and $x^{2} > 1$ as well. Thus, we have proven "If $x < -1$ or $x > 1$, then $x^{2} > 1$", which is the contrapositive of "If $x^{2} \leq 1$, then $-1 \leq x \leq 1$."

Since we have proven both the conditional statements, "$-1\leq x\leq 1$ if and only if $x^{2}\leq 1$" must be true.
# Question 3

Prove $m, n$ have same parity if and only if $m+n$ is even.
## Discussion

We break the biconditional statements into the following parts:

1. $m, n$ have same parity $\implies$ $m+n$ is even.
2. $m+n$ is even $\implies$ $m,n$ have same parity.

For the first part, we can just use casework for when $m$ and $n$ are both even or both odd and show that their sum is always going to be even. For the second part, we can use proof by contrapositive to make things easier.

## Proof

To prove this biconditional statement, we will prove its individual conditional statements.

For the first statement "If $m$ and $n$ have the same parity, then $m + n$ is even", we will use casework on the shared parity of $m$ and $n$. In the case that both $m$ and $n$ are odd, we can let $m=2a+1$ and $n=2b+1$. Summing them, $m+n = 2a+1 + 2b+ 1 = 2a + 2b + 2 = 2(a+b+1)$. Since we can write $m+n$ as $2$ multiplied by some whole number ($a,b,1$ are all whole numbers), $m+n$ must be even if $m$ and $n$ are odd. In the case that $m$ and $n$ are even, we can let $m=2a$ and $n=2b$. Summing them, $m+n=2a+2b=2(a+b)$. Once again, since we can write $m+n$ as a multiple of $2$, $m+n$ must be even if both $a$ and $b$ are even. Since $m+n$ is even if $m$ and $n$ are both even or odd, we can conclude $m+n$ is even if $m$ and $n$ have the same parity.

For the second statement, "If $m + n$ is even, then $m$ and $n$ have the same parity", we will prove its contrapositive: "if $m$ and $n$ don't have the same parity, then $m + n$ is odd." We will start by letting $m=2a+1$ and $n=2b$, so that we have 2 numbers of different parities. So, $m+n=2a+1+2b=2(a+b) + 1$. Since $m+n$ is $1$ more than a multiple of $2$, we get that $m+n$ must be odd if $m$ is odd and $n$ is even or vice versa. By proving the contrapositive, we have proven that the second statement "$m+n$ is even $\implies$ $m,n$ have the same parity."

Since we have proven both conditional statements, we have successfully proven the biconditional statement "Whole numbers $m$ and $n$ have the same parity if and only if $m+n$ is even."

# Question 4

Let $m$ and $n$ be whole numbers. If $m\cdot n$ is odd, then $m$ and $n$ are both odd.

## Discussion

The contrapositive is "If $m$ and $n$ are not both odd, then $m\cdot n$ is even." We can rewrite one of the numbers as a multiple of 2, and then show that the product of the two numbers has to be even as well.
## Proof

We will prove this proposition with a proof by contrapositive. The contrapositive is "If $m$ and $n$ are not both odd, then $m\cdot n$ is even." 

Since we know at least one of $m$ or $n$ must be even, we can arbitrarily let one of the two numbers, say $m$, be written as $2k$, where $k$ is a whole number. The product is $2k\cdot n$, or $2(kn)$. Both $k$ and $n$ are whole numbers, so the product $m\cdot n$ must be a multiple of 2 and even. Since we have proven the contrapositive, we have proven the original statement "if $k$ and $n$ are 2 odd whole numbers, the $m$ and $n$ are both odd."
# Question 5

Every odd whole number can be written as the difference of two perfect squares.

a. For the odd whole numbers $n = -3, -1, 1, 3, 5, 7, 9$, write $n$ as the difference of two perfect squares.

$$
\begin{align}
-3 &= 1^{2}-2^{2} \\
-1 &= 0^{2}-1^{2} \\
1 &= 1^{2}-0^{2} \\
3 &= 2^{2}-1^{2} \\
5 &= 3^{2}-2^{2} \\
7 &= 4^{2}-3^{2} \\
9 &= 5^{2}-4^{2}
\end{align}
$$

b. Use any pattern in a to help write a proof for the proposition.
## Discussion

The pattern here seems to be every odd number is the difference between the squares of consecutive numbers. We will use the expansion of $(n+1)^{2}$ in our proof and subtract $n^{2}$ to get the solve for the general form of an odd number.

## Proof

Let $n$ be an odd number. We can then write $n$ as $2k+1$ for some whole number $k$. 

Notice that $2k + 1=(k^{2}+2k+1)-k^{2} = (k+1)^{2}-k^{2}$. Therefore, we can write any odd number $n$ as the difference of the squares of 2 consecutive numbers.