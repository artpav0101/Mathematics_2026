### Exercise 11. Shortening the Calculation with Row Operations

Start with

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}.
$$

Apply the row replacements

$$
R_2\leftarrow R_2-R_1,\qquad
R_3\leftarrow R_3-R_1.
$$

These operations do not change the determinant, giving

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 2 & 3 \\
\end{pmatrix}.
$$

Expanding along the first column,

$$
\det A=
\det\begin{pmatrix}
1 & 1 \\
2 & 3 \\
\end{pmatrix}
=1\cdot3-1\cdot2=1.
$$

Therefore, $\det A=1$.
