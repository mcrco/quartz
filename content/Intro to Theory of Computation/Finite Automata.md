# Finite Automata

- simple model of [[Computation]]
- reads input left to right, one symbol at a time
- maintains **state**
	- information about seen inputs
	- finite automaton $\implies$ finite # of states (loses memory over time)
- described by diagram or formally

## Diagram

![[Pasted image 20240105131038.png]]

- start arrow at left
- alphabet in example: $\{ 0,1 \}$
- states: $q_{1},q_{2},q_{3}$
	- $q_{3}$ is accept state
- transitions are arrows denoted by number (input)
- this FA decides $L=\{ x:x \in \{ 0,1 \}^{*},x_{n-1}=1 \land x_{n}=0 \}$
	- [[Computation#^3dcd80|language]]  is every string ending with $10$

## Formal Definition

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Finite Automaton","label":"finite-automaton","_index":0}] Definition 1 (Finite Automaton).
> A finite automaton is a 5-tuple
> $$
> \left( Q,\Sigma, \sigma, q_{0}, F \right)
> $$
> - $Q$: finite set called the states
> - $\Sigma$: finite set called the alphabet
> - $\delta$: [[Single Variable Calculus/Functions|function]] $Q\times\Sigma\to Q$ called transition function
> - $q_{0}$: start state
> - $F$: subset of $Q$ containing accept states

^02be7c

## FA [[Computation#^3dcd80|Languages]] 

- closure union "$C=A \cup B$"
	- [[Sets|set]] of languages recognized by FA is closed under union
- closure under concatenation "$C=A\circ B$"
	- $A\circ B=\{ xy:x \in A \land y\in B \}$
- closure under $\star$
	- $C=A^{\star}=x_{1}x_{2}\dots, x_{i} \in A$

But,

- how to concatenate?
	- can try turning accept states of $A$ into start states of $B$
	- but then FA might start parsing string for $B$ when it should still be parsing $A$
	- need free transition $\epsilon$
	- multiple transitions with same label?!
	- introduces non-determinism, creating

# Non-Deterministic Finite Automaton

- can think of NFA operation as
- $x$ is accepted if there exists a way of inserting $\epsilon$'s into $x$ so that
- there exists a path of transitions from start to accept state.

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Nondeterministic Finite Automaton","label":"nondeterministic-finite-automaton","_index":1}] Definition 2 (Nondeterministic Finite Automaton).
> $$
> (Q,\Sigma,\delta,q_{0},F)
>$$
>- $Q,\Sigma,q_{0},F$ are same as [[#^02be7c]] 
>- $\delta: Q \times (\Sigma \cup \{ \epsilon \}) \to P(Q)$ where $P$ is [[Sets#Power Set]] of $Q$.

^4cf5d5

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"NFA Operation","label":"nfa-operation","_index":2}] Definition 3 (NFA Operation).
> NFA $M$ accepts a string $w=w_{1}w_{2}w_{3}\dots w_{n} \in \Sigma^{*}$ if $w$ can be written as 
> $$
> y=y_{1}y_{2}y_{3}\dots y_{m} \in (\Sigma \cup \{ \epsilon \})^{*}
> $$
> and $\exists$ $r_{0},r_{1},\dots,r_{m}$ of states for which $r_{0}=q_{0}$, $r_{i+1} \in \delta(r_{i},y_{i+1})$ for $i=0,1,\dots ,m-1$ and $r_{m} \in F.$

# NFA and FA Equivalence

> [!math|{"type":"theorem","number":"auto","setAsNoteMathLink":false,"_index":3}] Theorem 4.
> A language $L$ is recognized by a finite automata iff $L$ is recognized by a non-deterministic finite automata.

`\begin{proof}` Since FA are NFA, it is trivial to prove recognition by FA $\implies$ recognition by NFA.

To prove NFA recognition $\implies$ FA recognition, we prove all NFA can be simulated by FA - by setting states of FA to be subsets of the set of states of NFA. That is, given NFA $M=(Q,\Sigma,\delta,q_{0},F)$, we can construct simulation FA $M'=(Q',\Sigma',\delta',q_{0}',F')$ where 

- $Q'=P(Q)$, 
- $F'=\{ R \in Q':Q\text{ contains accept state of }M \}$
- $\delta'$: $\delta'(R,a)=\cup_{r \in R} E(\delta(r,a))$
	- $E=$
- $q_{0}'=$

Now we should prove construction works by induction on number of steps of computation but nah.
`\end{proof}`

# Limitations

We can prove that there are languages FA can't recognize through the existence of [[Regular Expression#Non Regular Languages]].