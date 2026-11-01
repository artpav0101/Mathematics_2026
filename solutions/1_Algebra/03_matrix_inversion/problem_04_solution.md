## Exercise 4. Gauss–Jordan

### Result

For

$$
A=
\begin{pmatrix}
1 & 2 \\
3 & 5 \\
\end{pmatrix}
$$

the inverse is

$$
A^{-1}=
\begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix}.
$$

### Main steps

Form the augmented matrix $[A\mid I]$ and apply row operations until the left block becomes $I$.

**Start.**

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
3 & 5 & \mid & 0 & 1 \\
\end{pmatrix}
$$

**Step 1.** $R_2\leftarrow R_2-3R_1$. This clears the entry below the first pivot. The new second row is $(3-3,\ 5-6\mid 0-3,\ 1-0)=(0,\ -1\mid -3,\ 1)$.

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
0 & -1 & \mid & -3 & 1 \\
\end{pmatrix}
$$

**Step 2.** $R_2\leftarrow -R_2$. This makes the second pivot equal to $1$.

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}
$$

**Step 3.** $R_1\leftarrow R_1-2R_2$. This clears the entry above the second pivot. The new first row is $(1,\ 2-2\mid 1-6,\ 0+2)=(1,\ 0\mid -5,\ 2)$.

$$
\begin{pmatrix}
1 & 0 & \mid & -5 & 2 \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}
$$

The left block is $I$. The right block is

$$
A^{-1}=
\begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix}.
$$

### Why the right block is the inverse

Each elementary row operation is the same as multiplication from the left by an invertible elementary matrix. If the operations used are $E_1,E_2,E_3$ (in this order), the whole procedure multiplies the augmented matrix by $E=E_3E_2E_1$:

$$
E\,[A\mid I]=[EA\mid E\,I]=[EA\mid E].
$$

The procedure ends with $EA=I$ on the left. By the definition of the inverse, this means $E=A^{-1}$. The right block is $E\,I=E$, and therefore it is exactly $A^{-1}$. In other words, the same operations that transform $A$ into $I$ transform $I$ into $A^{-1}$.

### Property / method

The Gauss–Jordan method works for any square matrix. If the left block cannot be reduced to $I$ (a zero row appears), the matrix is singular and has no inverse.

### Verification

Multiply $A$ by the result:

$$
AA^{-1}=
\begin{pmatrix}
1 & 2 \\
3 & 5 \\
\end{pmatrix}
\begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot(-5)+2\cdot 3 & 1\cdot 2+2\cdot(-1) \\
3\cdot(-5)+5\cdot 3 & 3\cdot 2+5\cdot(-1) \\
\end{pmatrix}=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}.
$$

The $2\times2$ formula gives the same matrix: $\det A=1\cdot 5-2\cdot 3=-1$, and

$$
A^{-1}=\frac{1}{-1}
\begin{pmatrix}
5 & -2 \\
-3 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix}.
$$
