## Question

### Exercise 3. Swapping Two Rows
For

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 3 & 1 \\
2 & 1 & 1 \\
\end{pmatrix}
$$

compute $\det A$. Then form a matrix $B$ by swapping the first and second rows of $A$.

First predict $\det B$ using a determinant property, and then verify your prediction by calculation.

> **Why this exercise:** gives a second classical calculation with a $3\times3$ determinant while teaching the precise effect of a row swap on the sign of the determinant.

## Solution

For

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 3 & 1 \\
2 & 1 & 1 \\
\end{pmatrix},\qquad
B=
\begin{pmatrix}
0 & 3 & 1 \\
1 & 2 & 0 \\
2 & 1 & 1 \\
\end{pmatrix}
$$

the determinants are

$$
\det A=6,\qquad \det B=-6.
$$

### Main steps

**1. The determinant of $A$ (Sarrus' rule).**

$$
\begin{aligned}
a_{11}a_{22}a_{33}+a_{12}a_{23}a_{31}+a_{13}a_{21}a_{32} &= 1\cdot 3\cdot 1+2\cdot 1\cdot 2+0\cdot 0\cdot 1 = 3+4+0=7, \\
a_{13}a_{22}a_{31}+a_{11}a_{23}a_{32}+a_{12}a_{21}a_{33} &= 0\cdot 3\cdot 2+1\cdot 1\cdot 1+2\cdot 0\cdot 1 = 0+1+0=1.
\end{aligned}
$$

Therefore

$$
\det A=7-1=6.
$$

**2. Prediction for $B$.** The matrix $B$ is obtained from $A$ by swapping rows $1$ and $2$. Swapping two rows multiplies the determinant by $-1$. Therefore

$$
\det B=-\det A=-6.
$$

**3. Direct computation of $\det B$.** For

$$
B=
\begin{pmatrix}
0 & 3 & 1 \\
1 & 2 & 0 \\
2 & 1 & 1 \\
\end{pmatrix}
$$

Sarrus' rule gives

$$
\begin{aligned}
b_{11}b_{22}b_{33}+b_{12}b_{23}b_{31}+b_{13}b_{21}b_{32} &= 0\cdot 2\cdot 1+3\cdot 0\cdot 2+1\cdot 1\cdot 1 = 0+0+1=1, \\
b_{13}b_{22}b_{31}+b_{11}b_{23}b_{32}+b_{12}b_{21}b_{33} &= 1\cdot 2\cdot 2+0\cdot 0\cdot 1+3\cdot 1\cdot 1 = 4+0+3=7.
\end{aligned}
$$

Therefore

$$
\det B=1-7=-6.
$$

The direct computation agrees with the prediction.

### Property / method

Swapping two rows of a square matrix changes the sign of its determinant. For a $2\times2$ matrix this is immediate:

$$
\det
\begin{pmatrix}
c & d \\
a & b \\
\end{pmatrix}=cb-da=-(ad-bc)=-\det
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}.
$$

The same rule holds for every size $n\times n$. It is the reason why the determinant measures orientation: a row swap reverses it.

### Verification

Swapping the same two rows a second time returns $B$ to $A$, so the determinant must change sign twice:

$$
\det A=-\det B=-(-6)=6.
$$

This agrees with the value computed in step 1.
