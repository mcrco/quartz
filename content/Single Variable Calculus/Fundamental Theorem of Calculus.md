[[Differentiation]] and [[Integration]] are actually inverse operations!

First, we prove that integration yields [[Limits and Continuity|continuous]] functions. 

`\begin{proof}` Let

$$
A(x) = \int_{a}^{x} f(t) \, dt .
$$

Then, $A$ is continuous iff $\lim_{ h \to 0 }A(c+h)=A(c)$. By definition,

$$
A(c+h)-A(c)=\begin{cases}
\int_{c}^{c+h} f(t) \, dt &\text{if } h\geq 0 \\
\int_{c+h}^{c} f(t) \, dt &\text{if } h<0.
\end{cases}
$$

Since $f$ is bounded and $h \to 0$, both tend to $0$.
`\end{proof}`

Now, we have

## The First Fundamental Theorem of Calculus

> [!math|{"type":"theorem","number":"auto","setAsNoteMathLink":false,"title":"First Fundamental Theorem of Calculus","label":"first-fundamental-theorem-of-calculus","_index":0}] Theorem 1 (First Fundamental Theorem of Calculus).
> Let $f$ be integrable on $[a,b]$ and $A$ its integral. If $c \in (a,b)$ and $f$ is continuous at $c$, then $A$ is differentiable at $c$ and $A'(c)=f(c)$.

`\begin{proof}` To show that $A(x)$ is differentiable at $c$, we need to evaluate

$$
L = \lim_{ h \to 0 } \frac{A(c+h)-A(c)}{h}.
$$

Letting 

$$
S = \begin{cases}
[c,c+h], &\text{if } h\geq 0 \\
[c+h,c], &\text{if } h < 0,
\end{cases}
$$

we get

$$
A(c+h)-A(c) = \int _{S}f(t) \, dt .
$$

Letting $s = \text{sup}_{f}(S)$ and $i=\text{inf}_{f}(S)$, 

$$
hi \leq \int _{S}f(t) \, dt \leq hs. 
$$

Therefore, 

$$
i \leq \frac{\int _{S}f(t) \, dt}{h} \leq s, 
$$

so, taking the limit, we get

$$
\lim_{ h \to 0 } i \leq L \leq \lim_{ h \to 0 } s.
$$

Since $f$ is continuous at $c$, $f(c)=\lim_{ h \to 0 }i = \lim_{ h \to 0 }s$. Hence, $L=f(c)$.
`\end{proof}`

## Second Fundamental Theorem of Calculus

First, we define

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Primitive","label":"primitive","_index":1}] Definition 2 (Primitive).
> Let $f$ be a function on an open interval $I$. A primitive $\phi$ of $f$ on $I$ is a differentiable function on $I$ with $\phi'(x)=f(x)$ for all $x \in I$. Not unique: $\phi \to \phi + c$.

Now,

> [!math|{"type":"theorem","number":"auto","setAsNoteMathLink":false,"title":"Second Fundamental Theorem of Calculus","label":"second-fundamental-theorem-of-calculus","_index":2}] Theorem 3 (Second Fundamental Theorem of Calculus).
> Suppose $f,\phi$ are functions on $[a,b]$ with $f$ integrable and $\phi$ is a primitive, defined and continuous. Then,
> 
> $$
> \phi(b)-\phi(a) = \int_{a}^{b} f(x) \, dx 
> $$

^0d77c5

`\begin{proof}` Let $P$ be a partition of $[a,b]$ with 

$$
P: a=t_{0}<t_{1}<\dots<t_{n}=b
$$

and set $M_{j}=\text{sup}_{f}([t_{j-1},t])$ and $m_{j}=\text{inf}([t_{j-1},t_{j}])$. By definition,

$$
L(f, P) = \sum_{j=1}^{n}m_{j}(t_{j}-t_{j-1}) \leq \int_{a}^{b} f(x) \, dx \leq \sum_{j=1}^{m}M_{j}(t_{j}-t_{j-1}) = U(f, P).
$$

On the other hand, by [[Differentiation#Mean Value Theorem|MVT]], there is $c_{j}\in [t_{j-1},t_{j}]$ s.t.

$$
\phi'(c_{j}) = \frac{\phi(t_{j})-\phi(t_{j-1})}{t_{j}-t_{j-1}}.
$$

But $f(c_{j})=\phi'(c_{j})$ and $m_{j}\leq f(c_{j}) \leq M_{j}$, so 

$$
m_{j}(t_{j}-t_{j-1}) \leq \phi(t_{j})-\phi(t_{j-1}) \leq M_{j}(t_{j}-t_{j-1}).
$$

Adding over all $j$, we get

$$
L(f, P) \leq \sum_{j=1}^{n}(\phi(t_{j})-\phi(t_{j-1})) = \phi(b) - \phi(a) \leq U(f, P).
$$

Since $f$ is integrable, we get that 

$$
L(f,P) = U(f,P) = \phi(b)-\phi(a) = \int_{a}^{b} f(x) \, dx. 
$$
`\end{proof}`