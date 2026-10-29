### Exercise 2. Determinant of a 3×3 Matrix

Given

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5 \\
\end{pmatrix},
$$

Sarrus' rule gives

$$
\begin{aligned}
\det A
&=1\cdot3\cdot5+2\cdot4\cdot2+(-1)\cdot0\cdot1 \\
&\quad-\bigl((-1)\cdot3\cdot2+2\cdot0\cdot5+1\cdot4\cdot1\bigr) \\
&=15+16+0-(-6+0+4) \\
&=31-(-2)=33.
\end{aligned}
$$

A check using cofactor expansion along the first row gives

$$
\begin{aligned}
\det A
&=1(15-4)-2(0-8)+(-1)(0-6) \\
&=11+16+6=33.
\end{aligned}
$$

Both calculations give $\det A=33$, so the result is consistent. Since the determinant is nonzero, $A$ is invertible.
