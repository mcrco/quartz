> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"","label":"","_index":0}] Definition 1.
> A sequence of real numbers is a set
> $$
> a_{1},a_{2},a_{3}\dots
> $$
> of real numbers indexed by the natural numbers. Usually, we write $(a_{n})_{n=1}^{\infty}$ or $a_{n}$.

## Examples

$a_{n}=\frac{1}{n}$: we can see that $a_{n} \to 0$ as $n\to \infty$, We can say that $a_{n}$ is converging to the limit $0$.

$a_{n}=(-1)^{n} \implies (a_{n})_{n=1}^{\infty}=(-1, 1, -1, 1, \dots)$. This just oscillates and doesn't converge.

Now, if $a_{n}=\frac{(-1)^{n}}{n}=(-1, \frac{1}{2}, -\frac{1}{3}, \frac{1}{4},\dots$, this also converges to the limit $0$.

## Convergence

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Convergence","label":"convergence","_index":1}] Definition 2 (Convergence).
> A sequence $(a_{n})^{\infty}_{n=1}$ converges to the limit $A$ iff for every $\forall \epsilon>0, \exists N=N(\epsilon) \in \mathbb{N}: |a_{n}-A|<\epsilon , n\geq N$. We write $\lim_{ n \to \infty }a_{n}=A$.

## Examples

Show that $a_{n}=\frac{1}{n} \to 0$. 

`\begin{proof}`
Fix $\epsilon>0$ and choose $N>\dots$.

Then, $\forall n\geq N$, we have

$$
| \frac{1}{n} - 0 | = \frac{1}{n} \leq \frac{1}{N} < \epsilon
$$

`\end{proof}`

## 

> [!math|{"type":"lemma","number":"auto","setAsNoteMathLink":false,"_index":2}] Lemma 3.
> If $(a_{n})$ and $(b_{n})$ are sequences with $\lim_{ n \to \infty }a_{n}=A$ and $\lim_{ n \to \infty }b_{n}=B$, then 
> a. $\lim_{ n \to \infty }(a_{n}+b_{n})=A+B$
> `\begin{proof}`\Since $\lim_{ n \to \infty }a_{n}=A$, $\exists N\mid |a_{n_{1A|<}}-\frac{\epsilon}{2} \forall n_{1}\geq N_{1}$. If Since $\lim_{ n \to \infty }b_{n}=B$, $\exists N_{2} \mid |b_{n}-B|< \frac{\epsilon}{2}, \forall n_{2}\geq N_{2}$. 
> If we let $N=max(N_{1},N_{2})$, then $\forall n\geq N$, $|a_{n}+b_{n}-(A+B)| = |(a_{n}-A) + (b_{n}-B)$ $\leq |a_{n}-A| + |b_{n} - B| < \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon$.
> `\end{proof}`
> b. $\lim_{ n \to \infty }ca_{n}=cA$ for $c \in \mathbb{R}$
> c. $\lim_{ n \to \infty } \frac{a_{n}}{b_{n}}$
> d. $\lim_{ n \to \infty }a_{n}b_{n}=AB$. 
## Monotone Sequence

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Monotonically Increasing Sequence","label":"monotonically-increasing-sequence","_index":3}] Definition 4 (Monotonically Increasing Sequence).
> A sequence $(a_{n})_{n=1}^{\infty}$ is monotone increasing, written $a_{n} \uparrow$, if $a_{n} \leq a_{n+1}, \, \forall n\geq 1$ and is monotone decreasing, written $a_{n} \downarrow$ if $a_{n+1} \leq a_{n}, \, \forall n\geq 1$. In either case, $a_{n}$ is monotone

> [!math|{"type":"theorem","number":"auto","setAsNoteMathLink":false,"title":"Monotone Sequence Convergence","label":"monotone-sequence-convergence","_index":4}] Theorem 5 (Monotone Sequence Convergence).
> Every bounded monotone sequence is convergent.
> `\begin{proof}`
> By the [[#^e56e85]] , $\{ a_{n} \}$ has a supremum $A$. Then, for any $\epsilon>0$, $A-\epsilon$ is not an uppre bound, so $\exists N\mid a_{n}>A-\epsilon$. But $(a_{n})$ is monotone increasing, so $a_{n} \geq a_{N} \geq A-\epsilon, \, \forall n\geq N$. 
> `\end{proof}`

# The Squeeze Principle

If $(a_{n})$, $(b_{n})$, and $(c_{n})$ are sequences such that

- $b_{n} \leq a_{n} \leq c_{n}, \, \forall n\geq i$
- $\lim_{ n \to \infty }b_{n}=\lim_{ n \to \infty }c_{n}=L$

then $\lim_{ n \to \infty }a_{n}=L$.

`\begin{proof}`
Choose $N_{1}$
`\end{proof}`
