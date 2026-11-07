## Question 

### Exercise 1. Determinant of a 2×2 Matrix
Compute

$$
\det
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix},\qquad \det
\begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix}.
$$

Which matrix is invertible? Justify your answer.

> **Why this exercise:** introduces the simplest determinant calculation and immediately connects it with invertibility.

## Solution

Let

$$
A=
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix},\qquad
B=
\begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix}.
$$

Then

$$
\det A=22,\qquad \det B=0.
$$

The matrix $A$ is invertible. The matrix $B$ is not invertible.

### Main steps

**1. The formula.** For a $2\times2$ matrix

$$
\det
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}=ad-bc.
$$

**2. The matrix $A$.** Here $a=3$, $b=-2$, $c=5$, $d=4$, so

$$
\begin{aligned}
\det A &= 3\cdot 4-(-2)\cdot 5 \\
       &= 12+10 \\
       &= 22.
\end{aligned}
$$

**3. The matrix $B$.** Here $a=1$, $b=7$, $c=2$, $d=14$, so

$$
\begin{aligned}
\det B &= 1\cdot 14-7\cdot 2 \\
       &= 14-14 \\
       &= 0.
\end{aligned}
$$

**4. Which matrix is invertible.**

**The matrix $A$.** Since $\det A=22\neq 0$, the matrix is invertible. By the $2\times2$ inverse formula,

$$
A^{-1}=\frac{1}{22}
\begin{pmatrix}
4 & 2 \\
-5 & 3 \\
\end{pmatrix}.
$$

**The matrix $B$.** Since $\det B=0$, the matrix is not invertible. This can also be seen directly: the second row of $B$ is twice the first row. For every $2\times2$ matrix $X$, each row of $BX$ is a combination of the rows of $X$ with the coefficients taken from the corresponding row of $B$. Hence the second row of $BX$ is always twice the first row of $BX$. The identity matrix does not have this property, because its first row is $(1,\ 0)$ and its second row is $(0,\ 1)\neq 2\cdot(1,\ 0)$. Therefore the equation $BX=I$ has no solution, and $B^{-1}$ does not exist.

### Property / method

A square matrix is invertible if and only if its determinant is nonzero. For a $2\times 2$ matrix the determinant $ad-bc$ is zero exactly when the rows $(a,\ b)$ and $(c,\ d)$ are proportional, that is, when one row is a multiple of the other. Proportional rows make the matrix singular.

### Verification

For $A$, multiply by the matrix from the inverse formula:

$$
A
\begin{pmatrix}
4 & 2 \\
-5 & 3 \\
\end{pmatrix}=
\begin{pmatrix}
3\cdot 4+(-2)\cdot(-5) & 3\cdot 2+(-2)\cdot 3 \\
5\cdot 4+4\cdot(-5) & 5\cdot 2+4\cdot 3 \\
\end{pmatrix}=
\begin{pmatrix}
22 & 0 \\
0 & 22 \\
\end{pmatrix}=22I.
$$

Dividing by $22$ gives $A\cdot A^{-1}=I$, which confirms both $\det A\neq 0$ and the form of $A^{-1}$.

For $B$, the second row equals $2$ times the first row: $(2,\ 14)=2\cdot(1,\ 7)$. This confirms $\det B=0$.
