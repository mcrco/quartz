> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"exp","label":"exp","_index":0}] Definition 1 (exp).
> The inverse function of $\log$ from $\mathbb{R} \to \mathbb{R}^{+}$ is $\exp(x)$.

# Properties

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"_index":1}] Proposition 2.
> $\exp(0)=1$

`\begin{proof}`$\exp(\log(y))=y, \log(1)=0$. `\end{proof}`

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"_index":2}] Proposition 3.
> $\frac{d}{dx}\exp=\exp$

`\begin{proof}`Since $\frac{d}{dx}\log x=\frac{1}{x}\neq 0$, using [[Differentiation#Derivatives of Inverses|the formula for the derivative of an inverse]], 

$$
\frac{d}{dx}\exp(x)=\frac{1}{\frac{d}{dx}\log(\exp(x))}=\frac{1}{\frac{1}{\exp(x)}}=\exp(x)
$$
`\end{proof}`

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"_index":3}] Proposition 4.
> For $x,y \in \mathbb{R}$, $\exp(x+y)=\exp(x)\exp(y)$

`\begin{proof}` For $x,y \in \mathbb{R}$, exists unique $u,v \in \mathbb{R}^{+}$ s.t. $x=\log u,y=\log v$.

$$
\begin{align}
\exp(x+y)&= \exp(\log u+\log v) \\
&= \exp(\log uv) \\
&= uv \\
&= \exp(x)\exp(y).
\end{align}
$$
`\end{proof}`

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"_index":4}] Proposition 5.
> $\exp$ is strictly increasing.

`\begin{proof}`If $x>y$, let $x=\log(u),y=\log v$. $\log$ is strictly increasing, so $u>v$, and thus $u=\exp(x)>\exp(y)=v$.
`\end{proof}`

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"_index":5}] Proposition 6.
> $\lim_{ x \to \infty }\exp(x)=\infty$, $\lim_{ x \to -\infty }(x)=0$

`\begin{proof}` For the first limit, we must show $\exp(x)>M$ when $x>L$, or equivalently $\log x>\log L\implies x>\log M$, which is possible since we choose $L$. Similarly, for the second limit, we must show $x<L\implies \exp(x)<\epsilon$ or $\log x<\log L\implies x<\log\epsilon$.`\end{proof}`

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"_index":6}] Proposition 7.
> $\int \exp(x) \, dx=\exp(x)+C$

`\begin{proof}`Since $\exp$ is differentiable, it is continuous. Thus, it is integrable on finite subintervals. We also know $\frac{d}{dx}\exp=\exp$.`\end{proof}`

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"_index":7}] Proposition 8.
> $\lim_{ x \to \infty } \frac{p(x)}{\exp(x)}=0$ and $\lim_{ x \to -\infty }p(x)\exp(x) = 0$ for polynomials $p$.

`\begin{proof}`Start with $\lim_{ x \to \infty } \frac{x^{j}}{\exp x}$. We know that $\frac{\exp x}{x^{j}} \to \infty$ since the $\log$ of the previous term is $x - j\log x = x(1-\frac{j\log x}{x}) \to \infty$. 

For $\lim_{ x \to -\infty }x^{j}\exp x$, check $\frac{1}{x\exp x}\to-\infty$, which is true since $\log\left( -\frac{1}{x\exp x} \right) = \log\left( -\frac{1}{x} \right)-x=x(\frac{\log x}{-x}-1)$.
`\end{proof}`

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"_index":8}] Proposition 9.
> $\int_{-\infty}^{b} \exp(x) \, dx=\exp(b)$

`\begin{proof}`We need to show

$$
L = \lim_{ x \to -\infty } \int_{x}^{b} \exp(t) \, dt=\lim_{ x \to -\infty } \exp b-\exp x .
$$

> [!math|{"type":"lemma","number":"auto","setAsNoteMathLink":false,"_index":9}] Lemma 10.
> If $f$ is differentiable on $(a,b)$ and $f'(x)=f(x) \forall x \in (a,b)$, then $\exists c$ s.t. $f(x)=c \exp x$ and if $f(0)=1$, $c=1$.

We can prove this lemma is true by differentiating $h(x)=\frac{f(x)}{\exp(x)}$ using [[Differentiation#Properties|quotient rule]] to find that $h$ is constant, say $c$. 
`\end{proof}`

# e

The number $e$ is defined as $e=\exp(1)$. 

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"_index":10}] Proposition 11.
> $\exp(x)=e^{x}$.

`\begin{proof}`Apply $\log$ to get $x=\log(e^{x})$.

Now, we will prove this is true for $\mathbb{Z}, \mathbb{Q},\mathbb{R}$ in that order.

We know

$$
1=\log e=\log((e^{1/n})n)=n\log(e^{1/n}) \implies \log(e^{1/n})=\frac{1}{n}
$$
and 

$$
\log(e^{n})=n\log(e)=n.
$$

Then,

$$
\log(e^{m/n})=m\log(e^{1/n})=\frac{m}{n}.
$$

Then, for $x \in \mathbb{R}$, take $\alpha_{n} \in \mathbb{Q} \to x$, so

$$
\log(e^{x})=\log(e^{\lim \alpha^{_{n}}}) = \log(\lim e^{\alpha n}) = \lim \log(e^{\alpha n}) = \lim \alpha_{n} = x.
$$
`\end{proof}`

Now, for every $a > 0, a^{x} = e^{x\log n}$, this is monotone so it has an inverse, all it $\log_a$. It is easy to see that

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"_index":11}] Proposition 12.
> $\frac{d}{dx}a^{x}=a^{x}\log a$.

## Hyperbolic Functions

$e$ is key to the hyperbolic trig functions:

$$
\sinh(x) = \frac{e^{x}-e^{-x}}{2}, \, \cosh (x) = \frac{e^{x} + e^{-x}}{2}, \, \tanh(x) = \frac{\sinh}{\cosh}.
$$

### Cool Properties

1. $\frac{d}{dx}\sinh=\cosh$
2. $\frac{d}{dx}\cosh=\sinh$
3. like Pythagorean theorem but with diff sign
4. model [[Conic Sections#Hyperbola|hyperbolas]]
