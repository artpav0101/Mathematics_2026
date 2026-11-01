## Exercise 12. Finding Inverses Without Starting from Scratch

### Result

Given

$$
A^{-1}=
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix},
$$

the required inverses are

$$
(3A)^{-1}=
\begin{pmatrix}
\frac23 & -\frac13 \\
-1 & \frac23 \\
\end{pmatrix},\qquad
(A^T)^{-1}=
\begin{pmatrix}
2 & -3 \\
-1 & 2 \\
\end{pmatrix},\qquad
(A^2)^{-1}=
\begin{pmatrix}
7 & -4 \\
-12 & 7 \\
\end{pmatrix}.
$$

### Main steps

**1. The inverse of $3A$.** For a number $c\neq 0$ and an invertible $A$,

$$
(cA)^{-1}=\frac1cA^{-1}.
$$

Justification: $(cA)\left(\frac1cA^{-1}\right)=\left(c\cdot\frac1c\right)AA^{-1}=I$. With $c=3$,

$$
(3A)^{-1}=\frac13
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}=
\begin{pmatrix}
\frac23 & -\frac13 \\
-1 & \frac23 \\
\end{pmatrix}.
$$

**2. The inverse of $A^T$.** For an invertible $A$,

$$
(A^T)^{-1}=(A^{-1})^T.
$$

Justification: using $(XY)^T=Y^TX^T$,

$$
A^T(A^{-1})^T=(A^{-1}A)^T=I^T=I.
$$

Hence the inverse of the transpose is the transpose of the inverse:

$$
(A^T)^{-1}=
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}^T=
\begin{pmatrix}
2 & -3 \\
-1 & 2 \\
\end{pmatrix}.
$$

**3. The inverse of $A^2$.** For an invertible $A$,

$$
(A^2)^{-1}=(A^{-1})^2.
$$

Justification: $A^2(A^{-1})^2=A(AA^{-1})A^{-1}=AIA^{-1}=AA^{-1}=I$. This is the rule $(AB)^{-1}=B^{-1}A^{-1}$ with $B=A$. Now square the given matrix:

$$
(A^{-1})^2=
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}=
\begin{pmatrix}
2\cdot 2+(-1)\cdot(-3) & 2\cdot(-1)+(-1)\cdot 2 \\
(-3)\cdot 2+2\cdot(-3) & (-3)\cdot(-1)+2\cdot 2 \\
\end{pmatrix}=
\begin{pmatrix}
7 & -4 \\
-12 & 7 \\
\end{pmatrix}.
$$

### Property / method

Properties of the inverse used (for invertible matrices of the same size and a number $c\neq 0$):

- $(cA)^{-1}=\frac1cA^{-1}$;
- $(A^T)^{-1}=(A^{-1})^T$;
- $(A^k)^{-1}=(A^{-1})^k$, a special case of $(AB)^{-1}=B^{-1}A^{-1}$.

Each of them follows from the definition of the inverse by checking that the proposed matrix multiplies the original one to $I$. The matrix $A$ itself is never needed.

### Verification

As an independent check only, recover $A$ from $A^{-1}$ by the $2\times 2$ formula. Here $\det A^{-1}=2\cdot 2-(-1)\cdot(-3)=1$, so

$$
A=
\begin{pmatrix}
2 & 1 \\
3 & 2 \\
\end{pmatrix}.
$$

Then

$$
A^2=
\begin{pmatrix}
2\cdot 2+1\cdot 3 & 2\cdot 1+1\cdot 2 \\
3\cdot 2+2\cdot 3 & 3\cdot 1+2\cdot 2 \\
\end{pmatrix}=
\begin{pmatrix}
7 & 4 \\
12 & 7 \\
\end{pmatrix},
$$

with $\det A^2=49-48=1$, and the $2\times 2$ formula gives

$$
(A^2)^{-1}=
\begin{pmatrix}
7 & -4 \\
-12 & 7 \\
\end{pmatrix},
$$

in agreement with step 3.

Similarly, for $3A$ we have $\det(3A)=6\cdot 6-3\cdot 9=9$ and

$$
3A=
\begin{pmatrix}
6 & 3 \\
9 & 6 \\
\end{pmatrix},\qquad
(3A)^{-1}=\frac19
\begin{pmatrix}
6 & -3 \\
-9 & 6 \\
\end{pmatrix}=
\begin{pmatrix}
\frac23 & -\frac13 \\
-1 & \frac23 \\
\end{pmatrix},
$$

which equals the matrix found in step 1.
