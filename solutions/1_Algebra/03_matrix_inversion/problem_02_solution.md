## Exercise 2. Formula for a 2×2 Matrix

### Result

For

$$
A=
\begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix}
$$

the inverse is

$$
A^{-1}=\frac12
\begin{pmatrix}
4 & -2 \\
-5 & 3 \\
\end{pmatrix}=
\begin{pmatrix}
2 & -1 \\
-\frac52 & \frac32 \\
\end{pmatrix}.
$$

### Main steps

**1. The formula.** For

$$
A=
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}
$$

with $\det A=ad-bc\neq 0$,

$$
A^{-1}=\frac{1}{ad-bc}
\begin{pmatrix}
d & -b \\
-c & a \\
\end{pmatrix}.
$$

The diagonal entries are swapped, and the off-diagonal entries change sign.

**2. The determinant.** Here $a=3$, $b=2$, $c=5$, $d=4$:

$$
\det A=3\cdot 4-2\cdot 5=12-10=2.
$$

Since $\det A=2\neq 0$, the inverse exists.

**3. Substitution into the formula.**

$$
A^{-1}=\frac12
\begin{pmatrix}
4 & -2 \\
-5 & 3 \\
\end{pmatrix}=
\begin{pmatrix}
2 & -1 \\
-\frac52 & \frac32 \\
\end{pmatrix}.
$$

### Property / method

The formula comes from the adjugate: $A^{-1}=\frac{1}{\det A}\,\mathrm{adj}(A)$. For a $2\times 2$ matrix the adjugate is obtained by swapping the diagonal entries and negating the off-diagonal entries. If $\det A=0$ the formula breaks down (division by zero), and no inverse exists.

### Verification

Compute the product $AA^{-1}$, using the unscaled matrix and the factor $\frac12$ separately:

$$
A\begin{pmatrix}
4 & -2 \\
-5 & 3 \\
\end{pmatrix}=
\begin{pmatrix}
3\cdot 4+2\cdot(-5) & 3\cdot(-2)+2\cdot 3 \\
5\cdot 4+4\cdot(-5) & 5\cdot(-2)+4\cdot 3 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 0 \\
0 & 2 \\
\end{pmatrix}.
$$

Multiplying by the factor $\frac12$ gives

$$
AA^{-1}=\frac12
\begin{pmatrix}
2 & 0 \\
0 & 2 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}=I.
$$

The product is the identity matrix, so $A^{-1}$ is correct.
