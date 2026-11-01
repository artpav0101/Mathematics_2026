## Exercise 7. Inverse of a Product

### Result

For

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad
B=
\begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix}
$$

we obtain

$$
(AB)^{-1}=B^{-1}A^{-1}=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & \frac13 \\
\end{pmatrix}.
$$

### Main steps

**1. The product $AB$.**

$$
AB=
\begin{pmatrix}
1\cdot 2+1\cdot 0 & 1\cdot 0+1\cdot 3 \\
0\cdot 2+1\cdot 0 & 0\cdot 0+1\cdot 3 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 3 \\
0 & 3 \\
\end{pmatrix}.
$$

**2. The inverse $(AB)^{-1}$ by the $2\times 2$ formula.** The determinant is $\det(AB)=2\cdot 3-3\cdot 0=6$, so

$$
(AB)^{-1}=\frac16
\begin{pmatrix}
3 & -3 \\
0 & 2 \\
\end{pmatrix}=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & \frac13 \\
\end{pmatrix}.
$$

**3. The inverses of the factors.** For $A$ we have $\det A=1$, and for the diagonal matrix $B$ the inverse is obtained by inverting the diagonal entries:

$$
A^{-1}=
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix},\qquad
B^{-1}=
\begin{pmatrix}
\frac12 & 0 \\
0 & \frac13 \\
\end{pmatrix}.
$$

**4. The product $B^{-1}A^{-1}$.**

$$
B^{-1}A^{-1}=
\begin{pmatrix}
\frac12\cdot 1+0\cdot 0 & \frac12\cdot(-1)+0\cdot 1 \\
0\cdot 1+\frac13\cdot 0 & 0\cdot(-1)+\frac13\cdot 1 \\
\end{pmatrix}=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & \frac13 \\
\end{pmatrix}.
$$

**5. Comparison.** The matrices in steps 2 and 4 are identical:

$$
(AB)^{-1}=B^{-1}A^{-1}.
$$

### Meaning of the reversed order

The product $AB$ applied to a vector $x$ means: first apply $B$, then apply $A$, because $(AB)x=A(Bx)$. To undo these two actions, they must be undone in the opposite order: first undo $A$ (apply $A^{-1}$), then undo $B$ (apply $B^{-1}$). This gives $B^{-1}A^{-1}$. Algebraically,

$$
(AB)(B^{-1}A^{-1})=A(BB^{-1})A^{-1}=AIA^{-1}=AA^{-1}=I,
$$

and the middle factors cancel only when $B^{-1}$ stands directly next to $B$.

### Property / method

For invertible square matrices of the same size,

$$
(AB)^{-1}=B^{-1}A^{-1}.
$$

The order must be reversed, because matrix multiplication is not commutative.

### Verification

The product in the wrong order is

$$
A^{-1}B^{-1}=
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
\frac12 & 0 \\
0 & \frac13 \\
\end{pmatrix}=
\begin{pmatrix}
\frac12 & -\frac13 \\
0 & \frac13 \\
\end{pmatrix}\neq (AB)^{-1}.
$$

Only the reversed order $B^{-1}A^{-1}$ gives the inverse of $AB$. Moreover,

$$
(AB)\,(B^{-1}A^{-1})=
\begin{pmatrix}
2 & 3 \\
0 & 3 \\
\end{pmatrix}
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & \frac13 \\
\end{pmatrix}=
\begin{pmatrix}
1 & -1+1 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}.
$$
