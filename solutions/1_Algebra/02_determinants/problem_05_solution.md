## Exercise 5. Row Operations

### Result

For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2 \\
\end{pmatrix}
$$

the determinant is

$$
\det A=21.
$$

### Main steps

The goal is to reach an upper triangular matrix using only operations whose effect on the determinant is known.

**Step 1.** $R_2\leftarrow R_2-2R_1$. This adds a multiple of one row to another row, so the determinant is **unchanged**.

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
-1 & 4 & 2 \\
\end{pmatrix}
$$

The new second row is $(2-2,\ 1-4,\ 0-6)=(0,\ -3,\ -6)$.

**Step 2.** $R_3\leftarrow R_3+R_1$. Again a multiple of one row is added to another row, so the determinant is **unchanged**.

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 6 & 5 \\
\end{pmatrix}
$$

The new third row is $(-1+1,\ 4+2,\ 2+3)=(0,\ 6,\ 5)$.

**Step 3.** $R_3\leftarrow R_3+2R_2$. The determinant is **unchanged**.

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 0 & -7 \\
\end{pmatrix}
$$

The new third row is $(0,\ 6+2\cdot(-3),\ 5+2\cdot(-6))=(0,\ 0,\ -7)$.

**Step 4. The determinant of the triangular matrix.** Since all three operations left the determinant unchanged, $\det A$ equals the determinant of the last matrix. It is upper triangular, so

$$
\det A=1\cdot(-3)\cdot(-7)=21.
$$

### Property / method

The effect of elementary row operations on the determinant:

- adding a multiple of one row to another row: the determinant does not change;
- swapping two rows: the determinant is multiplied by $-1$;
- multiplying a row by a number $c$: the determinant is multiplied by $c$.

In this exercise only operations of the first kind were used, so no correction factor is needed.

### Verification

Sarrus' rule for the original matrix:

$$
\begin{aligned}
&1\cdot 1\cdot 2+2\cdot 0\cdot(-1)+3\cdot 2\cdot 4=2+0+24=26, \\
&3\cdot 1\cdot(-1)+1\cdot 0\cdot 4+2\cdot 2\cdot 2=-3+0+8=5.
\end{aligned}
$$

The first line is the sum of the three positive terms and the second line is the sum of the three negative terms. Hence $\det A=26-5=21$, which agrees with the elimination result.
