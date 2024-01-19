The adjugate matrix is the transpose of the matrix of cofactors of $\mathbf{A}$. A cofactor is defined as 

$$
C_{ij} = (-1)^{i + j}\lvert M_{ij} \rvert
$$

where $|M_{ij}|$ is the determinant of the minor matrix for $A_{ij}$ .

The adjugate matrix is defined as 

$$
\text{adj}\mathbf{A} = \mathbf{C}^\intercal
$$

# Applications

## Matrix Inverse

The adjugate can be used to solve for the [[Inverse of a Matrix#Adjugate Matrix|inverse of a matrix]].

## Determinant Diagonal

$$
\mathbf{A} (\text{adj}\mathbf{A}) = \begin{pmatrix}
\det \mathbf{A} & 0 & 0 & \dots \\
0 & \det \mathbf{A} & 0 & \dots \\
0 & 0 & \det \mathbf{A} & \dots \\
0 & 0 & 0 & \det \mathbf{A}
\end{pmatrix}
$$

### Proof

We can see that

$$
\mathbf{A}(\text{adj}\mathbf{A})_{ij} = a_{i1}C_{j1} + a_{2i} C_{}
$$


The elements along the diagonal are equal to the determinant by definition. Take $\mathbf{A}_{1j}$ for example:

$$
\mathbf{A}(\text{adj}\mathbf{A})_{1j} = \mathbf{A}_{11} \cdot |\mathbf{M}_{11}| + \mathbf{A}_{12} \cdot |\mathbf{M}_{12}| \dots
$$



