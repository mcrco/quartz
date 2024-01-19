# Sets

- collection of objects
- use {} to denote sets
- no order
- no duplicate objects

## Implementation in C++

```cpp
#include set

// Create a set
set<int> int_set

// Insert element
int_set.insert(1)

// Get set size
int_set.size()

// Iterate through elements
set<int> :: iterator iter;
iter = int_set.begin();
while (iter != int_set.end()) {
	cout << *iter;
}

// Find element
iter = int_set.find(1);
cout << (iter != int_set.end());

```

## Belonging

- basic function of set
- use $\in$

## Elements

- must limit elements of set
- don't -> Russel's paradox
	- set is element of itself??

## Empty Set

- nothing in it
	- null
- special
- write as {}

## Comparing 

- contains: $\subseteq$
- equals: $A \subseteq B, B \subset A \implies A = B$

## Power Set

The power set is the set of all subsets of a set.
$$
P(\{ a,b \}) = \{\{  \}, \{ a \},\{ b \},\{ a,b \}\}
$$

## Cardinality

Cardinality is just the number of elements in set.

$$
A=\{ 1,2 \} \implies |A| = 2
$$

Since the power set of $A$ has $2^{|A|}$ elements, 

$$
|P(A)| = 2^{|A|}
$$

## Combining Sets

### Union

Union combines two sets. 

$$
\begin{align}
A = \{ 1,2,6 \} \\
B = \{ 1,4,7 \} \\
A \cup B = \{ 1,2,4,6,7 \}
\end{align}
$$

Can also find partial union:

$$
A \cup_{i=1}^2 B = \{ 1,2,4 \}
$$

### Intersection

Intersection finds the intersection of sets

$$
\begin{align}
A = \{ 1,2,6 \} \\
B = \{ 1,4,7 \} \\
A \cap B = \{ 1 \}
\end{align}
$$

Two sets $A$ and $B$ are disjoint if 

$$
A \cap B = \{  \}
$$

### Set Difference

Subtracting set $B$ from set $A$ means

$$
A - B = {x \in A | x \notin B}
$$

Example:

$$
\begin{align}
A &= \{ 1,2,5,7,8 \} \\
B &= \{ 1,2,3 \} \\
A - B &= \{ 5,7,8 \}
\end{align}
$$

Now, $B$ and $\{ 5,7,8 \}$ are complements.

## Partition

A partition is the breakdown of a set into disjoint subsets.

## Cartesian Product

Gives set involving all possible pairs between sets $A$ and $B$

$$
\begin{align}
A &= \{ 1,2 \} \\
B &= \{ 3,4,5 \} \\
A \times B &= \{ (1,3), (1,4), (2,3), (2,4), (2,5) \}
\end{align}
$$