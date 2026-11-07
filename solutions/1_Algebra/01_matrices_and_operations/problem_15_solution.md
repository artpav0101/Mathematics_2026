## Question

### Exercise 15. Associativity of Multiplication and Different Calculation Paths
Given

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\quad B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix},\quad C=
\begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix}.
$$

Compute $(AB)C$ and $A(BC)$. Compare the results and the number of intermediate operations. Explain what associativity of matrix multiplication means in this example.

> **Why this exercise:** reinforces associativity by comparing two mathematically equivalent calculation paths.

## Solution

For

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\qquad
B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix},\qquad
C=
\begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix}
$$

both calculation paths give the same matrix:

$$
(AB)C=A(BC)=
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}.
$$

The path $(AB)C$ needs $20$ multiplications of numbers, and the path $A(BC)$ needs $24$.

### Main steps

**Sizes.** $A$ is $2\times 3$, $B$ is $3\times 2$, $C$ is $2\times 2$. All products below are defined, because the number of columns of each left factor equals the number of rows of the right factor.

**Path 1. $(AB)C$.**

First compute $AB$, which has size $2\times 2$:

$$
AB=
\begin{pmatrix}
1\cdot 1+2\cdot 2+0\cdot(-1) & 1\cdot 0+2\cdot 1+0\cdot 3 \\
0\cdot 1+1\cdot 2+1\cdot(-1) & 0\cdot 0+1\cdot 1+1\cdot 3 \\
\end{pmatrix}=
\begin{pmatrix}
5 & 2 \\
1 & 4 \\
\end{pmatrix}.
$$

Then multiply by $C$:

$$
(AB)C=
\begin{pmatrix}
5 & 2 \\
1 & 4 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix}=
\begin{pmatrix}
5\cdot 2+2\cdot 0 & 5\cdot 1+2\cdot(-1) \\
1\cdot 2+4\cdot 0 & 1\cdot 1+4\cdot(-1) \\
\end{pmatrix}=
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}.
$$

**Path 2. $A(BC)$.**

First compute $BC$, which has size $3\times 2$:

$$
BC=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot 2+0\cdot 0 & 1\cdot 1+0\cdot(-1) \\
2\cdot 2+1\cdot 0 & 2\cdot 1+1\cdot(-1) \\
(-1)\cdot 2+3\cdot 0 & (-1)\cdot 1+3\cdot(-1) \\
\end{pmatrix}=
\begin{pmatrix}
2 & 1 \\
4 & 1 \\
-2 & -4 \\
\end{pmatrix}.
$$

Then multiply $A$ by $BC$:

$$
A(BC)=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
4 & 1 \\
-2 & -4 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot 2+2\cdot 4+0\cdot(-2) & 1\cdot 1+2\cdot 1+0\cdot(-4) \\
0\cdot 2+1\cdot 4+1\cdot(-2) & 0\cdot 1+1\cdot 1+1\cdot(-4) \\
\end{pmatrix}=
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}.
$$

**Comparison of the results.** The matrices are identical:

$$
(AB)C=A(BC)=
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}.
$$

**Comparison of the number of operations.** The product of an $m\times n$ matrix by an $n\times p$ matrix has $mp$ entries, and each entry needs $n$ multiplications and $n-1$ additions. Hence the product needs $mnp$ multiplications.

- $AB$ ($2\times 3$ by $3\times 2$): $2\cdot 3\cdot 2=12$ multiplications, $4\cdot 2=8$ additions.
- $(AB)C$ ($2\times 2$ by $2\times 2$): $2\cdot 2\cdot 2=8$ multiplications, $4\cdot 1=4$ additions.
- Path 1 in total: $12+8=20$ multiplications and $8+4=12$ additions.
- $BC$ ($3\times 2$ by $2\times 2$): $3\cdot 2\cdot 2=12$ multiplications, $6\cdot 1=6$ additions.
- $A(BC)$ ($2\times 3$ by $3\times 2$): $2\cdot 3\cdot 2=12$ multiplications, $4\cdot 2=8$ additions.
- Path 2 in total: $12+12=24$ multiplications and $6+8=14$ additions.

The counts treat every product of two numbers as an operation, including products with zero. Both paths lead to the same matrix, but the path $(AB)C$ is cheaper: $20$ against $24$ multiplications. The reason is that $AB$ has the small size $2\times 2$, whereas $BC$ has the larger size $3\times 2$ and carries more entries into the next product.

### What associativity means here

Matrix multiplication is associative:

$$
(AB)C=A(BC).
$$

The parentheses only describe in which order the two multiplications are carried out. They do not change the result. This is why the product of three (or more) matrices can be written without parentheses, simply as $ABC$.

Associativity does not allow the **order of the factors** to be changed: in general $AB\neq BA$, and here $BA$ is even a different size ($3\times 3$). Only the **grouping** is free.

In this example the matrices describe maps. The matrix $C$ maps a plane vector to a plane vector, $B$ maps a plane vector to a vector in space, and $A$ maps a vector in space back to the plane. The product $ABC$ is the map "first $C$, then $B$, then $A$". Associativity says that it makes no difference whether we first combine $A$ and $B$ into one map $AB$ and then apply $C$ first (path 1), or first combine $B$ and $C$ into one map $BC$ and then apply it before $A$ (path 2). Composition of maps is associative, and matrix multiplication reproduces this.

### Property / method

Associativity, $(XY)Z=X(YZ)$, holds whenever the sizes make the products defined. It is a property of the definition of the matrix product, and it is different from commutativity, which fails in general. The freedom of grouping has a practical use: the grouping can be chosen to minimize the number of operations, as the comparison $20$ versus $24$ shows.

### Verification

Apply both results to the vector $x=(1,\ 1)^T$ and compare with step-by-step action of the three matrices:

$$
Cx=
\begin{pmatrix}
2\cdot 1+1\cdot 1 \\
0\cdot 1+(-1)\cdot 1 \\
\end{pmatrix}=
\begin{pmatrix}
3 \\
-1 \\
\end{pmatrix},\qquad
B(Cx)=
\begin{pmatrix}
1\cdot 3+0\cdot(-1) \\
2\cdot 3+1\cdot(-1) \\
(-1)\cdot 3+3\cdot(-1) \\
\end{pmatrix}=
\begin{pmatrix}
3 \\
5 \\
-6 \\
\end{pmatrix}.
$$

$$
A\bigl(B(Cx)\bigr)=
\begin{pmatrix}
1\cdot 3+2\cdot 5+0\cdot(-6) \\
0\cdot 3+1\cdot 5+1\cdot(-6) \\
\end{pmatrix}=
\begin{pmatrix}
13 \\
-1 \\
\end{pmatrix}.
$$

The matrix obtained above gives the same vector:

$$
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
1 \\
\end{pmatrix}=
\begin{pmatrix}
13 \\
-1 \\
\end{pmatrix}.
$$
