To talk about differentiation, we need to know [[Series]] and 

> [!math|{"type":"theorem","number":"auto","setAsNoteMathLink":false,"_index":0}] Theorem 1.
> If $f \in C([a,b])$, then $f$ is bounded on $[a,b]$.

^621920

`\begin{proof}` `\end{proof}`

> [!math|{"type":"theorem","number":"auto","setAsNoteMathLink":false,"title":"Extremal Value Theorem","label":"extremal-value-theorem","_index":1}] Theorem 2 (Extremal Value Theorem).
> If $f \in C([a,b])$, there exists $c,d \in [a,b]$ s.t. $f(c)=\text{sup}f=\text{max}f$ and $f(d)=\text{inf }f=\text{min }f$.

^fe4b5f

`\begin{proof}` We focus on the first statement because the second follows by considering $-f$.

Let $M=\text{sup }f$ and $g(x)=M-f(x)$. If $M$ is never attained, then $g(x)>0$ for all $x \in [a,b]$. Hence, $\frac{1}{g(x)}$ is well-defined and continuous on $[a,b]$. Therefore, by [[#^621920]] , $\frac{1}{g(x)}$ is bounded on $[a,b]$. That is, $\exists C$ s.t.

$$
\frac{1}{g(x)} = \frac{1}{M-f(x)}<C
.$$

Rearranging gives $f<M-\frac{1}{C}$ for all $x \in [a,b]$, contradicting that $M=\text{sup }f$.
`\end{proof}`

# Derivative

Geometrically, the derivative of a [[Single Variable Calculus/Functions|function]] $f$ at $a$ is the slope of $f$ at $a$. The formal definition uses [[Limits and Continuity|Limits]] to evaluate the slope of $f$ as two points get infinitely close.

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Derivative","label":"derivative","_index":2}] Definition 3 (Derivative).
> A [[Single Variable Calculus/Functions|function]] $f$ defined on a neighborhood of $a \in \mathbb{R}$ is differentiable if
>
> $$
> \lim_{ h \to 0 } \frac{f(a+h)-f(a)}{h}
> $$
> 
> exists. This limit is called the derivative $f$ at $a$, denoted $f'(a)$.

The right limit is

$$
\lim_{ h \to 0^{+} } \frac{f(a+h)-f(a)}{h}.
$$

The left limit is

$$
\lim_{ h \to 0^{-} } \frac{f(a+h)-f(a)}{h}.
$$

$f'(a)$ exists iff left limit and right limit are equal.

# Differentiability

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Differentiable","label":"differentiable","_index":3}] Definition 4 (Differentiable).
> $f$ is differentiable on an open interval $I$ iff $f$ is differentiable at every point of $I$. $f'$ is a function on $I$. $f'$ might not be continuous, but if it is, $f$ is continuously differentiable. $f$ is twice differentiable if $f$ and $f'$ are both continuous. $f^{(n)}$ is the $n$th derivative of $f$. $f$ is $C^{n}$ at $a$ iff $f,f^{(1), \dots f^{(n)}}$ all exist and are continuous at $a$.

## Continuity

> [!math|{"type":"theorem","number":"auto","setAsNoteMathLink":false,"_index":4}] Theorem 5.
> If $f$ is differentiable at $a$, then it is continuous at $a$. 

`\begin{proof}` 

$$
f(a+h)=f(a)=h\left( \frac{f(a+h)-f(a)}{h} \right)
$$

Therefore, since $f'(a)$ exists, 

$$
\lim_{ h \to 0 } f(a+h) = f(a) + \lim_{ h \to 0 } h \cdot f'(a) = f(a).
$$

Hence, $f$ is continuous.
`\end{proof}`

# Properties

If $f,g$ are differentiable at $a$, then 

1. $(f+g)'(a)=f'(a)+g'(a)$
2. $(fg)'(a)=f'(a)g(a) +f(a)g'(a)$
3. $\left( \frac{f}{g} \right)'(a) = \frac{f'(a)g(a)-f(a)g'(a)}{g^{2}(a)}$ if $g(a)\neq 0$

`\begin{proof}` Using the limit definition of derivatives, we can expand and derive each formula`\end{proof}`

# Chain Rule

Let $\varphi=g\circ f$ with $f$ differentiable at $a$ and $g$ differentiable at $b=f(a)$. Then $\varphi$ is differentiable at $a$ and $\varphi'(a)=g'(b)f'(a)$.

`\begin{proof}` Let $k=f(a+h)-f(a)$. Then, $k\to 0$ as $h\to 0$, as $f$ is continuous at $a$. Since $b=f(a)$, we have $f(a+h)=b+k$ and $\varphi(a+h)=g(b+k)$. Thus,

$$
\frac{\varphi(a+h)-\varphi(a)}{h} = \frac{g(b+k)-g(b)}{h} = \frac{g(b+k)-g(b)}{k} \cdot \frac{f(a+h)-f(a)}{h}.
$$

Let $G(t)$ = $\frac{g(b+t)-g(b)}{t}-g'(b)$ for $t\neq 0$.

Then,

$$
g(b+t)-g(t)=t(G(t)+g'(b))
$$

for all $t\neq 0$. Now, we can extend $G$ to all of $\mathbb{R}$ by setting $G(0)=0$. Then, since $g$ is differentiable at $b$, $G$ is continuous at $0$. We then have

$$
\begin{gather}
\frac{\varphi(a+h)-\varphi(a)}{h} = \frac{k}{h}(G(k)+g'(b)) \\
\lim_{ h \to 0 } \frac{\varphi(a+h)-\varphi(a)}{h} = \lim_{ h \to 0 } \frac{k}{h}(G(k)+g'(b)) \\
\varphi'(a) = \lim_{ h \to 0 } \frac{k}{h} \cdot \lim_{ k \to 0 } (G(k)+g'(b)) \\
\varphi'(a) = f'(a) \cdot g'(a)
\end{gather}
$$

`\end{proof}`

## Derivatives of Inverses

One application of chain rule is the formula for the derivative of the inverse:

$$
\frac{d}{dx}f^{-1}(x) = \frac{1}{f'[f^{-1}(x)]}.
$$

`\begin{proof}` Let $y=f^{-1}(x)$, and $x=f(y)$. Then,

$$
\begin{gather}
\frac{d}{dx}x = \frac{d}{dx}f(y) \\
1 = f'(y)\cdot \frac{dy}{dx} \\
\frac{dy}{dx} =\frac{1}{f'(y)}.
\end{gather}
$$

Plugging in $y=f^{-1}(x)$,

$$
\frac{d}{dx}f^{-1}(x)=\frac{1}{f'[f^{-1}(x)]}.
$$
`\end{proof}`

# Extrema

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Extrema","label":"extrema","_index":5}] Definition 6 (Extrema).
> $f$ defined on a set $S$ has a local max at $c \in S$ if there is an open interval $I: c \in I$ s.t. $f(x)\leq f(c)$ for all $x \in I \cap S$. Local minima are defined similarly. Both are extrema of $f$.

> [!math|{"type":"theorem","number":"auto","setAsNoteMathLink":false,"_index":6}] Theorem 7.
> Suppose $f$ is defined on open interval $I$. If $f$ is differentiable and has a local extremum at $a \in I$, then $f'(a)=0$.

^bc5512

`\begin{proof}` Set $Q(x)=\frac{f(x)-f(a)}{x-a}$ if $x\neq a$ and $Q(a)=f'(a)$. Since $f$ is differentiable at $a$, $Q$ is continuous at $a$. We claim $Q(a)$ is 0. 

If $Q(a)>0$, then $Q>0$ on a neighborhood of $a$. But then $f(x)>f(a)$ for $x>a$ and $f(x)<f(a)$ for $x<a$ contradicting that $a$ is a local extremum. The case $Q<0$ also gives a contradiction, so 

$$
Q(a)=f'(a)=0.
$$
`\end{proof}`

# Critical Points

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Critical Point","label":"critical-point","_index":7}] Definition 8 (Critical Point).
> $a \in \mathbb{R}$ is a critical point of a function $f$ which is differentiable at $a$ iff $f'(a)=0$.

Thus, [[#^bc5512]] states that extrema must occur at critical points.

## Rolle's Theorem

> [!math|{"type":"theorem","number":"auto","setAsNoteMathLink":false,"title":"Rolle's Theorem","label":"rolle-theorem","_index":8}] Theorem 9 (Rolle's Theorem).
> Suppose $f$ is cont. and diff. on $[a,b]$ with $f(a)=f(b)$. Then, $\exists c\mid f'(c)=0$.

^5691b2

`\begin{proof}` Suppose $f'\neq 0$ on $(a,b)$. Then, $f$ must have its maximum and minimum at $a$ and $b$ by [[#^bc5512]]. But $f(a)=f(b)$, so we have $f(x)=f(a)$ for all $x \in [a,b]$. But then $f$ is constant and $f'=0$, a contradiction.
`\end{proof}`

## Mean Value Theorem

> [!math|{"type":"theorem","number":"auto","setAsNoteMathLink":false,"title":"Mean Value Theorem","label":"mean-value-theorem","_index":9}] Theorem 10 (Mean Value Theorem).
> If $f \in C([a,b]) \cap D((a,b))$, then there is $c \in (a,b)$ with $f(b)-f(a)=f'(c)(b-a)$. 

Intuitively, this is like saying a car must be driving the average speed at some point during a trip.

`\begin{proof}` Set $h(x)=f(x)(b-a)-x(f(b)-f(a))$ and note that $h(a)=h(b)=f(a)b-af(b)$. By [[#^5691b2]], there is $c$ s.t. $h'(c)=0$. Taking the derivative of $h$, we get

$$
h'(c)=f'(c)(b-a)-(f(b)-f(a)) = 0.
$$
`\end{proof}`
