**Invariants**: values that don't change.

**Monovariants**: values that change monotonically.

# Example 1

If you remove the diagonal corners of a 8x8 chess grid, can you fill it in with 31 2x1 dominoes?

### Proof

No, you can't.

Think about the number of black and white cells in the grid. Since you remove the diagonal corners, which are the same color, there are either 32 black and 30 white cells or vice versa. Notice that each domino must cover exactly 1 black and 1 white cell. Therefore, it's not possible.

# Example 2

Determine all $m,n\geq 2$ such that the $m\times n$ grid can be tiled by L tetrominoes. Rotations and reflections are allowed

### Proof

We can label the necessary, sufficient and impossible combinations.

**Necessary**

$4|mn$ because there are 4 blocks per L

**Sufficient**

The smallest rectangle you can make is $4\times 2$. Therefore, you can make any grid of form $2x \times 4y$ or $4x \times 2y$.

We can once again use coloring. If you alternate coloring each column black and white, notice that each L must cover 1 white and 3 black or 3 white and 1 black. 

Assume that $m$ is even. Then, there is always an even number of white and even number of black. Thus, there must be an even number of L's. Thus, $8|mn$. 

Work on showing necessary and sufficient

# Example 3

(IMO 193, extended)

Board game exists where in an infinite grid, $m \times n$  rectangle of soldiers can jump over adjacent soldiers into empty cell and kill them. How many $m,n$ exist such that game can end with exactly 1 soldier left?

### Proof

Just by trying out, we know that $2\times 2$ works, $2\times 3$ works, and $2\times 4$ works. From these 3 tries, we get some tricks:

- $2\times 2$ works unconditionally
- $2\times 4$ can reduce to $2\times {1}$ , effectively meaning we can do $2\times 3$ when we have $2\times 4$.

There is a third trick: we can reduce L-tetraminoes to a bottom corner (try it out), meaning we can reduce any $3\times n$  to $3\times n-1$.

Based on some more trying, we can show that it works as long as $3 \nmid mn$. 

We then use induction to show that $m\times n$ works $\implies$ $m+3 \times n$ is possible using the L-tetraminoe rule. We have our base cases of $(2,2), (2,4), (4,2), (4,4)$ to show that any $3\nmid n$ works. Thus, $3 \nmid mn\implies$ possible (sufficient).

Now, we must prove $3|mn\implies$ impossible. For this we use coloring. 

Color every third cell black. Then, we can perform casework to show that by killing a soldier, you always reduce the number of soldiers on white cells by an even number, and the number of soldiers on black cells by an odd number.

Now, WLOG assume $3|m$. Then, we must have $\frac{2mn}{3}$ white soldiers and $\frac{mn}{3}$ black soldiers. Since the number of white starts off as even, the last soldier cant be on white. Thus, it must be on black.

Now, shift the coloring 1 block left or right. The same conditions must hold true from earlier: last soldier must be on black. However, there are no overlapping black squares. Therefore, it's impossible.

# Example 4

# Example 5

Kontsevich's game.



