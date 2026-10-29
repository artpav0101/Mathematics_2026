Exercise 12. A Parameter Revealed by a Row Operation

Given

$$
A(t)=
\begin{pmatrix}
1 & 2 & 3\
2 & 4 & t\
0 & 1 & 1
\end{pmatrix},
$$

apply the row operation

$$
R_2\leftarrow R_2-2R_1.
$$

This operation does not change the determinant. The resulting matrix is

$$
\begin{pmatrix}
1 & 2 & 3\
0 & 0 & t-6\
0 & 1 & 1
\end{pmatrix}.
$$

Expanding along the second row gives

$$
\begin{aligned}
\det A(t)
&=-(t-6)
\begin{vmatrix}
1 & 2\
0 & 1
\end{vmatrix}\
&=-(t-6)(1\cdot1-2\cdot0)\
&=6-t.
\end{aligned}
$$

The matrix is not invertible when its determinant is zero:

$$
6-t=0
\quad\Longrightarrow\quad
\boxed{t=6}.
$$

For $t=6$, the second row of the original matrix is twice the first row:

$$
(2,4,6)=2(1,2,3).
$$

Therefore, the rows are linearly dependent, confirming that the determinant is zero.
