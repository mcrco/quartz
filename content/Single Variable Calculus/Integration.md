# Intuition

Intuitively, the integral of a function is the area under the curve. Let's try approximating it.

First, we define

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Partition","label":"partition","_index":0}] Definition 1 (Partition).
> A partition of $[a,b]$ is a collection of points $t_{0}=a<t_{1}<t_{2}<\dots<t_{n-1}<b=t_{n}$. 

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Step Function","label":"step-function","_index":1}] Definition 2 (Step Function).
> A [[Single Variable Calculus/Functions|function]] $S$ defined on $[a,b]$ is a step function if there is a partition $P$ and constants $c_{1},\dots, c_{n}$ s.t. $S(x)=c_{j}$ for $x \in [t_{j-1},t_{j})$ and $S(t_{n})=c_{n}$.

If we approximate a function as a step function for a given partition, we get that the integral is

$$
\int_{a}^{b} S(x) \, dx = \sum_{j=1}^{n}c_{j}(t_{j}-t_{j-1}).
$$

This approximation is a Riemann sum. It is equivalent to splitting up the area under the curve as rectangles, and then summing the areas of the rectangles.

![[Pasted image 20231103005227.png]]

If we choose $c_{j}=\text{inf}_{f}([t_{j-1},t_{j}])$, where $\text{inf}_{f}$ is the [[Real Numbers#^56a279|infimum]]  of the function $f$ for a given interval, then we get the lower Riemann Sum:

$$
L(f, P) = \sum_{j=1}^{n}\text{inf}_{f}([t_{j-1}, t_{j}]) \cdot (t_{j}-t_{j-1})
$$

If we choose $c_{j}=\text{sup}_{f}([t_{j-1},t_{j}])$, then we get the upper Riemann Sum:

$$
U(f,P) = \sum_{j=1}^{n}\text{sup}_{f}([t_{j-1}, t_{j}]) \cdot (t_{j}-t_{j-1})
$$

# Formal Definition

To define integration formally, we need more definitions.

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Refinement","label":"refinement","_index":2}] Definition 3 (Refinement).
> If $P,P'$ are partitions of $[a,b]$, $P'$ is a refinement of $P$ iff the set of points in $P$ is contained in the sets of points in $P'$.

Note that $P,P'$ have a common refinement $P''$. Considering common refinements, we can show that the sum and product of step functions are step functions.

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Span","label":"span","_index":3}] Definition 4 (Span).
> If $f$ is bounded on $[a,b]$, its span is $\text{span}_{f}([a,b])=\text{sup}([a,b])-\text{inf}_{f}([a,b])$, where $\text{sup}_{f}$ and $\text{inf}_{f}$ are the supremum and infimum. 

Now, we can define

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Integrable","label":"integrable","_index":4}] Definition 5 (Integrable).
> A bounded function $f$ on $[a,b]$ is integrable iff for every $\epsilon>0$, there is a partition $P:t_{0}=a<t_{1}<\dots<b=t_{n}$ s.t. the sum 
> $$
> \Delta_{f}(P)=\sum_{j=1}^{n}(t_{j}-t_{j-1})\text{span}_{f}([t_{j-1},t_{j}]) < \epsilon
> $$

Notice that $\Delta_{f}(P)$ is the difference between the upper Riemann sum and the lower Riemann sum.

Provided there is a sequence of partitions $P$ s.t. $\Delta_{f}(P)\to 0$, the function is (Riemann) integrable.

## Riemann Sum-Based Definition

Notice that if $P'$ is a refinement of $P$, then 

$$
\begin{align}
L(f,P) &\leq L(f,P') \\
U(f,P) &\geq U(f,P').
\end{align}
$$

Define the sets

$$
\begin{align}
\mathcal{L}(f) &= \{ L(f,P), P\text{ is a partition on } [a,b] \} \\
\mathcal{U}(f) &= \{ U(f,P), P\text{ is a partition on } [a,b] \}.
\end{align}
$$

> [!math|{"type":"lemma","number":"auto","setAsNoteMathLink":false,"_index":5}] Lemma 6.
> $\exists \underline{I} = \text{sup }\mathcal{L}(f)$ called the lower integral of $f$. $\exists \overline{I} = \text{inf }\mathcal{U}(f)$ called the upper integral of f called the upper integral of $f$.

`\begin{proof}` We will show $\mathcal{L}$ is bounded above and $\mathcal{U}$. Suppose $P,P'$ are partitions of $[a,b]$. Let $P''$ be a common refinement. Then,

$$
L(f,P) \leq L(f,P'') \leq U(f,P'') \leq U(f,P').
$$

Thus, $\mathcal{L}$ is bounded above by $U(f,P')$ and $\mathcal{U}$ is bounded below by $L(f,P)$.
`\end{proof}`
Note that 

$$
\underline{I}(f)\leq \overline{I}(f).
$$

> [!math|{"type":"lemma","number":"auto","setAsNoteMathLink":false,"title":"Integrable","label":"integrable","_index":6}] Lemma 7 (Integrable).
> A bounded function $f$  is integrable over $[a,b]$ iff $\underline{I}(f)= \overline{I}(f)$.

`\begin{proof}` If $f$ is integrable, then $\Delta_{f}(P) = U(f,P) - L(f,P)$ can be arbitrarily small, so $\underline{I}(f)=\overline{I}(f)$.

Conversely, if $\underline{I}(f)=\overline{I}(f)$, then for any $\epsilon>0$, exists $P,P'$ s.t. $U(f,P')-L(f,P)<\epsilon$. Taking a common refinement $P''$, we get 

$$
U(f,P'')-L(f,P'') < \epsilon,
$$

so $f$ is integrable.
`\end{proof}`

When $\underline{I}(f)=\overline{I}(f)$, the integral of $f$ is $I(f)=\underline{I}(f)=\overline{I}(f)$.

# Definite Integral

$$
\int_{a}^{b} f(x) \, dx .
$$

- definite integral
- b/c definite value
- $f$ is integrand
- $a$ is lower limit
- $b$ is upper limit
- generally

$$
\int_{b}^{a} f(x) \, dx = - \int_{a}^{b} f(x) \, dx .
$$

## Properties

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"title":"Sum","label":"sum","_index":7}] Proposition 8 (Sum).
> If $f,g$ are integrable over $[a,b]$, 
> 
> $$
> \int_{a}^{b} (f(x) + g(x)) \, dx = \int_{a}^{b} f(x) \, dx + \int_{a}^{b} g(x) \, dx 
> $$

`\begin{proof}` First, note that

$$
\begin{align}
\text{inf}_{f+g}([c,d])&\geq \text{inf}_{f}([c,d]) + \text{inf}_{g}([c,d]) \\
\text{sup}_{f+g}([c,d]) &\leq \text{sup}_{f}([c,d]) + \text{sup}_{g}([c,d]).
\end{align}
$$

Then, for any partition $P$, 

$$
\begin{align}
L(f+g,P) &\geq L(f,P) + L(g,P)  \\
U(f+g, P) &\geq U(f,P) + U(g,P)
\end{align}
$$

Then,

$$
\begin{align}
\underline{I}(f+g) &\geq \underline{I}(f) = \underline{I}(g) \\
\overline{I}(f+g) &\leq \overline{I}(f) + \overline{I}(g).
\end{align}
$$

But since $f$ and $g$ are both integrable, $\underline{I}(f)=\overline{I}(f)$ and $\underline{I}(g)=\overline{I}(g)$, so

$$
\overline{I}(f+g) \leq I(f) + I(g) \leq \underline{I}(f+g)
$$

which means

$$
\underline{I}(f+g) = \overline{I}(f+g) = I(f+g) = I(f) + I(g)
$$
`\end{proof}`

Similarly,

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"title":"Product of Integrable Functions and a Constant","label":"product-of-integrable-functions-and-a-constant","_index":8}] Proposition 9 (Product of Integrable Functions and a Constant).
> If $f$ is integrable over $[a,b]$, so is $\alpha f$ and 
> 
> $$
> \int_{a}^{b} \alpha f(x) \, dx = \alpha \int_{a}^{b} f(x) \, dx .
> $$

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"_index":9}] Proposition 10.
> If $a,b,c\in\mathbb{R}$ with $a<b<c$, $f$ is integrable on $[a,c]$ iff $f$ is integrable on $[a,b]$ and $[b,c]$, and 
> 
> $$
> \int_{a}^{c} f(x) \, dx = \int_{a}^{b} f(x) \, dx + \int_{b}^{c} f(x) \, dx 
> $$

`\begin{proof}` Given partitions $P,P'$ of $[a,b], [b,c]$, $P \cup P'$ is a partition of $[a,c]$. Conversely, if $P''$ is a partition of $[a,c]$ we can refine it by adding $b$ and get a partition of the form $P \cup P'$. Then, using the sum of upper or lower integrals, we can prove that the integrals are equal.
`\end{proof}`

# Techniques

- integration by substitution
- integration by parts

## Integration by Substitution

Let $g$ be a function that is differentiable on an open interval including $[a,b]$ with $g'$ continuous on $[a,b]$. If $f$ is continuous on $[a,b]$, then 

$$
\int_{a}^{b} f(g(x))g'(x) \, dx  = \int_{g(a)}^{g(b)} f(u) \, du .
$$

`\begin{proof}` Let $\phi$ be a primitive of $f$ (this exists because continuous functions on closed intervals are always integrable). By [[Fundamental Theorem of Calculus#^0d77c5|Second Fundamental Theorem of Calculus]], 

$$
\int_{g(a)}^{g(b)} f(u) \, du = \phi(g(b)) - \phi(g(a)) = \phi \circ g(b) - \phi \circ g(a).
$$

Chain rule gives

$$
(\phi \circ g)'(x) = \phi'(g(x))g'(x) = f(g(x))g'(x).
$$

Applying the Second Fundamental Theorem of Calculus again, we get

$$
\int_{a}^{b} f(g(x))g'(x) \, dx = \int_{a}^{b} (\phi \circ g)'(x) \, dx = \phi \circ g(b) - \phi \circ g(a).
$$
`\end{proof}`

## Integration by Parts

Let $f,g$ be differentiable functions on an open interval containing $[a,b]$ s.t. $f',g'$ are continuous on $[a,b]$. Then, 

$$
\int_{a}^{b} f(x)g'(x) \, dx = [f(x)g(x)]_{a}^{b} - \int_{a}^{b} f'(x)g(x) \, dx .
$$

`\begin{proof}` By product rule, 

$$
(fg)'(x) = f(x)g'(x) + f'(x)g(x).
$$

Rearranging,

$$
f(x)g'(x) = (fg)'(x) - f'(x)g(x).
$$

Integrating and using the second fundemental theorem, we get 

$$
\begin{align}
\int_{a}^{b} f(x)g'(x) \, dx  &= \int_{a}^{b} (fg)'(x)\, dx  - \int_{a}^{b} f'(x)g(x) \, dx  \\
&= [f(x)g(x)]_{a}^{b} - \int_{a}^{b} f'(x)g(x) \, dx .
\end{align}
$$
`\end{proof}`

# Polar Coordinates

If $S$ is an angular sector bounded by $\theta=a,\theta=b$, and $r=e$ with $b-a \in [0,2\pi]$, then its area is 

$$
A(s) = \frac{1}{2}(b-a)e^{2}.
$$

We apply the same concept to an area bounded by a radial set bounded by $\theta=a,\theta=b,r=f(\theta)$.

Let $R$ be a radial set bounded by $\theta=a,\theta=b,r=f(\theta)$, where $f^{2}$ is integrable on$[a,b]$ and $b-a \in [0,2\pi]$, Then,

$$
A(R) = \frac{1}{2}\int_{a}^{b} f(\theta)^{2} \, d\theta .
$$

`\begin{proof}` Fix a partition

$$
P:a=t_{0}<t_{1}<\dots<t_{n}=b.
$$

For every integer $j:1\leq j\leq n$, let 

$$
\begin{align}
m_{j}&=\text{inf}_{f}([t_{j-1},t_{j}]) \\
M_{j} &= \text{sup}_{f}([t_{j-1},t_{j}]).
\end{align}
$$

Denote $S_{j},S_{j}'$ as the angular sectors with radii $m_{j}, M_{j}$ between $\theta=t_{j-1}$ and $\theta=t_{j}$. Then,

$$
\frac{1}{2}L(f^{2},P) = \frac{1}{2}\sum_{j=1}^{n}(t_{j}-t_{j-1})m_{j}^{2} = \sum_{j=1}^{n}A(S_{j})
$$

and, similarly,

$$
\frac{1}{2}U(f^{2},P) = \sum_{j=1}^{n}A(S_{j}').
$$

Therefore, 

$$
\frac{1}{2}L(f^{2},P) \leq A(R) \leq \frac{1}{2}U(f^{2},P).
$$

Since $f^{2}$ is integrable, $L$ and $U$ converge to a common [[Limits and Continuity|limit]], which is 

$$
\frac{1}{2}\int_{a}^{b} f^{2}(x) \, dx 
$$

as required.
`\end{proof}`

# Improper Integrals

Let $f$ be a function defined on the interior of an interval $J:[a,b]$ s.t. either $b=\infty$ or $f$ becomes unbounded as $x\to b$. Suppose $a$ is finite and $f(a)$ is defined. Then, $\int _{J}f(x) \, dx$ exists if

1. for every $u \in (a,b)$, $f$ is integrable on $[a,u]$.
2. $\exists$

$$
\lim_{ u \to b , \, u<b} \int_{a}^{u} f(x) \, dx
$$

Then, 

$$
\int_{a}^{b} f(x) \, dx  = \lim_{ u \to b , \, u<b} \int_{a}^{u} f(x) \, dx.
$$

The same applies for $a$:

$$
\int_{a}^{b} f(x) \, dx = \lim_{ u \to a, \, u>a } \int_{u}^{b} f(x) \, dx. 
$$

Both of the above [[Limits and Continuity|limits]] are **improper integrals**.