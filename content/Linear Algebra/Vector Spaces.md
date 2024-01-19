- a vector space over a [[Fields|field]] $F$ is a set of of vectors where
	- addition is [[Vectors#^cbddf2]] 
	- multiplication is [[Vectors#^85a8b3]] 
- and satisfies the below axioms

# Addition

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"title":"Commutativity","label":"commutativity","_index":0}] Axiom 1 (Commutativity).
> $\vec{u}+\vec{v}=\vec{v}+\vec{u}$.

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"title":"Associativty","label":"associativty","_index":1}] Axiom 2 (Associativty).
> $(\vec{u}+\vec{v})+\vec{w}=\vec{u}+(\vec{v}+\vec{w})$.

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"title":"Zero Vector","label":"zero-vector","_index":2}] Axiom 3 (Zero Vector).
> Exists a vector $\vec{0}$ s.t. $\vec{v}+\vec{0}=\vec{v}$.

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"title":"Additive Inverse","label":"additive-inverse","_index":3}] Axiom 4 (Additive Inverse).
> $\forall \, \vec{v} \in V$, $\exists \, \vec{w}$ s.t. $\vec{v}+\vec{w}=\vec{0}$. $\vec{w}=-\vec{v}$.

^7661b4

## Multiplication

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"title":"Multiplicative Identity","label":"multiplicative-identity","_index":4}] Axiom 5 (Multiplicative Identity).
> $\exists \, 1 \in V$ s.t. $1\vec{u} = \vec{u}$.

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"title":"Multiplicative Associativity","label":"multiplicative-associativity","_index":5}] Axiom 6 (Multiplicative Associativity).
> For scalars $c,d$, $c(d\vec{u}) = (cd)\vec{u}$.

# Distribution

- connects addition and multiplication

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"title":"First Distribution","label":"first-distribution","_index":6}] Axiom 7 (First Distribution).
> $c(\vec{u} + \vec{v}) = c\vec{u} + c\vec{v}$.

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"title":"Second Distribution","label":"second-distribution","_index":7}] Axiom 8 (Second Distribution).
> $(c + d)\vec{u} = c\vec{u} + d\vec{u}$.

# Examples

- vector spaces over $\mathbb{R}$
	- $V=\mathbb{R}^{2}$
	- $V=\{ f:\mathbb{R}\to\mathbb{R} \}$
	- $V=\{ \text{continuous }f:\mathbb{R}\to\mathbb{R} \}$
	- $V=\{ p(x)=a_{0}+a_{1}x+\dots+a_{n}x^{n} \}$ where $a_{0},\dots a_{n}\in\mathbb{R}$
	- For field $K$, $K^{n}=\{ (a_{1},a_{2}, \dots, a_{n}) \} | a_{i} \in K$
		- $K-$vector space

# Subspace

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Vector Subspace","label":"vector-subspace","_index":8}] Definition 9 (Vector Subspace).
> If $V$ is a $K-$vector subspace then a subspace of $V$ is a subset $W \subset V$ s.t. $W$ is also a $K-$vector space using the same operations.

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Closure under Operation","label":"closure-under-operation","_index":9}] Definition 10 (Closure under Operation).
> A subset $S \subset V$ is closed under $\star$ if given $\vec{s}_{1}, \vec{s}_{2} \in S$ then $\vec{s}_{1}\star\vec{s_{2}}\in S$.

- vector spaces are also closed under addition and scalar multiplication, but didn't have to define since [[Vectors#^cbddf2|addition]] and [[Vectors#^85a8b3|multiplication]] are [[Vectors#^aed3cb|binary operations]] and closing by default
- notice that

> [!math|{"type":"proposition","number":"auto","setAsNoteMathLink":false,"_index":10}] Proposition 11.
> Nonempty $W \subset V$ is subspace $\iff$ $W$ is closed under addition and scalar multiplication

## Axioms

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"_index":11}] Axiom 12.
> $\vec{0} \in W$ always.

`\begin{proof}`For any $\vec{w} \in W$, $0 \cdot \vec{w}=\vec{0} \implies \vec{w} \in W$.`\end{proof}`

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"_index":12}] Axiom 13.
> [[#^7661b4|Additive Inverse]] $\in W$ always
> 

`\begin{proof}`For any $\vec{w} \in W$, $-1 \cdot \vec{w} = -\vec{w}$. `\end{proof}`

## Subspaces of $\mathbb{R}^{2}$

- if $W$ is subspace, then
- $\vec{w} \in W \neq \vec{0} \implies \lambda \vec{w} \in W$ for $\lambda \in \mathbb{R}$
- $L=\{ \lambda \cdot \vec{w} \mid \lambda \in \mathbb{R} \}$ is subspace (check for closure)
	- $L$ is actually just a line through $\vec{0}$ if visualized on plane

> [!math|{"type":"claim","number":"auto","setAsNoteMathLink":false,"_index":13}] Claim 14.
> If $W \subset V$ is a subspace, it's either $\vec{0}, \mathbb{R}^{2}$, or line through $\vec{0}$.

`\begin{proof}`Given $W$, assume it's not $\{ \vec{0} \}$
`\end{proof}`

> [!math|{"type":"claim","number":"auto","setAsNoteMathLink":false,"_index":14}] Claim 15.
> Given any $\vec{u} \in \mathbb{R}^{2}$, can write $\vec{u}=\lambda \vec{w} + \mu \vec{v}$ for unique $\lambda,\mu$

