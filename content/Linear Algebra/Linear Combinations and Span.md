In $xy$ plane, $\hat{i}$ and $\hat{j}$ are called **basis vectors**. 

Using a linear combination (scaled sum) of $\hat{i}$ and $\hat{j}$, we can reach any vector in 2D space. In this case, the 2D space is the **span** (set of all possible linear combinations) of $\hat{i}$ and $\hat{j}$. 

Notice that the span is not the same for basis vectors that line up or are 0.

The property that describes a basis vector that adds another dimension to span is **linear independence**. 

A more formal definition for linear independence within a set of vectors is $\vec{v}_{1}, \vec{v}_{2}, \dots \vec{v}_{p}$ are linearly independent if and only if 

$$
c_{1}\vec{v}_{1} + c_{2} \vec{v}_{2} \dots = 0
$$

has only trivial solution $\vec{c} = \vec{0}$

A set of vectors is linearly dependent if one of the following happen:

1. $v_{i} = \vec{0}$
2. $\vec{v}_{i} = k\vec{v}_{m}$
3. A vector is a linear combination of the rest
4. The number of vectors is greater than the number of components of each vector.

**Technical definition of basis**: The basis of a vector space is a set of linearly independent vectors that span the full space.