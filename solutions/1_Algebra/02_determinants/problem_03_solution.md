### Exercise 3. Swapping Two Rows

For

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 3 & 1 \\
2 & 1 & 1 \\
\end{pmatrix},
$$

expansion along the first row gives

$$
\begin{aligned}
\det A
&=1(3\cdot1-1\cdot1)-2(0\cdot1-1\cdot2) \\
&=2+4=6.
\end{aligned}
$$

Let $B$ be obtained by swapping the first and second rows:

$$
B=
\begin{pmatrix}
0 & 3 & 1 \\
1 & 2 & 0 \\
2 & 1 & 1 \\
\end{pmatrix}.
$$

Swapping two rows changes the sign of the determinant, so the prediction is $\det B=-\det A=-6$. Direct expansion along the first row verifies the prediction:

$$
\begin{aligned}
\det B
&=0-3(1\cdot1-0\cdot2)+1(1\cdot1-2\cdot2) \\
&=-3+(1-4)=-6.
\end{aligned}
$$

Thus $\det B=-6$, as predicted.
