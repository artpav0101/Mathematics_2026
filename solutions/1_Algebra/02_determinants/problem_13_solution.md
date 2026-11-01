## Exercise 13. Determinant by Elimination

### Result

For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 5 & 7 \\
1 & 0 & 2 \\
\end{pmatrix}
$$

the determinant is

$$
\det A=1.
$$

### Main steps

The elimination clears the entries below the pivots column by column. The effect of every operation on the determinant is recorded.

**Step 1.** $R_2\leftarrow R_2-2R_1$.

Effect on the determinant: none (adding a multiple of another row). The new second row is $(2-2,\ 5-4,\ 7-6)=(0,\ 1,\ 1)$.

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
1 & 0 & 2 \\
\end{pmatrix}
$$

**Step 2.** $R_3\leftarrow R_3-R_1$.

Effect on the determinant: none. The new third row is $(1-1,\ 0-2,\ 2-3)=(0,\ -2,\ -1)$.

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & -2 & -1 \\
\end{pmatrix}
$$

**Step 3.** $R_3\leftarrow R_3+2R_2$.

Effect on the determinant: none. The new third row is $(0,\ -2+2,\ -1+2)=(0,\ 0,\ 1)$.

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1 \\
\end{pmatrix}
$$

**Step 4. The determinant.** All three operations were of the type "add a multiple of one row to another row", so the determinant was never changed, and the correction factor is $1$. The final matrix is upper triangular:

$$
\det A=1\cdot 1\cdot 1=1.
$$

### Summary of the operations

- $R_2\leftarrow R_2-2R_1$: the determinant is unchanged (factor $1$).
- $R_3\leftarrow R_3-R_1$: the determinant is unchanged (factor $1$).
- $R_3\leftarrow R_3+2R_2$: the determinant is unchanged (factor $1$).

The total correction factor is $1\cdot 1\cdot 1=1$, so $\det A$ equals the product of the diagonal entries of the triangular matrix.

### Property / method

When a matrix is reduced to triangular form, the determinant of the original matrix equals the product of the diagonal entries divided by the product of all factors by which the operations changed the determinant (a swap contributes $-1$, scaling a row by $c$ contributes $c$). Here all factors equal $1$.

### Verification

Sarrus' rule for the original matrix:

$$
\begin{aligned}
&1\cdot 5\cdot 2+2\cdot 7\cdot 1+3\cdot 2\cdot 0=10+14+0=24, \\
&3\cdot 5\cdot 1+1\cdot 7\cdot 0+2\cdot 2\cdot 2=15+0+8=23.
\end{aligned}
$$

The first line is the sum of the positive terms and the second line is the sum of the negative terms. Hence $\det A=24-23=1$, in agreement with the elimination.
