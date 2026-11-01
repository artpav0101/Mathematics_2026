## Exercise 5. A 3×3 Matrix

### Result

For

$$
A=
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
\end{pmatrix}
$$

the inverse is

$$
A^{-1}=\frac12
\begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1 \\
\end{pmatrix}.
$$

### Main steps

Form the augmented matrix $[A\mid I]$ and reduce the left block to $I$.

**Start.**

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
1 & 0 & 1 & \mid & 0 & 0 & 1 \\
\end{pmatrix}
$$

**Step 1.** $R_3\leftarrow R_3-R_1$. This clears the entry below the first pivot.

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & -1 & 1 & \mid & -1 & 0 & 1 \\
\end{pmatrix}
$$

**Step 2.** $R_3\leftarrow R_3+R_2$. This clears the entry below the second pivot.

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & 0 & 2 & \mid & -1 & 1 & 1 \\
\end{pmatrix}
$$

**Step 3.** $R_3\leftarrow\frac12R_3$. This makes the third pivot equal to $1$.

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & 0 & 1 & \mid & -\frac12 & \frac12 & \frac12 \\
\end{pmatrix}
$$

**Step 4.** $R_2\leftarrow R_2-R_3$. This clears the entry above the third pivot. The new second row is $(0,\ 1,\ 0\mid 0+\frac12,\ 1-\frac12,\ 0-\frac12)$.

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 0 & \mid & \frac12 & \frac12 & -\frac12 \\
0 & 0 & 1 & \mid & -\frac12 & \frac12 & \frac12 \\
\end{pmatrix}
$$

**Step 5.** $R_1\leftarrow R_1-R_2$. This clears the entry above the second pivot. The new first row is $(1,\ 0,\ 0\mid 1-\frac12,\ 0-\frac12,\ 0+\frac12)$.

$$
\begin{pmatrix}
1 & 0 & 0 & \mid & \frac12 & -\frac12 & \frac12 \\
0 & 1 & 0 & \mid & \frac12 & \frac12 & -\frac12 \\
0 & 0 & 1 & \mid & -\frac12 & \frac12 & \frac12 \\
\end{pmatrix}
$$

The left block is $I$, so the right block is $A^{-1}$:

$$
A^{-1}=\frac12
\begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1 \\
\end{pmatrix}.
$$

### Property / method

The $2\times 2$ formula does not extend to $3\times 3$ matrices in a simple form, so the Gauss–Jordan method is used. It reduces $[A\mid I]$ to $[I\mid A^{-1}]$ by row operations: first clear the entries below the pivots (forward elimination), then scale the pivots to $1$ and clear the entries above them (backward elimination). The pivot $2$ obtained in step 2 is consistent with $\det A=2$, which is nonzero, so the inverse exists.

### Verification

Let

$$
N=
\begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1 \\
\end{pmatrix},
$$

so that $A^{-1}=\frac12N$. Compute $AN$ entry by entry:

$$
AN=
\begin{pmatrix}
1\cdot 1+1\cdot 1+0\cdot(-1) & 1\cdot(-1)+1\cdot 1+0\cdot 1 & 1\cdot 1+1\cdot(-1)+0\cdot 1 \\
0\cdot 1+1\cdot 1+1\cdot(-1) & 0\cdot(-1)+1\cdot 1+1\cdot 1 & 0\cdot 1+1\cdot(-1)+1\cdot 1 \\
1\cdot 1+0\cdot 1+1\cdot(-1) & 1\cdot(-1)+0\cdot 1+1\cdot 1 & 1\cdot 1+0\cdot(-1)+1\cdot 1 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 2 \\
\end{pmatrix}.
$$

Hence

$$
AA^{-1}=\frac12AN=
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}=I.
$$

The determinant of $A$ also fits: expanding along the first row gives $\det A=1\cdot(1\cdot 1-1\cdot 0)-1\cdot(0\cdot 1-1\cdot 1)+0=1+1=2$.
