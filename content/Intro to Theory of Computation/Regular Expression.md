> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Regular Expression","label":"regular-expression","_index":0}] Definition 1 (Regular Expression).
> $R$ is a regex if $R$ is
> - $a \in \Sigma$
> - $\epsilon$: empty string
> - empty set
> - $R_{1} \cup R_{2}$, where $R_{1}$ and $R_{2}$ are regex
> - $(R_{1} \circ R_{2})$ where $R_{1}$ and $R_{2}$ are regex
> - ($R_{1}^{\star}$) where $R_{1}$ is a regex

^a8210c

# Connection to [[Finite Automata]]

> [!math|{"type":"theorem","number":"auto","setAsNoteMathLink":false,"_index":1}] Theorem 2.
> A [[Computation#^3dcd80|language]] is recognized by a [[Finite Automata#^02be7c|FA]] $\iff$ $L$ is described by a [[#^a8210c]].  

`\begin{proof}`
$\implies$ (L is recognized if L is described by regex): 
By the rules of what a regex is by definition, we can see that the regex can describe transitions through a NFA.

$\impliedby$ (L is described by regex if L is recognized):
For a FA $M$, we can construct a GNFA:

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"Generalized NFA","label":"generalized-nfa","_index":2}] Definition 3 (Generalized NFA).
> A [[Finite Automata#^4cf5d5|NFA]] that has transitions in the form of regex. 

Notice that for a 2-state GNFA with just a start and accept state with transition $R$ (some regex), we have proven that the recognized language can be expressed by regex.

Now, we prove that $k$-state GNFA $G$ can be reduce to 2 states by simply ripping out every intermediate state by replacing regex transitions with a more robust one. Let $q_{i},q_{j},q_{r}$ be 3 states in $G$, with transitions $R_{1}: q_{i}\to q_{r}, R_{2}: q_{r}\to q_{r}, R_{3}: q_{r}\to q_{j}, R_{4}: q_{i}\to q_{j}$. Then, we can rip $q_{r}$ by setting the transition $q_{i} \to q_{j}$ with $(R_{1})(R_{2}^\star)(R_{3}) \cup R_{4}$.
`\end{proof}`	

# Non Regular Languages

> [!math|{"type":"lemma","number":"auto","setAsNoteMathLink":false,"title":"Pumping Lemma","label":"pumping-lemma","_index":3}] Lemma 4 (Pumping Lemma).
>For all regular languages $L$, there is a pumping length $p$ s.t. for all words $w=xyz$ with $|w| > p$, 
> 1. $w = xy^iz \in L$ for all $i\geq 0$
> 2. $|y| > 0$
> 3. $|xy| < p$

We can prove a language is non-regular by

1. assume $L$ is regular
2. must exist pumping length $p$
3. select string $w \in L$ of length $\geq p$
4. no matter how you write $w=xyz$ satisfying rules 2 and 3, pumping $y$ cannot give string in $L$
5. profit