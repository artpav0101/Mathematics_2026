## Exercise 2. Determinant of a 3×3 Matrix

### Result

For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5 \\
\end{pmatrix}
$$

the determinant is

$$
\det A=33.
$$

### Main steps

**1. Sarrus' rule.** For a $3\times3$ matrix with entries $a_{ij}$,

$$
\begin{aligned}
\det A &= a_{11}a_{22}a_{33}+a_{12}a_{23}a_{31}+a_{13}a_{21}a_{32} \\
       &\quad -a_{13}a_{22}a_{31}-a_{11}a_{23}a_{32}-a_{12}a_{21}a_{33}.
\end{aligned}
$$

The first three products follow the main diagonal and its two "wrapped" parallels. The last three products follow the anti-diagonal and its two "wrapped" parallels.

**2. Positive terms.**

$$
\begin{aligned}
a_{11}a_{22}a_{33} &= 1\cdot 3\cdot 5 = 15, \\
a_{12}a_{23}a_{31} &= 2\cdot 4\cdot 2 = 16, \\
a_{13}a_{21}a_{32} &= (-1)\cdot 0\cdot 1 = 0.
\end{aligned}
$$

Their sum is $15+16+0=31$.

**3. Negative terms.**

$$
\begin{aligned}
a_{13}a_{22}a_{31} &= (-1)\cdot 3\cdot 2 = -6, \\
a_{11}a_{23}a_{32} &= 1\cdot 4\cdot 1 = 4, \\
a_{12}a_{21}a_{33} &= 2\cdot 0\cdot 5 = 0.
\end{aligned}
$$

Their sum is $-6+4+0=-2$.

**4. The determinant.**

$$
\det A=31-(-2)=33.
$$

### Property / method

Sarrus' rule is valid only for $3\times 3$ matrices. It is the full expansion of the determinant into $3!=6$ signed products, three with sign $+$ and three with sign $-$.

### Verification

**Check by a determinant property.** Adding a multiple of one row to another row does not change the determinant, and the determinant of a triangular matrix is the product of its diagonal entries.

Apply $R_3\leftarrow R_3-2R_1$:

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
0 & -3 & 7 \\
\end{pmatrix}.
$$

Apply $R_3\leftarrow R_3+R_2$:

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
0 & 0 & 11 \\
\end{pmatrix}.
$$

Both operations leave the determinant unchanged, and the last matrix is upper triangular. Hence

$$
\det A=1\cdot 3\cdot 11=33.
$$

The two methods agree.
