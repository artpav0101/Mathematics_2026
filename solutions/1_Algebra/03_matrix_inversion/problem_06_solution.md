## Exercise 6. Solving a System Using the Inverse

### Result

For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix},\qquad
b=
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix}
$$

the solution of $Ax=b$ is

$$
x=A^{-1}b=
\begin{pmatrix}
\frac85 \\
\frac95 \\
\end{pmatrix}.
$$

### Main steps

**1. The inverse of $A$.** The determinant is

$$
\det A=2\cdot 3-1\cdot 1=5\neq 0,
$$

so $A^{-1}$ exists. By the $2\times2$ formula,

$$
A^{-1}=\frac15
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}.
$$

**2. Why $x=A^{-1}b$.** Multiply both sides of $Ax=b$ from the left by $A^{-1}$:

$$
A^{-1}(Ax)=A^{-1}b\quad\Longrightarrow\quad (A^{-1}A)x=A^{-1}b\quad\Longrightarrow\quad Ix=A^{-1}b\quad\Longrightarrow\quad x=A^{-1}b.
$$

**3. The product.**

$$
x=\frac15
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix}=\frac15
\begin{pmatrix}
3\cdot 5-1\cdot 7 \\
-1\cdot 5+2\cdot 7 \\
\end{pmatrix}=\frac15
\begin{pmatrix}
8 \\
9 \\
\end{pmatrix}=
\begin{pmatrix}
\frac85 \\
\frac95 \\
\end{pmatrix}.
$$

### Property / method

If $A$ is invertible, the system $Ax=b$ has exactly one solution, $x=A^{-1}b$. The inverse is applied from the left, because $A$ multiplies $x$ from the left in the equation.

### Verification

Substitute $x=\left(\frac85,\ \frac95\right)^T$ into $Ax$:

$$
Ax=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
\frac85 \\
\frac95 \\
\end{pmatrix}=
\begin{pmatrix}
2\cdot\frac85+\frac95 \\
\frac85+3\cdot\frac95 \\
\end{pmatrix}=
\begin{pmatrix}
\frac{16}{5}+\frac95 \\
\frac85+\frac{27}{5} \\
\end{pmatrix}=
\begin{pmatrix}
\frac{25}{5} \\
\frac{35}{5} \\
\end{pmatrix}=
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix}=b.
$$

The equation is satisfied.
