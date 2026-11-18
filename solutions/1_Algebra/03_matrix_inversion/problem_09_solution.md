## Question

### Exercise 9. Matrix Equation
Given

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}.
$$

Solve the equation $AX=B$ for $X$. Before calculating, decide on which side of the equation $A^{-1}$ must be used. Then check the result by computing $AX$.

> **Why this exercise:** teaches that order matters in matrix equations and must guide the solution.

## Solution

For

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad
B=
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}
$$

the solution of $AX=B$ is

$$
X=A^{-1}B=
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix}.
$$

### Main steps

**1. Side on which $A^{-1}$ is used.** In the equation $AX=B$ the matrix $A$ stands on the **left** of the unknown $X$. To remove it, multiply both sides by $A^{-1}$ from the **left**, so that $A^{-1}$ meets $A$:

$$
A^{-1}(AX)=A^{-1}B\quad\Longrightarrow\quad (A^{-1}A)X=A^{-1}B\quad\Longrightarrow\quad X=A^{-1}B.
$$

Multiplication from the right would produce $AXA^{-1}=BA^{-1}$, where the factor $A^{-1}$ is separated from $A$ by $X$ and does not cancel.

**2. The inverse of $A$.** Here $\det A=1\cdot 1-2\cdot 0=1$, so

$$
A^{-1}=
\begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}.
$$

**3. The product $A^{-1}B$.**

$$
X=
\begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot 3+(-2)\cdot 2 & 1\cdot 1+(-2)\cdot 4 \\
0\cdot 3+1\cdot 2 & 0\cdot 1+1\cdot 4 \\
\end{pmatrix}=
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix}.
$$

### Property / method

Matrix multiplication is not commutative, so in a matrix equation the inverse must be applied on the same side where the known matrix stands:

- $AX=B$ gives $X=A^{-1}B$;
- $XA=B$ gives $X=BA^{-1}$.

### Verification

Compute $AX$:

$$
AX=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot(-1)+2\cdot 2 & 1\cdot(-7)+2\cdot 4 \\
0\cdot(-1)+1\cdot 2 & 0\cdot(-7)+1\cdot 4 \\
\end{pmatrix}=
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}=B.
$$

The equation holds. The wrong side would give a different matrix:

$$
BA^{-1}=
\begin{pmatrix}
3 & -5 \\
2 & 0 \\
\end{pmatrix}\neq X,
$$

and it does not satisfy $AX=B$.
