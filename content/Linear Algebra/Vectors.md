- magnitudes in directions
- ordered tuples
- point in space

$$
\mathbb{R}^{n}=\left\{  
\begin{pmatrix}
x_{1} \\
x_{2} \\
\dots \\
x_{n}
\end{pmatrix}
\right\}  
$$

# Operations

## Addition

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Addition","label":"addition","_index":0}] Definition 1 (Addition).
> 
> 
> For
> 
> $$
> \vec{v}=\begin{pmatrix}
> x_{1} \\
> y_{1}
> \end{pmatrix},
> \vec{w}=\begin{pmatrix}
> x_{2} \\
> y_{2}
> \end{pmatrix}
> ,$$
> 
> $$
> \vec{v}+\vec{w}=\begin{pmatrix}
> x_{1}+x_{2} \\
> y_{1}+y_{2}
> \end{pmatrix}
> .$$
> 

^cbddf2

**Intuition**: joining two arrows from tail to head

## Scalar Multiplication

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Scalar Multiplication","label":"scalar-multiplication","_index":1}] Definition 2 (Scalar Multiplication).
> 
>$$
>\alpha\cdot \begin{pmatrix}
>x \\
>y
>\end{pmatrix}
> = \begin{pmatrix}
>\alpha x \\
>\alpha y
>\end{pmatrix}
>.$$
>

^85a8b3

**Intuition**: scaling arrow in direction by $\alpha$.

# Binary Operation

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"BInary Operation","label":"binary-operation","_index":2}] Definition 3 (BInary Operation).
> For set $S$, binary operation $*$: $S\times S\to S$ 
> Examples: $\times, +$ on $\mathbb{R}$, $\circ$ on $\{ f:\mathbb{R}\to\mathbb{R} \}$

^aed3cb

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Commutative","label":"commutative","_index":3}] Definition 4 (Commutative).
> $*$ is commutative if $a*b=b*a$ for $a,b \in S$. 
> Ex: $\times,+$ are commutative, $\circ$ is not.

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Associative","label":"associative","_index":4}] Definition 5 (Associative).
> $(a*b)*c=a*(b*c)$ for all $a,b,c \in S$
> Example: $+, \circ, \times$ are all associative.

## Identity Element

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Identity Element","label":"identity-element","_index":5}] Definition 6 (Identity Element).
> $e\in S$ is identity element for $*$ if 
> $$
> e * s = s * e = s
> $$
> for all $s \in S$.
> Examples: $f(x)=x$ is identity element of $S=\{ f:\mathbb{R}\to\mathbb{R} \}$

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"title":"Unique Identity","label":"unique-identity","_index":6}] Proposition 7 (Unique Identity).
> Identity elements are unique.
>
>`\begin{proof}`Suppose $e,f$ are both identities. Then,
>
>$$
>e=e* f=f
>$$
>`\end{proof}`

# Inverses

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Inverse","label":"inverse","_index":7}] Definition 8 (Inverse).
> For $*$ with identity $e$, then $b \in S$ is inverse to $a \in S$ if $a*b=b*a=e$.

### Inverses for Composition

$$
g = f^{-1} \iff f(g(x))=x \, \land \, g(f(x))=x.
$$

- to solve $g(f(x))=x$, need $f$ is [[Single Variable Calculus/Functions#Injection|injective]]
	- then set $g(f(x))=x$ for all $x$, $g(y)=0$ if $y $
- to solve $f(g(x))=x$, need $f$ is [[Single Variable Calculus/Functions#Surjection|surjective]]


