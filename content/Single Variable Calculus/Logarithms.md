> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Natural Logarithm","label":"natural-logarithm","_index":0}] Definition 1 (Natural Logarithm).
> For any $x>0$, we define its natural logarithm by
>
> $$
> \log x = \ln x = \int_{1}^{x} \frac{dt}{t}
> $$

# Properties

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"_index":1}] Proposition 2.
> $\log 1=0$

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"_index":2}] Proposition 3.
> $\log x$ is differentiable on $(0,\infty)$ with derivative $\frac{1}{x}$

`\begin{proof}`For any $x$, the function $\frac{1}{t}$ is continuous on $[1,x]$, so by the [[Fundamental Theorem of Calculus#The First Fundamental Theorem of Calculus|first fundamental theorem of calculus]], $\log x$ is differentiable with derivative $\frac{1}{x}$.`\end{proof}`

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"_index":3}] Proposition 4.
> For all $x,y>0$, $\log xy = \log x + \log y$.

`\begin{proof}` Fix $y>0$ and consider the function given by

$$
l(x)=\log (xy)
$$

for $x>0$.

Since $l(x)$ is the composition of the differentiable functions $x \mapsto xy$ and $u \mapsto \log u$, it is also differentiable. By chain rule,

$$
l'(x)=y\left( \frac{1}{yx} \right)=\frac{1}{x}.
$$

Thus, $l$ and $\log x$ have the same derivative, so

$$
l(x)=\log x+c.
$$

Taking $x=1$, we get

$$
\log y=l(1)=0+c \implies \log y=c,
$$

so that

$$
\log xy=l(x)=\log x+c=\log x+\log y.
$$
`\end{proof}`

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"_index":4}] Proposition 5.
> $\log x$ is strictly increasing on $(0,\infty)$.

`\begin{proof}` Since $\frac{d}{dx}\log x=\frac{1}{x}>0$ for all $x>0$, the function is strictly increasing. 
`\end{proof}`

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"_index":5}] Proposition 6.
> $\log x \to \infty$ as $x \to \infty$ and $\log x \to -\infty$ as $x \to 0$.

`\begin{proof}` $\log x$ is strictly increasing and $\log 1=0$, so $\log 2>0$. Then,

$$
\log(2^{n})=n\log 2 \to \infty
$$

as $n \to \infty$.

In the other direction, notice that $\log \frac{1}{2} < 0$, so 

$$
\log\left( \frac{1}{2^{n}} \right) = n\log \frac{1}{2} \to -\infty
$$

as $n \to \infty$.
`\end{proof}`


> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"_index":6}] Proposition 7.
>  $\log x$ is integrable on any finite subinterval of $(0,\infty)$ and 
>  $$
> \int \log x \, dx = x\log x - x + C   
> $$

`\begin{proof}` Since $\log x$ is continuous, it is integrable on any finite subinterval of $0,\infty$. By integration by parts, 

$$
\begin{align}
\int \log x \, dx &=x\log x-\int x \frac{d}{dx}(\log x) \, dx \\
&= x\log x - \int 1 \, dx  \\
&= x\log x - x + c  
\end{align}
$$

`\end{proof}`

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"_index":7}] Proposition 8.
> $$
> \lim_{ x \to 0 } x\log x=0 \quad \text{and} \quad \lim_{ x \to 0 } \frac{\log x}{x} = 0
> $$

`\begin{proof}` Let $L=\lim_{ x \to 0 }x\log x$. If $u=\frac{1}{x}$, $f(u)=-\log(\frac{1}{u})$ and $g(u)=u$, then

$$
L = \lim_{ u \to \infty } \frac{1}{u}\log\left( \frac{1}{u} \right) = -\lim_{ u \to \infty } \frac{f(u)}{g(u)}
$$

Using [[L'Hopital's Rule]],

$$
\begin{align}
-\lim_{ u \to \infty } \frac{f(u)}{g(u)} &= -\lim_{ u \to \infty } \frac{f'(u)}{g'(u)} \\
&= -\lim_{ u \to \infty } \frac{1}{u} \\
&= 0
\end{align}
$$

We can similarly prove 

$$
\lim_{ x \to 0 } \frac{\log x}{x}.
$$
`\end{proof}`

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"_index":8}] Proposition 9.
> [[Integration#Improper Integrals|Improper integral]] of $\log x$ over $(0,b]$ exists for any $b>0$ and 
> 
> $$
> \int_{0}^{b} \log x \, dx =b\log b - b.
> $$

`\begin{proof}` 
$$
\begin{align}
L&=\lim_{ a \to 0 } \int_{a}^{b} \log t \, dt \\
&= \lim_{ a \to 0 } [t\log t-t]_{a}^{b} \\
&= \lim_{ a \to 0 } b\log b-b-(a\log a-a) \\
&= b\log b-b-\lim_{ a \to 0 } (a\log a-a) \\
&= b\log b-b.
\end{align}
$$
`\end{proof}`