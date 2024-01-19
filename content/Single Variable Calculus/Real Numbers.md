- [[Sets|set]] of infinite decimal expansions
- $a_{0}.a_{1}a_{2}a_{3}\dots$, where $a_{0}\in\mathbb{Z}$ and $0\leq a_{i}\leq 9$ for $i\geq 1$.
- 'fills in number line'
- $0.\bar{9} = 1$

# Field Axioms

On $\mathbb{R}$, there are 2 binary operations $+$ and $\cdot$ such that 

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"title":"Commutativity","label":"commutativity","_index":0}] Axiom 1 (Commutativity).
> $x=y=y+x$, $xy = yx$.

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"title":"Associativity","label":"associativity","_index":1}] Axiom 2 (Associativity).
> $$
> \begin{gather*}
> x+(y+z)\geq(x+y)+z, \\
> x(yz) = (xy)z \\
> \end{gather*}
> $$ 

^a925ed

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"title":"Distributivity","label":"distributivity","_index":2}] Axiom 3 (Distributivity).
> $$
>x(y+z)=xy+xz
>$$

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"title":"Existence of $0,1$","label":"existence-of-01","_index":3}] Axiom 4 (Existence of $0,1$).
> $$
> \begin{gather}
> 0+x=0,  \\
> 1\cdot x=x \\
> \end{gather} 
> $$

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"title":"Existence of Negatives","label":"existence-of-negatives","_index":4}] Axiom 5 (Existence of Negatives).
> $$
> \forall x \in \mathbb{R}, \exists y \mid y + x = 0
> $$
> This is the definition of $-x$.

We may now define

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Comparator","label":"comparator","_index":5}] Definition 6 (Comparator).
> 
> $$
> \begin{gather*}
> x<y \iff y - x \in \mathbb{R}_{+} \\
> x>y \iff y<x \iff x-y \in \mathbb{R}_{+}
> \end{gather*}
> $$
In particular, $x>0$ iff $x \in \mathbb{R}_{+}$.

> [!math|{"type":"lemma","number":"auto","setAsNoteMathLink":false,"title":"Transitivity of Comparator","label":"transitivity-of-comparator","_index":6}] Lemma 7 (Transitivity of Comparator).
> If $a<b$ and $b<c$, then $a<c$. 
> `\begin{proof}`
> $a<b$ and $b<c$ mean that $b-a\in \mathbb{R}_{+}$ and $c-b\in\mathbb{R}_{+}$.
> 
> But, by , 
> 
> $$
> \begin{gather}
> (c-b)+(b-a) \in \mathbb{R}_{+} \\
> \implies c-a \in \mathbb{R}_{+} \\
> \implies a < c
> \end{gather}
> $$
> `\end{proof}`

> [!math|{"type":"lemma","number":"auto","setAsNoteMathLink":false,"_index":7}] Lemma 8.
> If $a<b$ and $c>0$, then $ac<bc$.
> `\begin{proof}`
> $b-a>0$ and $c>0$ implies by \ref that $(b-a)c>0 \implies bc-ac>0 \implies ac<bc$.
> `\end{proof}`

> [!math|{"type":"lemma","number":"auto","setAsNoteMathLink":false,"_index":8}] Lemma 9.
> $$
> a\neq 0\implies a^{2}>0
> $$
> `\begin{proof}`
> If $a>0$, then $a^{2}>0$ by previous lemma. 
> 
> Assume $a^{2}\leq0$. Then, because $a\neq 0$, we must have $a<0$. However, that implies by axiom 8 that $-a>0 \implies (-a)^{2}>0 \implies a^{2}>0$, a contradiction.
> `\end{proof}`

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"label":"upper-bound","_index":9,"title":"Upper Bound"}] Definition 10 (Upper Bound).
>Suppose $S$ is a nonempty subset of $\mathbb{R}$ and $B \in \mathbb{R}$ is such that $x\leq B$ for all $x \in S$. Then, we can say $B$ is an upperbound for $S$. If $B \in S$, we call B the maximum of $S$.

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Least Upper Bound","label":"least-upper-bound","_index":10}] Definition 11 (Least Upper Bound).
> $B \in \mathbb{R}$ is a least upper bound for a nonempty set $S$ if 
> 
> 1. $B$ is an upper bound for $S$.
> 2. No number less than $B$ is an upper bound for $S$

> [!math|{"type":"theorem","number":"auto","setAsNoteMathLink":false,"title":"Unique upper bound","label":"unique-upper-bound","_index":11}] Theorem 12 (Unique upper bound).
> The least upper bound for a set $S$ is unique
> `\begin{proof}`
> If there are 2 least upper bounds, $B_{1}$ and $B_{2}$, then $B_{1}\leq B_{2}$ and $B_{2}\leq B_{1}$ $\implies B_{1}=B_{2}$.
> `\end{proof}`

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Supremum and Infimum","label":"supremum-and-infimum","_index":12}] Definition 13 (Supremum and Infimum).
> If it exists, the least upper bound of a subset $S$ of set $P$ is called the supremum of $S$, denoted $\text{sup}(S)$. The greatest lower bound is the infimum, denoted $\text{inf}(S)$.

^56a279

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"title":"Continuitiy Axiom","label":"continuitiy-axiom","_index":13}] Axiom 14 (Continuitiy Axiom).
> Every nonempty set $S$ of $\mathbb{R}$ with an upper bound has a least upper bound or supremum.

^e56e85

> [!math|{"type":"theorem","number":"auto","setAsNoteMathLink":false,"_index":14}] Theorem 15.
> The natural number $\mathbb{N}$ are unbounded above.
> `\begin{proof}`Suppose instead that $\mathbb{N}$ is bounded above. Then, by continuity axiom, it has a supremum $B$. So $B-1$ is not an upper bound, so there is some $n \in \mathbb{N} \mid n>B-1$. But then $n+1\in\mathbb{N}$ has $n+1>B$, contradicting that $B$ is an upper bound.`\end{proof}`

> [!math|{"type":"theorem","number":"auto","setAsNoteMathLink":false,"label":"archimedean-property","_index":15,"title":"Archimedean Property"}] Theorem 16 (Archimedean Property).
> If $x>0$ any $y\in\mathbb{R}$, $\exists n \mid nx>y$.
> `\begin{proof}`If not, then $\frac{y}{x}\geq n$ for all $n\in \mathbb{N}$, so $\mathbb{N}$ would be bounded above.`\end{proof}`

> [!math|{"type":"theorem","number":"auto","setAsNoteMathLink":false,"title":"$\\sqrt{2}$","label":"sqrt","_index":16}] Theorem 17 ($\sqrt{2}$).
> 2 has a positive square root.
> `\begin{proof}`Let $S=\{ x \in \mathbb{R} \mid x^{2}\leq 2 \}$. Consider $\text{sup}(S)$. We claim that $\text{sup}(S)^{2}=2$, so we need to disprove that $\text{sup}(S)^{2} > 2$ and $\text{sup}(S)^{2}<2$. But first, we need to show that $\text{sup}(S)$ exists. To see that $S$ is non-empty, note that $0^{2}\leq 2$. To see that $S$ is bounded above, note $2^{2}=4>2$. Thus, by Continuity Axiom, $\text{sup}(S)$ does exist.  
> Let $B=\text{sup}(S)$. 
> Case A: $B^{2}>2$.
> Let $C=\frac{1}{2}(B+\frac{2}{B})$. Then, $C<B$. We can prove this by starting with $\frac{1}{2}\left( B+\frac{2}{B} \right) < B \iff \frac{1}{B} < \frac{B}{2} \iff 2<B^{2}$. But also, $C^{2}=\frac{1}{4}(B^{2}+4+\frac{4}{B^{2}}=2+\dots>2$. Therefore, $C$ is a smaller upper bound for $S$, contradicting the definition of $B=\text{sup}(S)$.
> Case B: $B^{2} < 2$. 
> Choose $C\mid C<B$, $C < \frac{2-B^{2}}{3B}, C>0$. Then, $(B+C)^{2}=B^{2}+2BC+C^{2}$. That is $B^{2}+C(2B+C)<B^{2}+3BC<B^{2}+(2-B^{2})=2$, contradicting that $B=\text{sup}(S)$. 
> `\end{proof}`