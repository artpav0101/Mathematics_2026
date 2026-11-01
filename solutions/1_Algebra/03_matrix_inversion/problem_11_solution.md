## Exercise 11. Parameter and Invertibility

### Result

For

$$
A(t)=
\begin{pmatrix}
1 & t \\
t & 1 \\
\end{pmatrix}
$$

the matrix is invertible if and only if $t\neq 1$ and $t\neq -1$. For these $t$,

$$
A(t)^{-1}=\frac{1}{1-t^2}
\begin{pmatrix}
1 & -t \\
-t & 1 \\
\end{pmatrix}.
$$

### Main steps

**1. The determinant.**

$$
\det A(t)=1\cdot 1-t\cdot t=1-t^2=(1-t)(1+t).
$$

**2. Condition for invertibility.** The matrix is invertible if and only if $\det A(t)\neq 0$:

$$
(1-t)(1+t)\neq 0\quad\Longleftrightarrow\quad t\neq 1\ \ \mathrm{and}\ \ t\neq -1.
$$

**3. The inverse.** By the $2\times 2$ formula with $a=1$, $b=t$, $c=t$, $d=1$,

$$
A(t)^{-1}=\frac{1}{1-t^2}
\begin{pmatrix}
1 & -t \\
-t & 1 \\
\end{pmatrix}.
$$

**4. What happens at the excluded values.** At $t=\pm 1$ the denominator $1-t^2$ equals $0$, and the formula is meaningless. The matrices are

$$
A(1)=
\begin{pmatrix}
1 & 1 \\
1 & 1 \\
\end{pmatrix},\qquad
A(-1)=
\begin{pmatrix}
1 & -1 \\
-1 & 1 \\
\end{pmatrix}.
$$

In the first matrix the two rows are equal. In the second matrix the second row is $-1$ times the first row. In both cases the rows are linearly dependent, the determinant is $0$, and the inverse does not exist.

Moreover, as $t$ approaches $\pm 1$ the entries of the formula, such as $\frac{1}{1-t^2}$, grow without bound. The inverse does not stay bounded and has no limit: no choice of finite entries can repair the formula at $t=\pm 1$.

### Property / method

A family of matrices depending on a parameter is invertible exactly outside the roots of its determinant. The inverse formula $A^{-1}=\frac{1}{\det A}\mathrm{adj}(A)$ has the determinant in the denominator, which is why the roots of $\det A(t)$ are precisely the excluded values.

### Verification

Multiply $A(t)$ by the formula for $t\neq\pm 1$:

$$
A(t)
\begin{pmatrix}
1 & -t \\
-t & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot 1+t\cdot(-t) & 1\cdot(-t)+t\cdot 1 \\
t\cdot 1+1\cdot(-t) & t\cdot(-t)+1\cdot 1 \\
\end{pmatrix}=
\begin{pmatrix}
1-t^2 & 0 \\
0 & 1-t^2 \\
\end{pmatrix}.
$$

Dividing by $1-t^2$ gives the identity matrix, so the formula is correct. For example, $t=2$ gives $\det A(2)=-3$ and

$$
A(2)^{-1}=-\frac13
\begin{pmatrix}
1 & -2 \\
-2 & 1 \\
\end{pmatrix}.
$$
