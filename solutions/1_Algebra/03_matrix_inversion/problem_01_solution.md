## Exercise 1. Definition of the Inverse

### Result

For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix},\qquad
B=
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}
$$

both products equal the identity matrix:

$$
AB=I,\qquad BA=I.
$$

Therefore $B=A^{-1}$.

### Main steps

**1. The product $AB$.** Each entry is the dot product of a row of $A$ with a column of $B$:

$$
AB=
\begin{pmatrix}
2\cdot 1+1\cdot(-1) & 2\cdot(-1)+1\cdot 2 \\
1\cdot 1+1\cdot(-1) & 1\cdot(-1)+1\cdot 2 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}=I.
$$

**2. The product $BA$.**

$$
BA=
\begin{pmatrix}
1\cdot 2+(-1)\cdot 1 & 1\cdot 1+(-1)\cdot 1 \\
(-1)\cdot 2+2\cdot 1 & (-1)\cdot 1+2\cdot 1 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}=I.
$$

**3. Relation to the definition.** A square matrix $B$ is the inverse of a square matrix $A$ if

$$
AB=BA=I.
$$

Both conditions hold, so $B=A^{-1}$ (and, symmetrically, $A=B^{-1}$).

### Property / method

The definition of the inverse is a statement about products, not about a formula: $B$ is the inverse of $A$ exactly when multiplying by $B$ undoes multiplication by $A$ from either side. The inverse of a matrix, if it exists, is unique, so a single matrix $B$ with $AB=BA=I$ is *the* inverse.

For square matrices of the same size, one of the equalities $AB=I$ and $BA=I$ already implies the other. Computing both, as done here, is a useful consistency check.

### Verification

By the $2\times 2$ formula, $\det A=2\cdot 1-1\cdot 1=1$ and

$$
A^{-1}=\frac{1}{1}
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}=B.
$$

This agrees with the result obtained from the definition.
