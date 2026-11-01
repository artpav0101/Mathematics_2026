## Exercise 15. Combining Determinant Properties

### Result

For invertible $2\times2$ matrices $A$ and $B$ with $\det A=-2$ and $\det B=3$:

$$
\det\left(B^{-1}A^TB\right)=-2.
$$

### Main steps

**1. Determinant of a product.** The determinant of a product of square matrices is the product of the determinants:

$$
\det\left(B^{-1}A^TB\right)=\det\left(B^{-1}\right)\cdot\det\left(A^T\right)\cdot\det B.
$$

**2. Determinant of the inverse.** Since $BB^{-1}=I$ and $\det I=1$,

$$
\det\left(B^{-1}\right)=\frac{1}{\det B}=\frac13.
$$

**3. Determinant of the transpose.** Transposition does not change the determinant:

$$
\det\left(A^T\right)=\det A=-2.
$$

**4. Substitution.**

$$
\begin{aligned}
\det\left(B^{-1}A^TB\right) &= \frac13\cdot(-2)\cdot 3 \\
                            &= -2.
\end{aligned}
$$

### Why the factors with $B$ cancel

The two factors containing $B$ are $\det\left(B^{-1}\right)$ and $\det B$. Because $\det\left(B^{-1}\right)=\frac{1}{\det B}$, they multiply to

$$
\det\left(B^{-1}\right)\cdot\det B=\frac{1}{\det B}\cdot\det B=1.
$$

Numbers can be multiplied in any order, so the factor $\det B$ can be moved next to $\det\left(B^{-1}\right)$, and the pair disappears. What is left is $\det\left(A^T\right)=\det A$. The result does not depend on $B$ at all, which is why the entries of the matrices were not needed.

### Property / method

The properties used, in order:

1. $\det(XYZ)=\det X\cdot\det Y\cdot\det Z$ for square matrices of equal size;
2. $\det\left(B^{-1}\right)=\frac{1}{\det B}$ for an invertible $B$;
3. $\det\left(A^T\right)=\det A$.

The matrix $B^{-1}A^TB$ is a **similarity transformation** of $A^T$. The computation shows that similar matrices have the same determinant: $\det\left(B^{-1}XB\right)=\det X$.

### Verification

Test the result on concrete diagonal matrices with the prescribed determinants. Let

$$
A=
\begin{pmatrix}
1 & 0 \\
0 & -2 \\
\end{pmatrix},\qquad
B=
\begin{pmatrix}
3 & 0 \\
0 & 1 \\
\end{pmatrix},
$$

so that $\det A=-2$ and $\det B=3$. Then $A^T=A$, $B^{-1}=\mathrm{diag}\left(\frac13,\ 1\right)$, and

$$
B^{-1}A^TB=
\begin{pmatrix}
\frac13 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
0 & -2 \\
\end{pmatrix}
\begin{pmatrix}
3 & 0 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 0 \\
0 & -2 \\
\end{pmatrix},
$$

with determinant $1\cdot(-2)=-2$, as computed above.
