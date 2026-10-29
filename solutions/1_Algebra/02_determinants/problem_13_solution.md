### Exercise 13. Determinant by Elimination

Given

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 5 & 7 \\
1 & 0 & 2 \\
\end{pmatrix},
$$

apply row replacements:

$$
R_2\leftarrow R_2-2R_1,\qquad
R_3\leftarrow R_3-R_1.
$$

Neither operation changes the determinant, so the matrix becomes

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & -2 & -1 \\
\end{pmatrix}.
$$

Next, apply $R_3\leftarrow R_3+2R_2$, which also leaves the determinant unchanged:

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1 \\
\end{pmatrix}.
$$

The resulting matrix is upper triangular. Its determinant is the product of the diagonal entries:

$$
\det A=1\cdot1\cdot1=1.
$$
