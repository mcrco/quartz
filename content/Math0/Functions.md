# Question 1

Let $m\neq 0$ and $b$ be real numbers and consider the function $f: \mathbb{R} \to \mathbb{R}$ given by $f(x)=mx+b$.

a. Prove that $f$ is a bijection.

## Discussion

We want to show that $f$ is both injective and surjective. 

To show $f$ is injective, we need to show that if $f(t_{1}) = f(t_{2})$, $t_{1}=t_{2}$. We will start by assuming $f(t_{1})=f(t_{2})$. Since $f(t_{1})=mt_{1}+b$ and $f(t_{2})=mt_{2}+b$, $mt_{1}+b=mt_{2}+b$. Then we will solve for the equation and show $t_{1}= t_{2}$.

To show f is surjective, we need to show that for $t \in \mathbb{R}$, $\exists s \in \mathbb{R}$  such that $t=f(s)$. We will let $f(s)=ms+b$ and solve $t=ms+b$ to show that $s \in \mathbb{R}$.

## Proof

To prove that $f$ is a bijection, we will prove that $f$ is both injective and surjective.

To prove $f$ is injective, we will assume $f(t_{1}) = f(t_{2})$. Since $f(x)=mx+b$, $f(t_{1})=mt_{1}+b$ and $f(t_{2})=mt_{2}+b$. Thus, $mt_{1}+b=mt_{2}+b$. Subtracting $b$ from both sides, $mt_{1}=mt_{2}$. Dividing by $m$, $t_{1}=t_{2}$, so we can conclude $f$ is injective.

To prove $f$ is surjective, we will assume $t \in R$ and show that $\exists s \in \mathbb{R}$ such that $f(s)=t$. Since $f(x)=mx+b$, $f(s)=ms+b$. Equating $f(s)=t=ms+b$, we get that $s=\frac{t-b}{m}$.  Since $t,b,m \in \mathbb{R}$, $s \in \mathbb{R}$ must also be true. Thus, we can conclude $f$ is surjective.

Since we have proven $f$ is both injective and surjective, we can conclude that $f$ is a bijection.

b. Find the inverse $f^{-1}$ and show it's an inverse by demonstrating that

$$
f^{-1}(f(x)) = x
$$

## Discussion

We can simply let $y = f(x)$ and swap $x$ and $y$ in the equation $y=mx+b$ to solve for $x$ in terms of $y$. The new $y$ is the inverse. Then, to demonstrate that it is in fact the inverse, we plug the value of $f(x)$ into the function $f^{-1}(x)$ to make sure the resulting value is $x$.

## Proof

Let $y=f(x)$. Thus, $f(x)=y=mx+b$. To find the inverse of $f(x)$, we can simpy swap $y$ and $x$ and solve for $y$ in terms of $x$ again to find the inverse. Solving, we get

$$
\begin{gather}
y=mx+b \to x = my+b \\
x - b = my \\
\frac{x-b}{m} = y \\
y = \frac{1}{m}x - \frac{b}{m}.
\end{gather}
$$

and thus the inverse $f^{-1}(x) = \frac{1}{m}x - \frac{b}{m}$ .

To prove that it truly is the inverse, we validate that $f^{-1}(f(x)) = x$. Plugging in, we get

$$
\begin{align}
f^{-1}(f(x)) &= f^{-1}(mx+b) \\
&= \frac{1}{m}(mx+b) - \frac{b}{m} \\
&= x + \frac{b}{m} - \frac{b}{m} \\
&= x.
\end{align}
$$

Since the equation is true, $f^{-1}(x) = \frac{1}{m}x - \frac{b}{m}$.
# Question 2

Let $\gamma,\rho \in R$ be real numbers such that $\gamma \cdot \rho\neq 1$. Let $\mathbb{R}-\{ \gamma \}$ and $\mathbb{R-\{ -\rho \}}$ be the set of all real numbers $\mathbb{R}$ except for $\gamma$ and $-\rho$, respectively. Consider the function $f:\mathbb{R}-\{ -\rho \} \to \mathbb{R} - \{ \gamma \}$ given by 

$$
f(x) = \frac{\gamma x+1}{x+\rho}.
$$

Show that $f$ is a bijection.

## Discussion

We want to show $f$ is both injective and surjective. 

To show $f$ is injective, we will assume $f(t_{1})=f(t_{2})$. Then, we will plug in $t_{1}$ and $t_{2}$ into the formula for $f(x)$, equate the 2 expressions, solve the equation, and show that $t_{1} = t_{2}$.

To show that $f$ is surjective, we have to show for any element $t \in \mathbb{R-\{ \gamma \}}$, there exists $s \in R - \{ -\rho \}$ such that $f(s)=t$. We will plug in $s$ into the formula for $f$ and solve for $s$ in terms of $t$ and show that $s$ is a ratio between 2 real numbers, meaning $s \in \mathbb{R}$. 

## Proof

To prove $f$ is a bijection, we will prove $f$ is both injective and surjective.

For injectivity, we will let $t_{1},t_{2} \in \mathbb{R} - \{ -\rho \}$ and assume that $f(t_{1}) = f(t_{2})$. Since $f(x)=\frac{\gamma x+1}{x+\rho}$, $f(t_{1})=\frac{\gamma t_{1}+1}{t_{1}+\rho}$ and $f(t_{2})=\frac{\gamma t_{2}+1}{t_{2}+\rho}$. Plugging these expressions into $f(t_{1})=f(t_{2})$, we get $\frac{\gamma t_{1}+1}{t_{1}+\rho}=\frac{\gamma t_{2}+1}{t_{2}+\rho}$. We know that the denominator can't be $0$, since $t_{1},t_{2}\neq\rho$, so we can multiply both sides by both denominators to get $(\gamma t_{1}+1)(t_{2}+\rho)=(\gamma t_{2}+1)(t_{1}+\rho)$. Distributing, we get $\gamma t_{1}t_{2}+\gamma t_{1}\rho+t_{2}+\rho=\gamma t_{1}t_{2} + \gamma t_{2}\rho+t_{1}+\rho$. Simplifying, we get $\gamma t_{1}\rho - t_{1}=\gamma t_{2}\rho - t_{2}$. Dividing both sides by $\gamma\rho-1$, we get $t_{1}=t_{2}$. Since $t_{1}=t_{2}$, we can conclude that $f$ is injective.

For surjectivity, let $t\in \mathbb{R} - \{ \gamma \}$. To prove $t$ has a pre-image $s \in \mathbb{R} - \{ -\rho \}$, let $f(s)=t$. Since $f(s)=\frac{\gamma s+1}{s+\rho}=t$, we can solve for $s$ in terms of $t$. 

$$
\begin{gather}
\frac{\gamma s+1}{s+\rho}=t \\
\gamma s+1 = st+\rho t \\
\gamma s-st=\rho t-1 \\
s(\gamma-t) = \rho t-1 \\
s = \frac{\rho t-1}{\gamma-t}
\end{gather}
$$

Since $t\neq\gamma$, we know that there exists $s \in \mathbb{R}$, and since $s+\rho$ was in the denominator, we know $s\neq -\rho$. Thus, there exists an $s \in \mathbb{R-\{ -\rho \}}$ for every $t\in\mathbb{R-\gamma}$.

Since we have proven that $f$ is both injective and surjective, we can conclude that $f$ is a bijection.

# Question 3

Let $f:S\to T$ and $g:T\to R$ be functions. Show that if $g \circ f$ is injective, then $f$ is injective.

## Discussion

We want to show that $f(x_{1}) = f(x_{2})$, then $x_{1}=x_{2}$. Since we know $g$ is well-defined, if $f(x_{1})=f(x_{2})$, then $g(f(x_{2}))=g(f(x_{2}))$. Since we know $g\circ f$ is injective, if $g(f(x_{1}))=g(f(x_{2}))$ , then $x_{1}=x_{2}$. We can use this to conclude $f$ is injective.

## Proof

Assume $f(x_{1}) = f(x_{2})$. Since $g$ is a function and therefore well-defined, $g(f(x_{1}))=g(f(x_{2}))$. Since we know $g \circ f$ is injective, if $g \circ f(x_{1}) = g \circ f(x_{2})$, then $x_{1}=x_{2}$. Thus, we can conclude that if $f(x_{1})=f(x_{2})$, then $x_{1} = x_{2}$, and $f$ is injective.

# Question 4

Let $C([0,1])$ be the set of all real, continuous functions on the interval $[0,1]$. That is,

$$
C([0,1]) = {f|f:[0,1] \to \mathbb{R} \text{ is a continuous function}}
$$

Consider the function $\varphi:C([0,1]) \to \mathbb{R}$ given by

$$
\varphi(f) = \int_{0}^{1} f(x) \, dx.
$$

a. Show that the function $\varphi$ is surjective by showing that for every $a \in \mathbb{R}$, there exists a pre-image $f \in C([0,1])$ such that $\varphi(f) = a$.

## Discussion

To prove surjectivity, we want to show there is some continuous function whose definite integral from $0$ to $1$ evaluates to $a$ for every $a \in \mathbb{R}$. To do this, we can just consider a constant function $g(x) = a$.

## Proof

Let $a \in \mathbb{R}$. Consider the constant function $g(x)=a$. Evaluating $\varphi(g)$, we get

$$
\begin{align}
\varphi(g) &= \int_{0}^{1} a \, dx \\
&= [ax]_{0}^{1} \\
&= a
\end{align}
$$

Since we have successfully shown that for every $a \in \mathbb{R}$, applying $\varphi$ to the constant function $g(x)=a$ gives us $a$, we have proven that there exists a continuous function in $C([0,1])$, the domain of $\varphi$, for every value in the codomain of $\varphi$.

b. Show that the function $\varphi$ is not injective by finding 2 distinct functions $f,g \in C([0,1])$ such that $\varphi(f) = \varphi(g)$.

## Discussion

Not much to discuss, just need to come up with 2 functions that have the same integral but are different. For me, the first two that came to mind were $-x+1$ and $x$.

## Proof

To prove $\varphi$ is not injective, consider the functions $a(x) = -x + 1$ and $b(x)=x$. Evaluating $\varphi(a)$ and $\varphi(b)$, we get

$$
\begin{align}
\varphi(a)&=\int_{0}^{1} -x + 1 \, dx \\
&= \left[ -\frac{x^{2}}{2} + x \right]_{0}^{1} \\
&= -\frac{1}{2}+1 \\
&= \frac{1}{2} \\
\varphi(b) &= \int_{0}^{1} x \, dx  \\
&= \left[ \frac{x^{2}}{2} \right]_{0}^{1} \\
&= \frac{1}{2}
\end{align}
$$

Since $\varphi(a)=\varphi(b)$ but $a$ and $b$ are different functions, we can conclude $\varphi$ is not injective.