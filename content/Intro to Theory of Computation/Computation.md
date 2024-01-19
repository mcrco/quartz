# Problem

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Problem","label":"problem","_index":0}] Definition 1 (Problem).
> A problem associates each input to an output. Input and output are strings over a finite alphabet $\Sigma^{}$. $\Sigma^{\star}$ is infinite [[Sets|set]] of finite strings.
> 
> $$
> f:\Sigma ^{\star} \to \Sigma^{\star}
> $$

More simply,

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Decision Problem","label":"decision-problem","_index":1}] Definition 2 (Decision Problem).
> $f:\Sigma^{\star} \to \{ \text{accept}, \text{reject} \}$

**Every problem has a simpler decision problem**.

## Prime Factoring

Given an integer $m$, find its prime factors. Integers are represented as $\{ 0,1 \}^{\star}$ cuz binary.

### Problem

$$
f_{\text{factor}}:\{ 0,1 \}^{\star}\to \{ 0,1 \}^{\star}.
$$

$f_{\text{factor}}$ outputs [[Sets|set]] of prime factors.

### Decision

$$
f:\{ m,k \}\to \{ \text{accept}, \text{reject} \}.
$$

$f$ outputs whether or not $m$ has a prime factor smaller than $k$. Can be paired with binary search to solve original problem.

# Computation

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Computation","label":"computation","_index":2}] Definition 3 (Computation).
> $$
> \text{input} \to \text{machine} \to \begin{cases}
> \text{accept} \\
> \text{reject} \\
> \text{loop forever}
> \end{cases}
> $$

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Language","label":"language","_index":3}] Definition 4 (Language).
> $L \subseteq \Sigma^{\star}$: subset of strings over $\Sigma^{}$

^3dcd80

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Recognition","label":"recognition","_index":4}] Definition 5 (Recognition).
> [[Sets|set]] of strings that lead to accept is language **recognized** by machine

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Decision","label":"decision","_index":5}] Definition 6 (Decision).
> every other string ($x \notin L$) leads to reject $\implies$ language is **decided** by the machine