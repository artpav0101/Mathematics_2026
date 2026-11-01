## Exercise 8. Inverse of a Transformation

### Result

For the scaling matrix

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & \frac12 \\
\end{pmatrix}
$$

the inverse is

$$
S^{-1}=
\begin{pmatrix}
\frac12 & 0 \\
0 & 2 \\
\end{pmatrix}.
$$

### Main steps

**1. The inverse.** $S$ is a diagonal matrix with nonzero diagonal entries $2$ and $\frac12$. Its inverse is the diagonal matrix with the reciprocal entries $\frac12$ and $2$. The $2\times 2$ formula confirms it: $\det S=2\cdot\frac12-0\cdot 0=1$, and

$$
S^{-1}=\frac11
\begin{pmatrix}
\frac12 & 0 \\
0 & 2 \\
\end{pmatrix}.
$$

**2. Geometric meaning of $S$.** The transformation $x\mapsto Sx$ stretches the plane by a factor of $2$ in the $x$-direction and compresses it by a factor of $\frac12$ in the $y$-direction:

$$
S
\begin{pmatrix}
x \\
y \\
\end{pmatrix}=
\begin{pmatrix}
2x \\
\frac12y \\
\end{pmatrix}.
$$

**3. Geometric meaning of $S^{-1}$.** The transformation $x\mapsto S^{-1}x$ does the opposite: it compresses the plane by a factor of $\frac12$ in the $x$-direction and stretches it by a factor of $2$ in the $y$-direction. Every stretching is cancelled by the corresponding compression, so $S^{-1}$ undoes $S$ and returns every point to its original position.

**4. Action on a simple vector.** Take $v=(1,\ 2)^T$. First apply $S$:

$$
Sv=
\begin{pmatrix}
2 & 0 \\
0 & \frac12 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}=
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}.
$$

Then apply $S^{-1}$ to the result:

$$
S^{-1}(Sv)=
\begin{pmatrix}
\frac12 & 0 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}=
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}=v.
$$

The original vector is recovered.

### Property / method

The inverse of an invertible matrix represents the inverse transformation: $S^{-1}(Sv)=v$ and $S(S^{-1}v)=v$ for every vector $v$. For a scaling with factors $s_1,s_2\neq 0$ the inverse is the scaling with factors $\frac{1}{s_1},\frac{1}{s_2}$.

### Verification

Check both products of matrices:

$$
SS^{-1}=
\begin{pmatrix}
2\cdot\frac12 & 0 \\
0 & \frac12\cdot 2 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad
S^{-1}S=
\begin{pmatrix}
\frac12\cdot 2 & 0 \\
0 & 2\cdot\frac12 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}.
$$

Also, $\det S=1$ means that $S$ preserves areas (stretching by $2$ and compressing by $\frac12$ cancel in area), and the same is true for $S^{-1}$.
