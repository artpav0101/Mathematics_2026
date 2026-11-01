## Exercise 13. Undoing a Composite Transformation

### Result

For

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad
H=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad
T=HS=
\begin{pmatrix}
2 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

the inverse is

$$
T^{-1}=S^{-1}H^{-1}=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & 1 \\
\end{pmatrix}.
$$

The product in the wrong order, $H^{-1}S^{-1}$, is a different matrix.

### Main steps

**1. The matrix $T=HS$.**

$$
T=HS=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot 2+1\cdot 0 & 1\cdot 0+1\cdot 1 \\
0\cdot 2+1\cdot 0 & 0\cdot 0+1\cdot 1 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 1 \\
0 & 1 \\
\end{pmatrix}.
$$

**Method 1. Compute $T$ first, then invert it.** The determinant is $\det T=2\cdot 1-1\cdot 0=2$, so by the $2\times 2$ formula

$$
T^{-1}=\frac12
\begin{pmatrix}
1 & -1 \\
0 & 2 \\
\end{pmatrix}=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & 1 \\
\end{pmatrix}.
$$

**Method 2. Use $(HS)^{-1}=S^{-1}H^{-1}$.** First find the inverses of the factors:

$$
S^{-1}=
\begin{pmatrix}
\frac12 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad
H^{-1}=
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}.
$$

The matrix $S^{-1}$ is diagonal with reciprocal entries. For $H$ we have $\det H=1$, and the $2\times 2$ formula gives $H^{-1}$. Now multiply in the order $S^{-1}H^{-1}$:

$$
S^{-1}H^{-1}=
\begin{pmatrix}
\frac12 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
\frac12\cdot 1+0\cdot 0 & \frac12\cdot(-1)+0\cdot 1 \\
0\cdot 1+1\cdot 0 & 0\cdot(-1)+1\cdot 1 \\
\end{pmatrix}=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & 1 \\
\end{pmatrix}.
$$

**Comparison.** Both methods give the same matrix:

$$
T^{-1}=S^{-1}H^{-1}=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & 1 \\
\end{pmatrix}.
$$

**The incorrect order $H^{-1}S^{-1}$.**

$$
H^{-1}S^{-1}=
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
\frac12 & 0 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot\frac12+(-1)\cdot 0 & 1\cdot 0+(-1)\cdot 1 \\
0\cdot\frac12+1\cdot 0 & 0\cdot 0+1\cdot 1 \\
\end{pmatrix}=
\begin{pmatrix}
\frac12 & -1 \\
0 & 1 \\
\end{pmatrix}.
$$

This is not $T^{-1}$: the entry in position $(1,2)$ is $-1$ instead of $-\frac12$. Indeed, it does not undo $T$:

$$
T\,(H^{-1}S^{-1})=
\begin{pmatrix}
2 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
\frac12 & -1 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}\neq I.
$$

### The rule "undo from the end"

The product $T=HS$ applied to a vector $x$ means: first apply $S$ (nonuniform scaling), then apply $H$ (shear), since $Tx=H(Sx)$:

$$
x\ \xrightarrow{\ S\ }\ Sx\ \xrightarrow{\ H\ }\ HSx.
$$

The last operation performed is $H$, so it must be undone first. Then $S$ is undone:

$$
HSx\ \xrightarrow{\ H^{-1}\ }\ Sx\ \xrightarrow{\ S^{-1}\ }\ x.
$$

Written as a matrix product, the operation that acts first stands rightmost. Here $H^{-1}$ acts first and $S^{-1}$ acts second, therefore

$$
T^{-1}=S^{-1}H^{-1}.
$$

### Property / method

For invertible matrices of the same size,

$$
(HS)^{-1}=S^{-1}H^{-1}.
$$

The inverse of a composition is the composition of the inverses in the reverse order.

### Verification

Check that $S^{-1}H^{-1}$ multiplies $T$ to the identity:

$$
T\,(S^{-1}H^{-1})=
\begin{pmatrix}
2 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
2\cdot\frac12+1\cdot 0 & 2\cdot\left(-\frac12\right)+1\cdot 1 \\
0\cdot\frac12+1\cdot 0 & 0\cdot\left(-\frac12\right)+1\cdot 1 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}.
$$
