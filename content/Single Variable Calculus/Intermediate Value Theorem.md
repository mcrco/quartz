Note that because of [[Limits and Continuity|continuity]], 

> [!math|{"type":"lemma","number":"auto","setAsNoteMathLink":false,"_index":0}] Lemma 1.
> If [[Single Variable Calculus/Functions|function]] $f$ is continuous at $c$ and $f(c)\neq 0$, there is an interval $(c-\delta, c+\delta)$ around $c$ where $f$ has the same size as $c$.

^54e2e4

`\begin{proof}` For $\epsilon=\frac{|f(c)|}{2}$, $\exists\delta>0$ s.t. $|x-c|<\delta \implies |f(x)-f(c)| < \frac{|f(c)|}{2}$. $\therefore f(x)$ has the same sign as $f(c)$. 
`\end{proof}`

Due to the above lemma, we have

# Bolzano's Theorem

> [!math|{"type":"theorem","number":"auto","setAsNoteMathLink":false,"title":"Bolzano's Theorem","label":"bolzano-theorem","_index":1}] Theorem 2 (Bolzano's Theorem).
> Suppose $f$ is continuous on $[a,b]$ and $f(a)$ and $f(b)$ have opposite signs. Then, $\exists c\in(a,b):f(c)=0$.

^1959fb

`\begin{proof}` Suppose WLOG that $f(a)<0, f(b)>0$. Let $B$ be the set $\{ x \in[a,b] \mid f(x)\leq 0 \}$. This is bounded and nonempty so $c=\text{sup}B$ exists. We claim $f(c)=0$. 

If $f(c)>0$, then by [[#^54e2e4]] , it is positive in some neighborhood of $c$, so there is $c'<c$ which is an upper bound for $B$, contradicting the definition of $c$.

If $f(c)<0$, then again by [[#^54e2e4]], there is $c''>c$ s.t. $f(c'')<0$, again a contradiction
`\end{proof}`

Generalizing Bolzano's, we get

# Intermediate Value Theorem

> [!math|{"type":"theorem","number":"auto","setAsNoteMathLink":false,"title":"Intermediate Value Theorem","label":"intermediate-value-theorem","_index":2}] Theorem 3 (Intermediate Value Theorem).
> Let $f\in C([a,b])$. If $x_{1}$ and $x_{2}$ are 2 points in $[a,b]$ with $x_{1}<x_{2}$ and $f(x_{1})\neq f(x_{2})$, then $f$ takes every value between $f(x_{1})$ and $f(x_{2})$ in the interval $(x_{1},x_{2})$.

`\begin{proof}` Suppose WLOG that $f(x_{1})<f(x_{2})$. For $t \in (f(x_{1}),f(x_{2}))$, consider $g(x)=f(x)-t$. Then, $g(x_{1})<0$, $g(x_{2})>0$, and $g$ is continuous, so we can apply [[#^1959fb]] to find $c\mid g(c)=0$. Then, $f(c)-t=0$, or $f(c)=t$.
`\end{proof}`