# Question 1

Let $a,b,c \in \mathbb{N}$. Show that if $a+b=a+c$, then $b=c$.
## Proof

We will perform a proof by induction. Consider the statement $P(a)$ given by if $a+b=a+c$, then $b=c$ for $a,b,c \in \mathbb{N}$.

We will start by proving the base case, $S(0).$ Since $x+0=x$ for all $x \in \mathbb{N}$ by definition, we know that by commutativity $0+b=b+0=b$ and $0+c=c+0=c$. Thus, $a+b=a+c\implies 0+b=0+c \implies b=c$. 

Now, we perform the inductive step. Assume that $P(k)$ is true for $k \in N, k\geq 0$. So, we assume that if $k+b=k+c$, then $b=c$. We will use this information to prove $P(S(k))$, which is if $S(k)+b=S(k)+c$, then $b=c$. 

We start with the equation

$$
\begin{gather*}
S(k)+b=S(k)+c. \\
\end{gather*}
$$

By commutativity, we get

$$
b+S(k)=c+S(k). \\
$$

By the definition of addition, we get

$$
S(b+k)=S(c+k). \\
$$

By the properties of the successor function, we get

$$
b+k=c+k. \\
$$

By commutativity, we get

$$
k+b=k+c.
$$

Since we have reduced $P(S(k))$ to $P(k)$ which we know is true, we can conclude that $P(k)\implies P(S(k))$. Thus, by induction, we know the statement if $a+b=a+c$, then $b=c$ is true.

# Question 2

a. Show that $a+a=2\cdot a$.

## Proof

By the reflexivity axiom, if we prove $2\cdot a=a+a$, we prove $a+a=2\cdot a$.

By commutativity, we know that $2\cdot a=a\cdot{2}$. By the definition of multiplication, we know that $a\cdot 2= a\cdot S(1)=a+(a\cdot 1)=a+(a\cdot S(0))=a+(a+(a\cdot 0))=a+a+0=a+a.$ 
Since we have proved $a\cdot 2=2\cdot a=a+a$, we have proven $a+a=2\cdot a$.

b. Show that $a+a+a\dots+a=n\cdot a$.

## Proof

Once again, we can prove the statement by proving the reflected statement with a commutated product: $a\cdot n=a+a\dots+a$. We will do a proof by induction. Consider the statement $S(n)$ given by $a\cdot n=a+a+\dots+a$ $n$ times for $n\geq 0$. 

The base case, $S(0)$, is given by $a\cdot 0=0$. This is true by the definition of multiplication.

Now, we perform the inductive step. Assume that $S(k)$ is true for $k\geq 0$. Thus,

$$
a\cdot k=a+a+\dots+a
$$

$k$ times. We will use this to prove $S(k+1):$

$$
a\cdot(k+1)=a+a+\dots+a
$$

$k+1$ times. 

Starting with the LHS of $S(k+1)$, we use the distributive property to get

$$
\begin{align*}
a\cdot(k+1)&=a\cdot k+a\cdot 1 \\
&= a\cdot k+a\cdot S(0) \\
&= a\cdot k+a+a\cdot 0 \\
&= a\cdot k+a.
\end{align*}
$$

Since we know that $a\cdot k=a+a+\dots+a$ $k$ times, $a\cdot k+a = a+a+\dots+a$ $k+1$ times. Thus, we have proven that $S(k+1)$ is true.

By mathematical induction, we have proven the statement $S(n)$ given by $a\cdot n=a+a+\dots+a$ $n$ times, and thus, we have proven $a+a\dots+a$ $n$ times equals $n\cdot a$.

# Question 3

a. Let $a,b,c \in N$ such that $c\neq 0$ and $a=b\cdot c$. Prove that $b\leq a$. 

By the definition of multiplication, we get that $b\cdot c=b + b\cdot S^{-1}(c)$.  Since we know that $c\neq 0$ and $c \in \mathbb{N}$, $S^{-1}(c) \in \mathbb{N}$. Thus, $a=b+b\cdot S^{-1}(c)$ for $a,b,S^{-1}(c) \in \mathbb{N}$. We know that $b \cdot S^{-1}(c) \in \mathbb{N}$ because $\mathbb{N}$ is closed under multiplication. Therefore, $a\geq b$ and $b\leq a$ by the definition of $\leq$.

b. Prove that $a\leq a$.

Since $a+0\leq a$, we can satisfy the definition of $\leq$, which is $x+y\leq z$ for $x,y,z \in \mathbb{N}$ if we just let $x=z=a$ and $y=0$.

c. Prove that if $a\leq b$ and $b\leq c$, then $a\leq c$.

Assume that $a\leq b$ and $b\leq c$. Thus, for some natural number $p \in \mathbb{N}$, $a+p=b$, and for some number $q \in \mathbb{N}$, $b+q=c$. Substituting $b=a+p$ in the second equation, we get $a+p+q=c$. Since $p+q \in \mathbb{N}$, we can let $r=p+q$ for some $r \in \mathbb{N}$. Thus, $a+r=c$, and we satisfy the conditions for $a\leq c$.

d. Prove that if $a\leq b$ and $b \leq a$, then $a=b$. 

Assume that $a\leq b$ and $b\leq a$. Thus, $a+p=b$ and $b+q=a$ for some $p,q \in \mathbb{N}$. Substituting the first equation into the second, we get

$$
a+p+q=a.
$$

We can rewrite this as

$$
a+(p+q)=a+0.
$$

By the statement we proved in problem 1, we can conclude

$$
p+q=0.
$$

Now we want to prove that $p$ and $q$ are both $0$. We will do this with a proof by contradiction. Suppose that $p\neq 0$. Let $q=S(r)$ for $q \in \mathbb{R}$. Then,

$$
p+S(r)=0.
$$

By the definition of addition, we can write

$$
S(p+r)=0.
$$

However, we know this isn't true because of the Peano axioms, which state that $0$ is not a successor of any other natural number. Thus, $p=0$. Then,

$$
\begin{gather*}
a+p=b \\
a+0=b \\
a=b.
\end{gather*}
$$

Thus, if $a\leq b$ and $b\leq a$, then $a=b$.