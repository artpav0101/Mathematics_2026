### Exercise 14. A System of Equations and the Determinant

The coefficient matrix is

$$
A=
\begin{pmatrix}
1 & 2 \\
k & 4 \\
\end{pmatrix}.
$$

Its determinant is

$$
\det A=4-2k.
$$

The system has exactly one solution for every right-hand side $b$ precisely when $A$ is invertible, which occurs when

$$
4-2k\neq0
\quad\Longrightarrow\quad
k\neq2.
$$

For the exceptional value $k=2$, the system has coefficient rows $(1,2)$ and $(2,4)$, so the second equation's left-hand side is twice the first.

**Infinitely many solutions:** choose

$$
b=
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}.
$$

The system becomes $x+2y=1$ and $2x+4y=2$. The second equation repeats the first, so there are infinitely many solutions.

**No solution:** choose

$$
b=
\begin{pmatrix}
1 \\
0 \\
\end{pmatrix}.
$$

The system becomes $x+2y=1$ and $2x+4y=0$. The second equation contradicts twice the first, so there is no solution.
