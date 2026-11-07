## Question

### Exercise 10. Detecting Dependence
Without carrying out a full determinant calculation, explain why

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 5 \\
\end{pmatrix}=0.
$$

Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.

> **Why this exercise:** teaches how to recognize a zero determinant from the structure of a matrix.

## Solution

The determinant

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 5 \\
\end{pmatrix}=0
$$

because the second row is twice the first row. The matrix is therefore not invertible.

### Main steps

Denote the matrix by $A$ and its rows by $r_1=(1,\ 2,\ 3)$, $r_2=(2,\ 4,\ 6)$, $r_3=(0,\ 1,\ 5)$.

**1. The dependence between the rows.** Compare $r_2$ with $r_1$:

$$
2\cdot r_1=2\cdot(1,\ 2,\ 3)=(2,\ 4,\ 6)=r_2.
$$

Equivalently,

$$
2r_1-r_2+0\cdot r_3=0.
$$

This is a nontrivial linear relation among the rows (not all coefficients are zero), so the rows are linearly dependent.

**2. Why the determinant vanishes.** Apply the row operation $R_2\leftarrow R_2-2R_1$. It does not change the determinant, and it produces a zero row:

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & 0 \\
0 & 1 & 5 \\
\end{pmatrix}.
$$

A matrix with a zero row has determinant $0$: expanding along that row, every term contains the factor $0$. Hence $\det A=0$.

**3. Connection with non-invertibility.** Suppose $A$ had an inverse $A^{-1}$. Let $y=(2,\ -1,\ 0)$ be the row vector of coefficients from step 1. The relation in step 1 says

$$
yA=2r_1-r_2+0\cdot r_3=(0,\ 0,\ 0).
$$

Multiplying on the right by $A^{-1}$ would give

$$
y=yAA^{-1}=(0,\ 0,\ 0)\cdot A^{-1}=(0,\ 0,\ 0),
$$

which contradicts $y\neq 0$. Therefore $A^{-1}$ does not exist. This is consistent with the criterion that a matrix is invertible if and only if its determinant is nonzero.

### Property / method

If one row of a square matrix is a multiple of another row (more generally, if the rows are linearly dependent), the determinant is zero and the matrix is not invertible. This can be recognized by inspection, without expanding the determinant. The same statement holds for columns.

### Verification

A direct computation by Sarrus' rule, performed only as a check:

$$
\begin{aligned}
&1\cdot 4\cdot 5+2\cdot 6\cdot 0+3\cdot 2\cdot 1=20+0+6=26, \\
&3\cdot 4\cdot 0+1\cdot 6\cdot 1+2\cdot 2\cdot 5=0+6+20=26.
\end{aligned}
$$

The first line is the sum of the positive terms and the second line is the sum of the negative terms. Their difference is $26-26=0$, as expected.
