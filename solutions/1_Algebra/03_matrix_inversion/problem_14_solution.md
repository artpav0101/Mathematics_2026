## Exercise 14. A Matrix That Is Its Own Inverse

### Result

If a square matrix $A$ satisfies $A^2=I$, then $A^{-1}=A$.

An example of a $2\times 2$ matrix with this property that is different from $I$ and $-I$ is

$$
A=
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix}.
$$

### Main steps

**1. The proof.** By definition, a square matrix $B$ is the inverse of $A$ if

$$
AB=I\qquad\mathrm{and}\qquad BA=I.
$$

Take $B=A$. Then both conditions read

$$
AA=A^2=I,
$$

and this is the assumption. Hence $B=A$ satisfies the definition of the inverse. Since the inverse of a matrix is unique, $A$ is invertible and

$$
A^{-1}=A.
$$

**2. The example.** Take the matrix that swaps the two coordinates:

$$
A=
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix}.
$$

It is different from $I$ and from $-I$, because its diagonal entries are $0$.

**3. Verification by multiplication.**

$$
A^2=
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
0\cdot 0+1\cdot 1 & 0\cdot 1+1\cdot 0 \\
1\cdot 0+0\cdot 1 & 1\cdot 1+0\cdot 0 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}=I.
$$

By the first part, $A^{-1}=A$. The $2\times 2$ formula agrees: $\det A=0\cdot 0-1\cdot 1=-1$, and

$$
A^{-1}=\frac{1}{-1}
\begin{pmatrix}
0 & -1 \\
-1 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix}=A.
$$

### Property / method

A matrix with $A^2=I$ is called an **involution**. Geometrically it undoes itself when it is applied twice. The matrix above reflects the plane in the line $y=x$, and two reflections in the same line give the identity transformation.

Other examples of $2\times 2$ involutions different from $\pm I$ are

$$
\begin{pmatrix}
1 & 0 \\
0 & -1 \\
\end{pmatrix},\qquad
\begin{pmatrix}
1 & 1 \\
0 & -1 \\
\end{pmatrix}.
$$

### Verification

For the last matrix, call it $C$:

$$
C^2=
\begin{pmatrix}
1 & 1 \\
0 & -1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & -1 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot 1+1\cdot 0 & 1\cdot 1+1\cdot(-1) \\
0\cdot 1+(-1)\cdot 0 & 0\cdot 1+(-1)\cdot(-1) \\
\end{pmatrix}=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}=I.
$$

Also, from $A^2=I$ it follows that $(\det A)^2=\det I=1$, so an involution always has $\det A=1$ or $\det A=-1$. This matches the examples above: the first one has determinant $-1$.
