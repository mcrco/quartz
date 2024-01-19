Series are the sum of [[Sequences]], where we take a sequence $(a_{n})_{n=1}^{\infty}$ and add up all of its terms.

# Convergence

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Series","label":"series","_index":0}] Definition 1 (Series).
> A series $(a_{n})_{n=1}^{\infty}$ converges if the sequence of partial sums $S_{1}=a_{1}, S_{2}=a_{1}+a_{2}, S_{3}=a_{1}+a_{2}+a_{3}\dots$ converges. We then set $\sum_{k=1}^{\infty}a_{k}=\lim_{ n \to \infty }S_{n}$.

## Examples

Show that 

$$
\sum_{k=0}^{\infty}x^{k}=\frac{1}{1-x}, \, |x|<1
$$

`\begin{proof}`

Let 

$$
S_{n} = \sum_{k=0}^{n}x^{k} = x^{0} + x^{1} + \dots + x^{n}
$$

Then,

$$
xS_{n} = x\sum_{k=0}^{n}x^{k} = x^{1} + x^{2} + \dots + x^{n+1}.
$$

Subtracting the second equation from the first, we get

$$
\begin{gather}
S_{n}-S_{n}x = 1 - x^{n+1} \\
S_{n}(1-x) = 1-x^{n+1} \\
S_{n} = \frac{1-x^{n+1}}{1-x}.
\end{gather}
$$

Now, by the definition of convergence, we just need to make sure that $\lim_{ n \to \infty }S_{n}$ converges. Plugging in, we get

$$
\lim_{ n \to \infty } \frac{1-x^{n+1}}{1-x} = \frac{1}{1-x}.
$$

Therefore, 

$$
xS_{n} = x\sum_{k=0}^{n}x^{k} = x^{1} + x^{2} + \dots + x^{n+1}
$$

converges.
`\end{proof}`
## Sum of Two Converging Series

> [!math|{"type":"lemma","number":"auto","setAsNoteMathLink":false,"title":"Sum of 2 Converging Series","label":"sum-of--converging-series","_index":1}] Lemma 2 (Sum of 2 Converging Series).
> If $\sum a_{k}$ and $\sum b_{k}$ converge, then $\sum(\alpha a_{k}+\beta b_{k})$ converges for $\alpha,\beta \in \mathbb{R}$.

## Divergence of Harmonic Series

> [!math|{"type":"lemma","number":"auto","setAsNoteMathLink":false,"title":"Harmonic Series","label":"harmonic-series","_index":2}] Lemma 3 (Harmonic Series).
> $\sum_{k=1}^{\infty} \frac{1}{k}$ diverges. 

`\begin{proof}`

Observe that 

$$
\begin{align}
\sum_{k=n+1}^{2n} \frac{1}{k} &= \frac{1}{n+1} + \frac{1}{n+2} + \dots + \frac{1}{2n} \\
&> \frac{1}{2n} + \frac{1}{2n} + \dots + \frac{1}{2n} \\
&= \frac{n}{2n} = \frac{1}{2}
.\end{align}
$$

Therefore, 

$$
\begin{align}
\sum_{k=1}^{2^{S}} \frac{1}{k} &= \sum_{k=1}^{2} \frac{1}{k} + \sum_{k=3}^{4} \frac{1}{k} + \sum_{k=5}^{8} \frac{1}{k} + \dots + \sum_{k=2^{S-1}+1}^{2^{S}} \frac{1}{k} \\
&> \frac{S}{2}
\end{align}
$$

Thus, the set of partial sums diverges.
`\end{proof}`

## Telescoping Series

Similarly, $\sum_{k=1}^{\infty} \frac{1}{k+1}$ diverges. However, their difference $\sum_{k=1}^{\infty} \frac{1}{k} - \frac{1}{k+1}$ converges. This is because of telescoping series.

$$
\begin{align}
\sum_{k=1}^{\infty} \frac{1}{k} -\frac{1}{k+1} &= \frac{1}{1} - \frac{1}{2} + \frac{1}{2} - \frac{1}{3} + \frac{1}{3} - \frac{1}{4} \dots - \frac{1}{\infty} \\
&= 1
\end{align}
$$

## Necessary Limit Condition

> [!math|{"type":"lemma","number":"auto","setAsNoteMathLink":false,"title":"Limit of Converging Series Term","label":"limit-of-converging-series-term","_index":3}] Lemma 4 (Limit of Converging Series Term).
> If $\sum_{k=1}^{\infty} a_{n}$ converges, then $\lim_{ n \to \infty }a_{n}=0$.

`\begin{proof}`

$$
S_{n} = \lim_{ n \to \infty } \sum_{k=1}^{n}a_{k} = L \implies S_{n-1} = L \implies S_{n}- S_{n-1} = L - L = 0 = a_{n}
$$
`\end{proof}`

## Comparison Test

If $\sum_{}^{}b_{n}$ converges and $a_{n} \leq c b_{n}$ for $n\geq 1, c > 0$, then $\sum_{}^{}a_{n}$ converges.

`\begin{proof}`This is obvious when comparing partial sums (both are bounded). `\end{proof}`

## Limit Comparison Test

If $a_{n}, b_{n} > 0$ and $\lim_{ n \to \infty } \frac{a_{n}}{b_{n}} = 1$, then $\sum_{}^{}a_{n}$ converges iff $\sum_{}^{}b_{n}$ converges.

`\begin{proof}`$\lim_{ n \to \infty } \frac{a_{n}}{b_{n}} = 1 \implies \exists N \in \mathbb{N}$ such that $\frac{1}{2} < \frac{a_{n}}{b_{n}} < \frac{3}{2}$ for $n \geq N \implies b_{n} < 2a_{n}, a_{n} < \frac{3}{2} b_{n}$ for $n \geq N$. Then, we can apply Comparison Test.
`\end{proof}`

## Root Test

If $a_{k}\geq 0$ for $k\geq 1$ in $\sum_{k=1}^{\infty}a_{k}$ and $\lim_{ n \to \infty }a_{k}^{\frac{1}{k}} = R$, then 

1. If $R < 1$, the series converges ($a_{n}=\frac{n}{3^{n}}$)
2. If $R>1$, the series diverges ($a_{n}=n^{2}2^{n}$)
3. If $R=1$, inconclusive ($a_{n}=\frac{1}{n\log n}$)

`\begin{proof}` If $R<1$, choose $x$ such that $R<x<1$. Then, $\exists N \mid a_{n}^{\frac{1}{n}} < x$ for $n\geq N$. Then, $a_{n} < x^{n}$ for $n\geq N$ and $x < 1 \implies x^{n} \to 0$. 

If $R > 1$, then $\lim_{ n \to \infty }a_{n} \neq 0$.
`\end{proof}`

## Ratio Test

Suppose

$$
\sum_{k=1}^{\infty}a_{k}:\forall k\geq 1, a_k>0, \lim_{ n \to \infty } \frac{a_{n+1}}{a_{n}} = L.
$$

1. If the [[Limits and Continuity|limit]] $L<1$, the series converges
2. If $L>1$, the series diverges
3. If $L=1$, inconclusive

`\begin{proof}` If $L<1$, let $x:L<x<1$. Then, there exists $N$ such that $\frac{a_{n+1}}{a_{n}}<x$ for all $n\leq N$. This implies $\frac{a_{n+1}}{x^{n+1}}< \frac{a_{n}}{x_{n}}$ for all $n\geq N$. Thus, $\frac{a_{n}}{x^{n}}<c$ for some $c>0$, and $\sum_{}^{}a_{n}$ converges by the Comparison Test.

If $L>1$, then $a_{n+1}>a_{n}$ for all $n\geq N$, which clearly doesn't converge.
`\end{proof}`

# Absolute Convergence

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Absolute Convergence","label":"absolute-convergence","_index":4}] Definition 5 (Absolute Convergence).
> $\sum_{}^{}a_{n}$ is absolutely convergent if $\sum_{}^{}|a_{n}|$ converges. If $\sum_{}^{}a_{n}$ converges and $\sum_{}^{}|a_{n}|$ diverges, then $\sum_{}^{}a_{n}$ is conditionally convergent.

Absolute convergence is useful because

## Absolute Convergence Test

> [!math|{"type":"lemma","number":"auto","setAsNoteMathLink":false,"_index":5}] Lemma 6.
> If $\sum_{}^{}a_{n}$ is absolutely convergent, it is convergent.

`\begin{proof}` Let $b_{n}=a_{n}+|a_{n}|$. Then $bn=0$ or $bn=2|a_{n}|$, so $0\leq b_{n}\leq 2|a_{n}|$. By Comparison Test, $\sum_{}^{}b_{n}$ converges, so $\sum_{}^{}a_{n}=\sum_{}^{}b_{n}-\sum_{}^{}|a_{n}|$ also converges.
`\end{proof}`

To find conditional convergence, we use

## Alternating Series Test

If $a_{n}$ is monotonically decreasing and $a_{n}\to{0}$, then $\sum_{}^{}(-1)^{n-1}a_{n}$ converges.

`\begin{proof}` The partial sums $S_{2n}$ are monotonic increasing since

$$
S_{2n+2} - S_{2n} = a_{2n+1} - a_{2n+2} > 0
.$$

Similarly, $S_{2n+1}$ is decreasing.

Both sequences are bounded below by $S_{2}$ and above by $S_{1}$. Then,

$$
\begin{align}
\lim_{ n \to \infty } S_{2n} - \lim_{ n \to \infty } S_{2n-1} &= \lim_{ n \to \infty } S_{2n}-S_{2n-1} \\
&= \lim_{ n \to \infty } -a_{2n} \\
&= 0
\end{align}
$$

Thus, $\sum_{}^{}a_{n}$ converges.
`\end{proof}`

## Integral Test

For $S=\sum_{n=1}^{\infty}a_{n}$ w/ $a_{n}=f(n)$ for $f>0$, monotone and decreasing on $[1,\infty]$, then $S$ converges iff $I=\int_{1}^{\infty} f(x) \, dx$ converges.

`\begin{proof}`Partition $[1,N]$ into $1<2<3<\dots<N$ so

$$
\begin{align}
U(f,P_{N})&=a_{1}+a_{2}+\dots+a_{N-1}\\
L(f,P_{N})&=a_{2} + \dots + a_{N}
.\end{align}
$$

We know

$$
L(f,P_{N})<\int_{1}^{N} f \, dx < \int_{1}^{\infty} f(x) \, d\mathbf{x}.
$$

Let $N\to \infty$, so $S-a_{1}<\int_{1}^{\infty} f(x) \, dx$.

For the converse, notice

$$
\int_{1}^{N} f(x) \, dx =\sum_{j=1}^{j=N-1}\int_{j}^{j+1} f(x) \, dx.
$$

Let the $b_{j}=\int_{j}^{j+1} f(x) \, dx$. Clearly, $a_{n+1}<b_{n}\leq a_{n}$, so by [[#Comparison Test]], $S-a_{1}\leq\int_{1}^{\infty} f(x) \, dx\leq S$. 
`\end{proof}`

# Power Series

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Power Series","label":"power-series","_index":6}] Definition 7 (Power Series).
> A power series is an infinite series of the form
> $$
> \sum_{n=0}^{\infty}a_{n}(z-a)^{n}=a_{0}+a_{1}(z-a)+a_{2}(z-a)^{2}+\dots
> $$

## Convergence

> [!math|{"type":"lemma","number":"auto","setAsNoteMathLink":false,"_index":7}] Lemma 8.
> If the power series $\sum_{}^{}a_{n}z^{n}$ converges for a particular $z=z_{1}\neq 0$, then it converges absolutely for all $z:|z|<|z_{1}|$.

^d5c99e

`\begin{proof}` Since $\sum_{}^{}a_{n}z_{1}^{n}$ converges, $a_{n}z_{1}^{n}\to0$ as $n\to \infty$. Therefore, there is $N \in \mathbb{N}$ s.t. $|a_{n}z_{1}^{n}|<1$ for all $n\geq N$. If $|z|<|z_{1}|$, then 

$$
|a_{n}z^{n}|=|a_{n}z_{1}^{n}| |\frac{z}{z_{1}}|^{n}< |\frac{z}{z_{1}}|^{n}
$$

for all $n\geq N$. Since $\sum_{}^{}|\frac{z}{z_{1}}|^{n}<\infty$, $\sum_{}^{}a_{n}z^{n}$ converges by comparison.
`\end{proof}`

## Radius of Convergence

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"title":"Radius of Convergence","label":"radius-of-convergence","_index":8}] Axiom 9 (Radius of Convergence).
> If the $\sum_{}^{}a_{n}z^{n}$ converges for at least one $z=z_{1}\neq 0$ and diverges for $z=z_{2}\neq 0$, there exists a positive real number $R$ called the radius of convergence s.t. the series converges absolutely if $|z|<R$ and diverges if $|z|>R$.

`\begin{proof}` Let $A$ be the set of $|z|$ for which $\sum_{}^{}a_{n}z^{n}$ converges. Then $A\neq \emptyset$ and the set is bounded by $|z_{2}|$. Therefore, $R=\text{sup} A$ exists. Then, $\sum_{}^{}a_{n}z^{n}$ diverges for all $|z|>R$. If $|z|<R$, then $\exists x$ with $|z|<x<R$ s.t. the series converges. So by [[#^d5c99e]], $a_{n}z^{n}$ also converges.
`\end{proof}`
We find the radius of convergence by using the [[Series#Ratio Test]].

