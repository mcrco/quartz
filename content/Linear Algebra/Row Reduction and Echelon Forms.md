# Definitions

**leading entry**: leftmost non-zero entry of row

**echelon form**: 
1. all non-zero rows are above all-zero rows
2. leading entry of row is to the right of leading entry of column above
3. all entries in column below leading entry are 0

**reduced echelon matrix**:
1. echelon form
2. leading entry in each nonzero row is 1

# Example Problem

Express in row-echelon form

$$
\begin{align}
\begin{pmatrix}
0 & -3 & -6 & 4 & 9 \\
-1 & -2 & -1 & 3 & 1 \\
-2 & -3 & 0 & 3 & -1  \\
1 & 4 & 5 & -9 & -7
\end{pmatrix}
\end{align}
$$

$$
\begin{align}
R_{1} \leftrightarrow  R_{3}, R_{2} \to \frac{1}{2}(R_{2} + R_{1}), R_{3} \to \frac{1}{5}(R_{3} + 2R_{1}) 
&\implies \begin{pmatrix}
1 & 4 & 5 & -9 & -7 \\
0 & 1 & 2 & -3 & -3 \\
0 & 1 & 2 & -3 & -3 \\
0 & -3 & -6 & 4 & 9
\end{pmatrix} \\
R_{3} \to \frac{1}{5}(R_{3} + 3R_{2}) 
&\implies \begin{pmatrix}
1 & 4 & 5 & -9 & -7 \\
0 & 1 & 2 & -3 & -3 \\
0 & 0 & 0 & 1 & 0 \\
0 & 0 & 0 & 0 & 0
\end{pmatrix} \\
R_{2} \to R_{2} + 3 R_{3}, R_{1} \to R_{1} - 4R_{4}, R_{1} \to R_{1} - 3R_{3} 
&\implies \begin{pmatrix}
1 & 0 & -3 & 0 & 5 \\
0 & 1 & 2 & 0 & -3 \\
0 & 0 & 0 & 1 & 0 \\
0 & 0 & 0 & 0 & 0
\end{pmatrix}
\end{align}
$$
