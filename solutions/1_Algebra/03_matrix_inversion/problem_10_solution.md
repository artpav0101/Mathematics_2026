## Exercise 10. Inverse of a Diagonal Matrix

### Result

For

$$
D=
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5 \\
\end{pmatrix},\qquad
E=
\begin{pmatrix}
2 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}
$$

the matrix $D$ is invertible with

$$
D^{-1}=
\begin{pmatrix}
\frac12 & 0 & 0 \\
0 & -\frac13 & 0 \\
0 & 0 & \frac15 \\
\end{pmatrix},
$$

and the matrix $E$ is not invertible.

### Main steps

**1. The rule for diagonal matrices.** A diagonal matrix with diagonal entries $d_1,d_2,d_3$ is invertible if and only if all $d_i\neq 0$. In this case the inverse is the diagonal matrix with the entries $\frac{1}{d_1},\frac{1}{d_2},\frac{1}{d_3}$. The reason is that multiplication of two diagonal matrices multiplies the diagonal entries separately:

$$
\mathrm{diag}(d_1,d_2,d_3)\cdot\mathrm{diag}(e_1,e_2,e_3)=\mathrm{diag}(d_1e_1,\ d_2e_2,\ d_3e_3),
$$

and the product is $I$ exactly when $d_ie_i=1$ for each $i$.

**2. The matrix $D$.** The diagonal entries $2$, $-3$, $5$ are all nonzero. Hence $D$ is invertible, and

$$
D^{-1}=\mathrm{diag}\left(\frac12,\ -\frac13,\ \frac15\right).
$$

**3. The matrix $E$.** The diagonal entry $d_2=0$ is zero, so $E$ is not invertible. Directly: the second row of $E$ is the zero row, so for every matrix $X$ the second row of $EX$ is also zero. But the second row of $I$ is $(0,\ 1,\ 0)\neq(0,\ 0,\ 0)$. Therefore $EX=I$ has no solution.

### Property / method

For a diagonal matrix, invertibility and the inverse can be read from the diagonal. No elimination is needed. Equivalently, $\det D=2\cdot(-3)\cdot 5=-30\neq 0$, whereas $\det E=2\cdot 0\cdot 5=0$.

### Verification

Multiply $D$ by $D^{-1}$:

$$
DD^{-1}=
\begin{pmatrix}
2\cdot\frac12 & 0 & 0 \\
0 & (-3)\cdot\left(-\frac13\right) & 0 \\
0 & 0 & 5\cdot\frac15 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}=I.
$$

The product $D^{-1}D$ is the same matrix, because diagonal matrices commute. This confirms that $D^{-1}$ is correct.
