Suppose $f$ is $n$ times differentiable on $I$. Then, the nth Taylor polynomial of $f$ at $x=a \in I$ is

$$
T_{n}(f(x);a) = \sum_{j=0}^{n} \frac{f^{(j)}(a)}{j!}(x-a)^{j}.
$$

Taylor polynomials are good approximations for functions.

# Useful Taylor Polynomials

> [!math|{"type":"lemma","number":"auto","setAsNoteMathLink":false,"_index":0}] Lemma 1.
> If $f(x)=a_{0}+a_{1}x+a_{2}x^{2}+\dots+a_{m}x^{m}$, then $f$ is infinitely differentiable and 
> 
> $$
> T_{n}(f(x);0)=\begin{cases}
> a_{0}+a_{1}x+\dots+a_{n}x^{n} \quad \text{if } n<m \\
> a_{0}+a_{1}x+\dots+a_{m}x^{m} \quad \text{if } n\geq m
\end{cases}
$$

We can prove the above using induction.

## Sin and Cos

$$
T_{n}(\sin x;0)=\sum_{j=1}^{n} (-1)^{j+1}\frac{x^{2j+1}}{(2j+1)!}
$$

We can once again prove the above using induction on the derivative of $\sin$.

