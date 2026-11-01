## Exercise 11. Shortening the Calculation with Row Operations

### Result

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}=1.
$$

### Main steps

Denote the matrix by $A$. The first column already has a leading entry $1$ in the first row. Use it to create zeros below it, and then use the new second row to create a zero in the third row.

**Step 1.** $R_2\leftarrow R_2-R_1$. The determinant is **unchanged**.

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
1 & 4 & 6 \\
\end{pmatrix}
$$

**Step 2.** $R_3\leftarrow R_3-R_1$. The determinant is **unchanged**.

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 2 & 3 \\
\end{pmatrix}
$$

**Step 3.** $R_3\leftarrow R_3-2R_2$. The determinant is **unchanged**.

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1 \\
\end{pmatrix}
$$

**Step 4.** The final matrix is upper triangular, so its determinant is the product of the diagonal entries:

$$
\det A=1\cdot 1\cdot 1=1.
$$

### Which operations do not change the determinant

All three operations used have the form "add a multiple of one row to another row":

$$
R_i\leftarrow R_i+cR_j,\qquad i\neq j.
$$

Such operations do not change the determinant. Therefore no correction factor appears, and the determinant of the original matrix equals the determinant of the triangular matrix. For comparison, the other two types of elementary operations do change it: a row swap multiplies the determinant by $-1$, and multiplying a row by $c$ multiplies it by $c$.

### Property / method

Planning the operations in advance (work column by column, clear the entries below each pivot) produces a triangular matrix in as few steps as possible. Choosing only operations of the type "add a multiple" keeps the bookkeeping trivial.

### Verification

Sarrus' rule for the original matrix:

$$
\begin{aligned}
&1\cdot 3\cdot 6+2\cdot 4\cdot 1+3\cdot 1\cdot 4=18+8+12=38, \\
&3\cdot 3\cdot 1+1\cdot 4\cdot 4+2\cdot 1\cdot 6=9+16+12=37.
\end{aligned}
$$

The first line is the sum of the positive terms and the second line is the sum of the negative terms. Hence $\det A=38-37=1$, which agrees with the result of the elimination.
