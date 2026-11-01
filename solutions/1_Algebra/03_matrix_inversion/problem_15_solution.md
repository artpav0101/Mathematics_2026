## Exercise 15. Two Methods for Solving the Same System

### Result

For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix},\qquad
b=
\begin{pmatrix}
7 \\
8 \\
\end{pmatrix}
$$

both methods give the same solution of $Ax=b$:

$$
x=
\begin{pmatrix}
\frac{13}{5} \\
\frac95 \\
\end{pmatrix}.
$$

### Main steps

**Method 1. Using $A^{-1}b$.**

The determinant is $\det A=2\cdot 3-1\cdot 1=5\neq 0$, so the inverse exists:

$$
A^{-1}=\frac15
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}.
$$

Then

$$
x=A^{-1}b=\frac15
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
7 \\
8 \\
\end{pmatrix}=\frac15
\begin{pmatrix}
3\cdot 7-1\cdot 8 \\
-1\cdot 7+2\cdot 8 \\
\end{pmatrix}=\frac15
\begin{pmatrix}
13 \\
9 \\
\end{pmatrix}=
\begin{pmatrix}
\frac{13}{5} \\
\frac95 \\
\end{pmatrix}.
$$

**Method 2. Gaussian elimination.**

Write the augmented matrix $[A\mid b]$:

$$
\begin{pmatrix}
2 & 1 & \mid & 7 \\
1 & 3 & \mid & 8 \\
\end{pmatrix}
$$

Swap the rows, $R_1\leftrightarrow R_2$, to obtain a pivot equal to $1$ and avoid fractions:

$$
\begin{pmatrix}
1 & 3 & \mid & 8 \\
2 & 1 & \mid & 7 \\
\end{pmatrix}
$$

Apply $R_2\leftarrow R_2-2R_1$. The new second row is $(2-2,\ 1-6\mid 7-16)=(0,\ -5\mid -9)$:

$$
\begin{pmatrix}
1 & 3 & \mid & 8 \\
0 & -5 & \mid & -9 \\
\end{pmatrix}
$$

The second row says $-5x_2=-9$, so

$$
x_2=\frac95.
$$

Back substitution into the first row $x_1+3x_2=8$ gives

$$
x_1=8-3\cdot\frac95=8-\frac{27}{5}=\frac{40}{5}-\frac{27}{5}=\frac{13}{5}.
$$

Therefore $x=\left(\frac{13}{5},\ \frac95\right)^T$.

### Comparison of the methods

Both methods give the same vector $x=\left(\frac{13}{5},\ \frac95\right)^T$.

- **Method 1 ($A^{-1}b$).** Essential steps: compute the determinant, build $A^{-1}$ (swap two entries, negate two entries, divide by $\det A$), multiply the matrix by the vector (four multiplications and two additions), and divide by $5$.
- **Method 2 (elimination).** Essential steps: one row swap, one row operation (two multiplications), and a short back substitution for two unknowns.

In this example, Gaussian elimination is shorter and simpler: it solves the system directly and never builds a matrix that is not needed afterwards. The inverse-matrix method has a different advantage. Once $A^{-1}$ is known, any other right-hand side $b$ requires only one matrix–vector product. It is therefore convenient when the same matrix $A$ is used with many different vectors $b$, and it gives a convenient formula $x=A^{-1}b$ for theoretical arguments. For a single system, elimination is the better choice, especially for matrices larger than $2\times 2$.

### Property / method

Both methods rely on the same fact: $A$ is invertible ($\det A\neq 0$), so the system $Ax=b$ has exactly one solution. Elimination finds it directly, and the inverse method finds it through the intermediate object $A^{-1}$.

### Verification

Substitute $x=\left(\frac{13}{5},\ \frac95\right)^T$ into $Ax$:

$$
Ax=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
\frac{13}{5} \\
\frac95 \\
\end{pmatrix}=
\begin{pmatrix}
\frac{26}{5}+\frac95 \\
\frac{13}{5}+\frac{27}{5} \\
\end{pmatrix}=
\begin{pmatrix}
\frac{35}{5} \\
\frac{40}{5} \\
\end{pmatrix}=
\begin{pmatrix}
7 \\
8 \\
\end{pmatrix}=b.
$$

The equation is satisfied.
