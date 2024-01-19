# Question 1

## Discussion

As with other set equality proofs, we want to show that both sets are subsets of one another: $\overline{S \cap T} \subset \bar{S} \cup \bar{T}$ and $\bar{S}\cup \bar{T} \subset \overline{S \cap T}$. As with the other DeMorgan's Law subset proof, we will use one of DeMorgan's Logic Laws: $\neg (p \land q) \equiv \neg p \lor \neg q$. 

## Proof

To prove the set equality, we want to show that both sets are subsets of one another: $\overline{S \cap T} \subset \bar{S} \cup \bar{T}$ and $\bar{S}\cup \bar{T} \subset \overline{S \cap T}$. 

For $\overline{S \cap T} \subset \bar{S} \cup \bar{T}$, we assume that $x \in \overline{S \cap T}$. Thus, $x\notin S \cup T$, and the statement $x \in S$ and $x \in T$ cannot be true. By DeMorgan's Logic Laws, this is equivalent to $x \notin S$ or $x \notin T$ being true. If $x \notin S$, $x \in \bar{S}$, and if $x \notin T$, $x \in \bar{T}$, so $x$ is in the union of $x \in \bar{S} \cap \bar{T}$. Thus, $\overline{S \cap T} \subset \bar{S} \cup \bar{T}$.

For the other inclusion, we assume that $x \in \bar{S} \cup \bar{T}$. This means $x \notin S$ or $x \notin T$. By DeMorgan's Logic Laws, this is the same as $x \in S$ and $x \in T$ not being true. Thus, $x \notin S \cap T$, and so $x \in \overline{S \cap T}$. Thus, $\bar{S} \cup \bar{T} \subset \overline{S\cap T}$.

Since we have proved both subset inclusions, the two sets are equal: $\overline{S \cap T} = \bar{S} \cup \bar{T}$.

# Question 2

Prove $S \cap (T \cup R) = (S \cap T) \cup (S \cap R)$.
## Discussion

We want to show that the two sets are subsets of one another: $S \cap (T \cup R) \subset (S \cap T) \cup (S \cap R)$ and $(S \cap T) \cup (S \cap R) \subset S \cap (T \cup R)$. 

For the first subset inclusion, we will assume $x \in S \cap (T \cup R)$. We can break it down to the cases $x \in S$ and $x \in T$ or $x \in S$ and $x \in R$ and prove that both cases lead to the subset inclusion.

For the second subset inclusion, we will assume $x \in (S \cap T) \cup (S \cap R)$. We will split it up into the cases $x \in S \cap T$ or $x \in S \cap R$. In the first case, we will use the fact that $x \in T \subset T \cup R$ and $x \in S$ to say that $x$ is in the intersection of $S$ and $T \cup R$, meaning $x \in S \cap (T \cup R)$. Thus, $(S \cap T) \cup (S \cap R) \subset S \cap (T \cup R)$ in the first case. Similarly, we will use the fact that $x \in R \subset (T \cup R)$ and $x \in S$ in the second case to say that $x \in S \cap (T \cup R)$. Thus, the subset inclusion is true in both cases.

## Proof

We will prove the set equality by proving that the two sets are subsets of one another: $S \cap (T \cup R) \subset (S \cap T) \cup (S \cap R)$ and $(S \cap T) \cup (S \cap R) \subset S \cap (T \cup R)$. 

For the first subset inclusion, we will assume $x \in S \cap (T \cup R)$. Thus, $x \in S$ and $x \in T \cup R$ are both true. $x \in T \cup R$ gives us 2 cases: $x \in T$ or $x \in R$. In the first case, $x \in T$, so $x \in S$ and $x \in T$ are both true. Thus, $x$ is in the intesection of the 2 sets, or $x \in S \cap T$, and since $S \cap T \subset (S \cap T) \cup (S \cap R)$, $S \cap (T \cup R) \in (S \cap T) \cup (S \cap R)$ in this first case. In the second case, $x \in R$, so $x \in S$ and $x \in R$ are both true and $x$ is in the intersection of $S$ and $R$, thus $x \in S \cup R$. Since $x \in S \cup R \subset (S \cap T) \cup (S \cap R)$, $S \cap (T \cup R) \subset (S \cap T) \cup (S \cap R)$ is true for both possible cases.

For the second subset inclusion, we will assume $x \in (S \cap T) \cup (S \cap R)$. The "or" statement gives us 2 cases: $x \in S \cap T$ or $x \in S \cap R$. In the first case, we know that $x \in S$ and $x \in T$ are both true. Since $x \in T \subset T \cup R$, we can say $x \in S$ and $x \in T \cup R$ are both true. Thus, $x$ is in the intersection of $S$ and $T \cup R$, so $x \in S \cap (T \cup R)$. Thus, $(S \cap T) \cup (S \cap R) \subset S \cap (T \cup R)$ is true in the first case. In the second case, we know that $x \in S$ and $x \in R$ are both true. Since $x \in R \subset T \cup R$, we can say $x \in S$ and $x \in T \cup R$ are both true, giving us $x \in S \cap (T \cup R)$ again. Thus, $(S \cap T) \cup (S \cap R) \subset S \cap (T \cup R)$ is true in both cases.

Since we have proven both subset inclusions, we have proven the 2 sets are equal.

# Question 3

Show that if $A \subset B$ and $C \subset D$, then $A \times C \subset B \times D$. 

## Discussion

Assuming $(x,y) \in A \times C$. We will use $x \in A \subset B$ to say $x \in B$ and likewise with $y \in C \subset D$ to say $y \in D$. Thus, for any $(x,y) \in A \times C$, $(x,y) \in B \times D$ is also true. 

## Proof

To prove the subset inclusion, we will assume $(x,y) \in A \times C$. Since $x \in A \subset B$, $x \in B$ is true. Since $y \in C \subset D$, $y \in D$ is true. Since $x \in B$ and $y \in D$, we know that $(x,y) \in B \times D$. Thus, $A \times C \subset B \times D$.

# Question 4

Show that $A \times (B \cap C) = (A \times B) \cap (A \times C)$.

## Discussion

The 2 subset inclusions we need to prove are $A \times (B \cap C) \subset (A \times B) \cap (A \times C)$ and $(A \times B) \cap (A \times C) \subset A \times (B \cap C)$. We will use the general tuple form $(x,y)$ to represent an arbitrary element in each set and use the properties of $x$ and $y$ to show that they will be in the other set as well.

## Proof

To prove the set equality, we will prove 2 subset inclusions:$A \times (B \cap C) \subset (A \times B) \cap (A \times C)$ and $(A \times B) \cap (A \times C) \subset A \times (B \cap C)$.

For the first subset inclusion, we will assume $(x,y) \in A \times (B \cap C)$. Thus, $x \in A$ and $y \in B \cap C$. Since $y \in B \cap C$, $y \in B$ and $y \in C$. Since $x \in A$ and $y \in B$, we know that $(x,y) \in A \times B$. Since $x \in A$ and $y \in C$, we know that $(x,y) \in A \times C$. Since $(x,y) \in A \times B$ and $(x,y) \in A \times C$, we know that $(x,y)$ is in the intersection of the two sets, we can conclude that $(x,y) \in (A \times B) \cap (A \times C)$. Thus, $A \times (B \cap C) \subset (A \times B) \cap (A \times C)$.

For the second subset inclusion, we will assume $(x,y) \in (A \times B) \cap (A \times C)$. Thus, $(x,y) \in A \times B$ and $(x,y) \in (A \times C)$. Since $(x,y) \in A \times B$, we know that $x \in A$ and $y \in B$. Since $(x,y) \in A \times C$, we additionally know that $y \in C$. Since $y \in B$ and $y \in C$, $y$ is in the intersection of the 2 sets, so $y \in B \cap C$. Thus, $(x,y) \in A \times (B \cap C)$, and $(A \times B) \cap (A \times C) \subset (A \times (B \cap C)$ is true.


# Question 5

Show that 

$$
A \times (B \cup C) = (A \times B) \cup (A \times C)
$$

## Discussion

We want to prove the set equality with 2 subset inclusions: $A \times (B \cup C) \subset (A \times B) \cup (A \times C)$ and $(A \times B) \cup (A \times C) \subset A \times (B \cup C)$. We will use the general form of a tuple in either set and use the properties of $(x,y)$ to show that both sets are subsets of one another. 

For the first subset inclusion, we will do casework on $y \in B \cup C$. For the second subset inclusion, we will do casework on $(x,y) \in A \times B$ and $(x,y) \in (A \times C)$. 

## Proof

To prove the set equality, we will prove 2 subset inclusions: $A \times (B \cup C) \subset (A \times B) \cup (A \times C)$ and $(A \times B) \cup (A \times C) \subset A \times (B \cup C)$.

For the first subset inclusion, we will assume $(x,y) \in A \times (B \cup C)$. Thus, $x \in A$ and $y \in B \cup C$. Since $y \in B \cup C$, we will break it up into two cases: when $y \in B$ and when $y \in C$. When $y \in B$, since $x \in A$ and $y \in B$, $(x,y) \in (A \times B) \subset (A \times B) \cup (A \times C)$. When $y \in C$, since $x \in A$ and $y \in B$, $(x,y) \in (A \times C) \subset (A \times B) \cup (A \times C)$. Since $(x,y) \in (A \times B) \cup (A \times C)$ in both cases, we can conclude that $A \times (B \cup C) \subset (A \times B) \cup (A \times C)$.

For the second subset inclusion, we will assume that $(x,y) \in (A \times B) \cup (A \times C)$. We will break it up into 2 cases: when $(x,y) \in A \times B$ and when $(x,y) \in (A \times C)$. When $(x,y) \in A \times B$, $x \in A$ and $y \in B$. Since $y \in B \subset B \cup C$, $y \in B \cup C$. Since $x \in A$ and $y \in B \cup C$, we can conclude $(x,y) \in A \times (B \cup C)$. When $(x,y) \in A \times C$, $x \in A$ and $y \in C$. Since $y \in C \subset B \cup C$, $y \in B \cup C$. Since $x \in A$ and $y \in B \cup C$, we can conclude $(x,y) \in A \times (B \cup C)$. Since $(x,y) \in A \times (B \cup C)$ in both cases, we can conclude $(A \times B) \cup (A \times C) \subset A \times (B \cup C)$.

By proving both subset inclusions, we have proven that $A \times (B \cup C) = (A \times B) \cup (A \times C)$.