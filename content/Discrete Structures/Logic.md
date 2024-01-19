# Logic

**Propositions** are statements that are either true or false. 

$p, q, r, s$ are propositions.

## Conjunction

Conjunction is the && operator in C++. We write it as $p \land q$. 

| $p$ | $q$ | $p \land q$ |
| --- | --- | ----------- |
| T   | T   | T           |
| T   | F   | F           |
| F   | T   | F           |
| F   | F   | F           |

## Or

Conjunction is the || operator in C++. We write it as $p \lor q$. 

| $p$ | $q$ | $p \land q$ |
| --- | --- | ----------- |
| T   | T   | T           |
| T   | F   | T           |
| F   | T   | T           |
| F   | F   | F           |

## Not

!= in C++. 

| $p$ | $-p$ |
| --- | ---- |
| T   | F    |
| F   | T    | 

## Conditional Proposition

Pretty much the if statement in C++

$p \implies q$

### Code

```cpp
if (p) 
	do q;
```

### Truth Table

| $p$ | $q$ | $p \implies q$ |
| --- | --- | -------------- |
| T   | T   | T              |
| T   | F   | F              |
| F   | T   | T              |
| F   | F   | T              |

### Creating New Propositions

Based on $p \implies q$, we can make 3 new propositions:

1. Converse: $q \implies p$
2. Inverse: $-p \implies -q$
3. Contrapositive $-q \implies -p$

The contrapositive is the only statement necessarily logically equivalent to the $p \implies q$.

## Biconditional Proposition

P happens if and only if q.

$$
p \iff q
$$

| $p$ | $q$ | $p \iff q$ |
| --- | --- | ---------- |
| T   | T   | T          |
| T   | F   | F          |
| F   | T   | F          |
| F   | F   | T          |

## Logical Equivalence

Two propositions produce the same ouput.

### Example

Is $p \land q$ logically equivalent to $-p \lor -q$?

| p   | q   | $p \land q$ | $-p \lor -q$ |
| --- | --- | ----------- | ------------ |
| T   | T   | T           | F            |
| T   | F   | F           | F            |
| F   | T   | F           | F            |
| F   | F   | F           | T            |

Nope.

## DeMorgan's Law

$$
\begin{align}
-(p \land q) &\leftrightarrow -p \lor q \\
- (p \lor q) &\leftrightarrow  -p \land -q
\end{align}
$$

## Rules

### Addition

Given $p$ is true, $p \lor q$ must be true.

### Modus Ponens

Given $p \implies q$ and $p$ is true, $q$ must be true.

## Negating Quantifiers

### Examples

$P(x)$: x is an accountant
$Q(x)$: x owns a Porsche

All accountants own Porches:

$$
\forall x (P(x) \implies Q(x))
$$

To negate,

$$
\exists x (P(x) \implies Q(x))
$$

is not true.



