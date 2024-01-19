# Span

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Linear Combination","label":"linear-combination","_index":0}] Definition 1 (Linear Combination).
> A vector of the form
> $$
> \sum_{i=1}^{n}a_{i}\cdot \vec{v_{i}}
> $$
> where $\vec{v_{i}} \in$ some vector space $V$ over $\mathbb{F}$ and $a_{i} \in \mathbb{F}$.

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Span","label":"span","_index":1}] Definition 2 (Span).
> For $K$-[[Vector Spaces|vector space]] $V$, $S=\{ v_{1},v_{2},\dots,v_{n} \} \subset V$, $\text{span}(S)=\{ a_{1}\vec{v}_{1} + \dots + a_{n}\vec{v}_{n} \}$ (set of all linear combinations). $S$ spans $V$ (or generates $V$) if $\text{span}(S)=V$ aka .

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Finite Dimensional","label":"finite-dimensional","_index":2}] Definition 3 (Finite Dimensional).
> A [[Vector Spaces|vector space]] is finite dimensional if finite set of vectors spans it.

- example: $\mathbb{R}^{2}$ is finite dimensional
- $\vec{u} \in \mathbb{R}^{2} =a\vec{v}_{1} + b\vec{v}_{2}$ for $a,b \in \mathbb{R}$ if $\vec{v_{1}}, \vec{v_{2}}$ are not on the same line through $(0,0)$. 
- this property of $\{ \vec{v_{1}},\vec{v_{2}} \}$ is called

# Linear Independence

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Linear Independence","label":"linear-independence","_index":3}] Definition 4 (Linear Independence).
> Given a set $S \subset V$, $S$ is linearly independent if given $a_{1}\vec{v_{1}}+\dots+a_{n}\vec{v_{n}}=\vec{0}$ with $a_{i} \in K$ and $\vec{v_{i}} \in S$ distinct, then $a_{1}=a_{2}=\dots=a_{n}=0$. 

> [!math|{"type":"theorem","number":"auto","setAsNoteMathLink":false,"_index":4}] Theorem 5.
> If $S$ is linearly independent then $T \subset S$ is linearly independent.

- opposite would be

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Linear Dependence","label":"linear-dependence","_index":5}] Definition 6 (Linear Dependence).
> $S$ is linearly dependent if for $a_{1},\dots, a_{k} \in K$, $\vec{v_{1}},\dots,\vec{v_{n}} \in S$, $a_{1}\vec{v_{1}}+\dots+a_{n}\vec{v_{n}}=\vec{0}$ w/ some $a_{i}\neq 0$.

# Bases

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Basis","label":"basis","_index":6}] Definition 7 (Basis).
> Basis of $V$ ($\mathcal{B}(V)$) is a list of vectors that is linearly independent and spans $V$.

^c71fc8

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"title":"Basis","label":"basis","_index":7}] Proposition 8 (Basis).
> $S \subset V$ is a basis $\iff$ every vector $\vec{v} \in V$ can be expressed uniquely as $\vec{v} = a_{1}\vec{v_{1}} + \dots + a_{n}\vec{v_{n}}$.

`\begin{proof}`
$\impliedby$: definition of span
$\implies$: for $\vec{v}=a_{1}\vec{v_{1}}+\dots+a_{n}\vec{v_{n}}$ and $\vec{w}=b_{1}\vec{v_{1}}+b_{n}\vec{v_{n}}$,  $\vec{v}=\vec{w}\implies \vec{v}-\vec{w}=\vec{0}\implies (a_{1}-b_{1})\vec{v_{1}} + \dots + (a_{n}-b_{n})\vec{v_{n}} \implies a=b$
`\end{proof}`

> [!math|{"type":"example","number":"auto","setAsNoteMathLink":false,"title":"Standard Basis","label":"standard-basis","_index":8}] Example 9 (Standard Basis).
> $V=K^{n}$ has a standard basis $S=\{ e_{1},\dots,e_{n} \}$:
> $\vec{e_{1}}=(1,0,\dots,0)$
> $\vec{e_{2}}=(0,1,\dots,0)$
> ...
> $\vec{e_{n}}=(0,0,\dots,1)$

- example: a polynomial of degree $\leq d$ has standard basis $\{ 1,x,x^{2},\dots,x^{d} \}$

## Dimension

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Dimension","label":"dimension","_index":9}] Definition 10 (Dimension).
> If $V$ is basis $S$, **dimension** of $V$, or $\text{dim}(V)$ is $|S|$

> [!math|{"type":"claim","number":"auto","setAsNoteMathLink":false,"_index":10}] Claim 11.
> $\text{dim}$ is well defined: any two bases of a finite dimensional vector space have same length.

`\begin{proof}`Suppose $S,T$ are bases. Then, if $S$ is linearly independent and $T$i s spanning,

$$
|S|\leq|T|.
$$

Since we can flip around WLOG, 

$$
|T|\leq|S|.
$$

Thus, $|S|=|T|$.
`\end{proof}`

# Connection to [[Sets]]

- finite set $\iff$ finite dimensional
- $|A| \iff \text{dim}V$
- $A_{1} \cup A_{2} \iff V_{1} + V_{2}$
- $|A_{1} \cup A_{2}| = |A_{1}| + |A_{2}| - |A_{1} \cap A_{2}| \iff \text{dim}(V_{1}+V_{2}) = \text{dim}(V_{1}) + \text{dim}(V_{2}) - \text{dim}(V_{1} \cap V_{2})$