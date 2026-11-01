## Exercise 8. Determinant of a Product

### Result

For square matrices $A$ and $B$ of the same size with $\det A=3$ and $\det B=-5$:

$$
\det(AB)=-15,\qquad \det(BA)=-15,\qquad \det(A^{-1}B)=-\frac{5}{3}.
$$

### Main steps

**1. $\det(AB)$.** The determinant of a product equals the product of the determinants:

$$
\det(AB)=\det A\cdot\det B=3\cdot(-5)=-15.
$$

**2. $\det(BA)$.** By the same rule,

$$
\det(BA)=\det B\cdot\det A=(-5)\cdot 3=-15.
$$

**3. $\det(A^{-1}B)$.** Since $\det A=3\neq 0$, the matrix $A$ is invertible, so $A^{-1}$ exists. The determinant of the inverse is the reciprocal of the determinant:

$$
\det(A^{-1})=\frac{1}{\det A}=\frac13.
$$

Then

$$
\det(A^{-1}B)=\det(A^{-1})\cdot\det B=\frac13\cdot(-5)=-\frac53.
$$

**4. Why $\det(AB)=\det(BA)$ although usually $AB\neq BA$.** The matrices $AB$ and $BA$ are in general different matrices. However, the determinant of each of them is the product of the same two real numbers $\det A$ and $\det B$. Multiplication of real numbers is commutative:

$$
\det(AB)=\det A\cdot\det B=\det B\cdot\det A=\det(BA).
$$

The determinant "forgets" the order of the factors, even though the matrices themselves do not.

### Property / method

Properties used:

- $\det(AB)=\det A\cdot\det B$ for square matrices of the same size;
- $\det(A^{-1})=\frac{1}{\det A}$, which follows from $\det(A)\det(A^{-1})=\det(AA^{-1})=\det I=1$;
- a square matrix is invertible if and only if its determinant is nonzero.

### Verification

Take

$$
A=
\begin{pmatrix}
3 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad
B=
\begin{pmatrix}
-5 & 1 \\
0 & 1 \\
\end{pmatrix},
$$

so that $\det A=3$ and $\det B=-5$. Then

$$
AB=
\begin{pmatrix}
-15 & 3 \\
0 & 1 \\
\end{pmatrix},\qquad
BA=
\begin{pmatrix}
-15 & 1 \\
0 & 1 \\
\end{pmatrix}.
$$

These matrices are different, $AB\neq BA$, but $\det(AB)=-15\cdot 1-3\cdot 0=-15$ and $\det(BA)=-15\cdot 1-1\cdot 0=-15$. Both agree with the value $-15$ found above.
