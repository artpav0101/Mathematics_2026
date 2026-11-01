## Exercise 12. A Parameter Revealed by a Row Operation

### Result

For

$$
A(t)=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & t \\
0 & 1 & 1 \\
\end{pmatrix}
$$

the determinant is $\det A(t)=6-t$. The matrix is not invertible exactly for

$$
t=6.
$$

### Main steps

**1. The row operation $R_2\leftarrow R_2-2R_1$.** It does not change the determinant. The new second row is

$$
(2-2\cdot 1,\ 4-2\cdot 2,\ t-2\cdot 3)=(0,\ 0,\ t-6).
$$

The matrix becomes

$$
A'=
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & t-6 \\
0 & 1 & 1 \\
\end{pmatrix},\qquad \det A'=\det A(t).
$$

**2. Using the structure.** The first column of $A'$ contains only one nonzero entry, the $1$ in position $(1,1)$. Expand along the first column:

$$
\det A'=1\cdot\det
\begin{pmatrix}
0 & t-6 \\
1 & 1 \\
\end{pmatrix}.
$$

**3. The $2\times 2$ determinant.**

$$
\det
\begin{pmatrix}
0 & t-6 \\
1 & 1 \\
\end{pmatrix}=0\cdot 1-(t-6)\cdot 1=-(t-6)=6-t.
$$

Therefore

$$
\det A(t)=6-t.
$$

**4. Values of $t$ for which the matrix is not invertible.** The matrix is not invertible exactly when the determinant is zero:

$$
6-t=0\quad\Longleftrightarrow\quad t=6.
$$

For every $t\neq 6$ the determinant is nonzero and $A(t)$ is invertible.

### What happens to the rows for $t=6$

For $t=6$ the second row of $A'$ is $(0,\ 0,\ 0)$, because $t-6=0$. This means that in the original matrix

$$
R_2-2R_1=0,\qquad R_2=2R_1.
$$

Indeed, for $t=6$ the first two rows of $A(6)$ are $(1,\ 2,\ 3)$ and $(2,\ 4,\ 6)=2\cdot(1,\ 2,\ 3)$. The rows are linearly dependent: the second row is a multiple of the first. A matrix with proportional rows is singular, which agrees with $\det A(6)=0$.

For $t\neq 6$ the third entry of the second row of $A'$ is nonzero, no such dependence exists, and the three rows are linearly independent.

### Property / method

A row operation of the type "add a multiple of one row to another row" preserves the determinant but can expose hidden structure: here a row with two zeros and a single entry depending on $t$, which makes the expansion trivial and shows where the dependence of rows occurs.

### Verification

Direct computation of $\det A(t)$ by Sarrus' rule on the original matrix:

$$
\begin{aligned}
&1\cdot 4\cdot 1+2\cdot t\cdot 0+3\cdot 2\cdot 1=4+0+6=10, \\
&3\cdot 4\cdot 0+1\cdot t\cdot 1+2\cdot 2\cdot 1=0+t+4=t+4.
\end{aligned}
$$

The first line is the sum of the positive terms and the second line is the sum of the negative terms. Hence

$$
\det A(t)=10-(t+4)=6-t,
$$

in agreement with the result above.
