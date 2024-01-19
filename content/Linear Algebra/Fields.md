> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Field","label":"field","_index":0}] Definition 1 (Field).
> A field is a set $F$ together with 2 binary operations(addition and multiplication) that satisfy the below axioms.
> 1. Associativity
> 2. Commutativity
> 3. Additive Inverses
> 4. Additive Identity
> 5. Multiplicative Identity

# Axioms

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"title":"Associativity","label":"associativity","_index":1}] Axiom 2 (Associativity).
> $(a+b)+c=a+(b+c)$ and $(a\cdot b)\cdot c=a\cdot(b\cdot c)$ for $a,b,c \in F$

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"title":"Commutativity","label":"commutativity","_index":2}] Axiom 3 (Commutativity).
> $a+b=b+a$ and $a\cdot b=b\cdot a$.

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"title":"Identities","label":"identities","_index":3}] Axiom 4 (Identities).
> $\exists$ two distinct elements $0,1$ s.t. $a+0=a$ and $a\cdot{1}=a$ for $a \in F$.

^18bb35

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"title":"Inverses","label":"inverses","_index":4}] Axiom 5 (Inverses).
> For $a \in F$, 
> 1. $\exists$ $-a$ s.t. $a+(-a)=0$ and 
> 2. $\exists$ $a^{-1}$ s.t. $a \cdot a^{-1}=1$.

> [!math|{"type":"axiom","number":"auto","setAsNoteMathLink":false,"title":"Distributivitiy","label":"distributivitiy","_index":5}] Axiom 6 (Distributivitiy).
> $a\cdot(b+c)=ab+ac$.



# Examples

- Fields: $\mathbb{Q}$, $\mathbb{R}$, $\mathbb{C}$
- Non-fields: $\mathbb{Z}$ with addition and multiplication

## Binary Field

- unique field structure on the set $F=\{ 0,1 \}$
- example of a finite field
- suffices to determine addition and multiplication tables
- addition table:

|  | 0   | 1   |
| --- | --- | --- |
| 0   | 0   | 1   |
| 1   | 1   | 0    |

- $1+1$ must equal $0$ since $1+1=1\implies 1=0$ which violates [[#^18bb35]]
- multiplication table:

|     | 0   | 1   |
| --- | --- | --- |
| 0   | 0   | 0   |
| 1   | 0    | 1    |
