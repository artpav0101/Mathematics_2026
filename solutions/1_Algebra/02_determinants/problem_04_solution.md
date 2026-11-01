## Exercise 4. Triangular Matrix

### Result

$$
\det
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}=2\cdot(-3)\cdot 7=-42.
$$

### Main steps

**1. The matrix is upper triangular.** All entries below the main diagonal are zero. The diagonal entries are $2$, $-3$, $7$.

**2. The rule.** The determinant of any triangular matrix (upper triangular, lower triangular, or diagonal) equals the product of its diagonal entries:

$$
\det T=t_{11}t_{22}\cdots t_{nn}.
$$

**3. Applying the rule.**

$$
\det
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}=2\cdot(-3)\cdot 7=-42.
$$

**4. Why the rule works in this example.** Expand the determinant along the first column. The entries $0$ and $0$ in positions $(2,1)$ and $(3,1)$ contribute nothing, so only the entry $2$ remains:

$$
\det T=2\cdot\det
\begin{pmatrix}
-3 & 5 \\
0 & 7 \\
\end{pmatrix}.
$$

The remaining $2\times2$ matrix is again upper triangular. Expanding it along its first column leaves only $-3$:

$$
\det
\begin{pmatrix}
-3 & 5 \\
0 & 7 \\
\end{pmatrix}=(-3)\cdot 7-5\cdot 0=-21.
$$

Hence

$$
\det T=2\cdot(-21)=-42.
$$

### Property / method

For an upper triangular $n\times n$ matrix, expansion along the first column leaves only $t_{11}$ times the determinant of the $(n-1)\times(n-1)$ upper triangular submatrix obtained by deleting row $1$ and column $1$. Repeating the argument (induction on $n$) gives the product of all diagonal entries. For a lower triangular matrix, expand along the first row instead, or use $\det T^T=\det T$, since $T^T$ is upper triangular with the same diagonal.

This rule is the reason why Gaussian elimination is an efficient way to compute determinants: reduce the matrix to triangular form while keeping track of the operations, then multiply the diagonal.

### Verification

Sarrus' rule applied to the same matrix gives, for the three positive terms,

$$
2\cdot(-3)\cdot 7+4\cdot 5\cdot 0+1\cdot 0\cdot 0=-42,
$$

and for the three negative terms,

$$
1\cdot(-3)\cdot 0+2\cdot 5\cdot 0+4\cdot 0\cdot 7=0.
$$

So $\det T=-42-0=-42$, as before.
