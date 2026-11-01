## Exercise 3. When Does the Inverse Not Exist?

### Result

For

$$
A=
\begin{pmatrix}
2 & 4 \\
1 & 2 \\
\end{pmatrix}
$$

we have $\det A=0$, and the first row equals twice the second row. In both descriptions the matrix is singular, so $A^{-1}$ does not exist.

### Main steps

**Way 1. The determinant.**

$$
\det A=2\cdot 2-4\cdot 1=4-4=0.
$$

A square matrix is invertible if and only if its determinant is nonzero. Since $\det A=0$, the matrix $A$ is not invertible. In the $2\times2$ formula

$$
A^{-1}=\frac{1}{\det A}
\begin{pmatrix}
2 & -4 \\
-1 & 2 \\
\end{pmatrix}
$$

the factor $\frac{1}{\det A}=\frac10$ is undefined.

**Way 2. Dependence of the rows.** Denote the rows by $r_1=(2,\ 4)$ and $r_2=(1,\ 2)$. Then

$$
r_1=2\cdot r_2.
$$

The rows are linearly dependent. Suppose that a matrix $X$ with $AX=I$ existed. The rows of the product $AX$ are the combinations of the rows of $X$ with coefficients taken from the rows of $A$, therefore

$$
\mathrm{row}_1(AX)=2\cdot\mathrm{row}_2(AX).
$$

For $AX=I$ this would mean $(1,\ 0)=2\cdot(0,\ 1)=(0,\ 2)$, which is false. Hence no matrix $X$ satisfies $AX=I$, and $A$ has no inverse.

**The two descriptions are connected.** For a $2\times 2$ matrix with rows $(a,\ b)$ and $(c,\ d)$, the condition $ad-bc=0$ says exactly that the rows are proportional. Here this is the relation $r_1=2r_2$, and the determinant measures this dependence: when one row is a multiple of the other, the "parallelogram" spanned by the rows is flat and has area $0$.

### Property / method

The following statements are equivalent for a square matrix $A$:

- $A$ is invertible;
- $\det A\neq 0$;
- the rows of $A$ are linearly independent;
- the columns of $A$ are linearly independent.

Failure of any one of them is a sign that $A^{-1}$ does not exist.

### Verification

The columns are also dependent: the second column $(4,\ 2)^T$ equals twice the first column $(2,\ 1)^T$. A nonzero vector sent to zero shows this explicitly:

$$
\begin{pmatrix}
2 & 4 \\
1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 \\
-1 \\
\end{pmatrix}=
\begin{pmatrix}
2\cdot 2+4\cdot(-1) \\
1\cdot 2+2\cdot(-1) \\
\end{pmatrix}=
\begin{pmatrix}
0 \\
0 \\
\end{pmatrix}.
$$

If $A^{-1}$ existed, multiplying this equality by $A^{-1}$ would give $(2,\ -1)^T=A^{-1}\cdot(0,\ 0)^T=(0,\ 0)^T$, which is false. This confirms that $A$ is not invertible.
