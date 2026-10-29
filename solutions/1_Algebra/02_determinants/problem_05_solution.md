### Exercise 5. Row Operations

Given

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2 \\
\end{pmatrix},
$$

use row replacements, which do not change the determinant:

$$
R_2\leftarrow R_2-2R_1,\qquad
R_3\leftarrow R_3+R_1.
$$

The resulting matrix is

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 6 & 5 \\
\end{pmatrix}.
$$

Expanding along the first column,

$$
\begin{aligned}
\det A
&=\det\begin{pmatrix}
-3 & -6 \\
6 & 5 \\
\end{pmatrix} \\
&=(-3)\cdot5-(-6)\cdot6 \\
&=-15+36=21.
\end{aligned}
$$

Neither row replacement changes the determinant, so $\det A=21$.
