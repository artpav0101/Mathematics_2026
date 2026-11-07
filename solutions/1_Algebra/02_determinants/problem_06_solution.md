## Question

### Exercise 6. Parameter and Invertibility
For

$$
A(t)=
\begin{pmatrix}
t & 1 \\
2 & t \\
\end{pmatrix}
$$

find all values of $t$ for which the matrix is not invertible. Explain how your answer is related to the determinant being zero.

> **Why this exercise:** shows how the determinant can be used to study a family of matrices depending on a parameter.

### Exercise 7. Using Properties Instead of Recomputing
Suppose that for a $3\times3$ matrix, $\det A=-4$. Compute

$$
\det(2A),\qquad \det(A^T),\qquad \det(A^2),\qquad \det(-A).
$$

Justify each answer using the appropriate property.

> **Why this exercise:** teaches how to use determinant properties instead of repeating a full calculation.

## Solution

For

$$
A(t)=
\begin{pmatrix}
t & 1 \\
2 & t \\
\end{pmatrix}
$$

the determinant is $\det A(t)=t^2-2$. The matrix is not invertible exactly for

$$
t=\sqrt2\qquad\mathrm{and}\qquad t=-\sqrt2.
$$

### Main steps

**1. The determinant as a function of $t$.**

$$
\det A(t)=t\cdot t-1\cdot 2=t^2-2.
$$

**2. The condition for non-invertibility.** A square matrix is not invertible exactly when its determinant is zero:

$$
t^2-2=0.
$$

**3. Solving the equation.**

$$
t^2=2\quad\Longrightarrow\quad t=\sqrt2\quad\mathrm{or}\quad t=-\sqrt2.
$$

**4. Conclusion.** For $t=\pm\sqrt2$ the matrix $A(t)$ is not invertible. For every other real $t$ we have $t^2-2\neq 0$, and $A(t)$ is invertible.

### Property / method

The determinant criterion: $A$ is invertible if and only if $\det A\neq 0$. When a matrix depends on a parameter, $\det A(t)$ is a polynomial in $t$, and its roots are precisely the exceptional parameter values for which the matrix is singular.

The relation to dependence of rows is visible at the exceptional values.

For $t=\sqrt2$:

$$
A(\sqrt2)=
\begin{pmatrix}
\sqrt2 & 1 \\
2 & \sqrt2 \\
\end{pmatrix},\qquad
\sqrt2\cdot(\sqrt2,\ 1)=(2,\ \sqrt2).
$$

The second row is $\sqrt2$ times the first row.

For $t=-\sqrt2$:

$$
A(-\sqrt2)=
\begin{pmatrix}
-\sqrt2 & 1 \\
2 & -\sqrt2 \\
\end{pmatrix},\qquad
(-\sqrt2)\cdot(-\sqrt2,\ 1)=(2,\ -\sqrt2).
$$

The second row is $-\sqrt2$ times the first row.

In both cases the rows are proportional, which is exactly what $\det A(t)=0$ expresses.

### Verification

Substituting the roots into the determinant:

$$
(\sqrt2)^2-2=2-2=0,\qquad (-\sqrt2)^2-2=2-2=0.
$$

For a value outside the roots, for example $t=0$, the matrix is

$$
A(0)=
\begin{pmatrix}
0 & 1 \\
2 & 0 \\
\end{pmatrix}
$$

with determinant $0\cdot 0-1\cdot 2=-2\neq 0$, so it is invertible, as the criterion predicts.
