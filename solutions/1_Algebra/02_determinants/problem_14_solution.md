## Question 

### Exercise 14. A System of Equations and the Determinant
Consider the system $Ax=b$, where

$$
A=
\begin{pmatrix}
1 & 2 \\
k & 4 \\
\end{pmatrix}.
$$

For which values of $k$ does the system have exactly one solution for every $b$? For the remaining value, give an example of a right-hand side $b$ for which the system has infinitely many solutions, and an example for which it has no solution.

> **Why this exercise:** connects the determinant with uniqueness of solutions and requires distinguishing the exceptional cases.


## Solution

For $Ax=b$ with

$$
A=
\begin{pmatrix}
1 & 2 \\
k & 4 \\
\end{pmatrix}
$$

we have $\det A=4-2k$. The system has exactly one solution for every $b$ if and only if

$$
k\neq 2.
$$

For $k=2$ the system has either no solution or infinitely many solutions, depending on $b$. Examples:

- $b=(1,\ 2)^T$ gives infinitely many solutions;
- $b=(1,\ 3)^T$ gives no solution.

### Main steps

**1. The determinant.**

$$
\det A=1\cdot 4-2\cdot k=4-2k.
$$

**2. The case $k\neq 2$.** Then $\det A\neq 0$, so $A$ is invertible. For every right-hand side $b$ the equation $Ax=b$ has the solution $x=A^{-1}b$, and this solution is unique: if $Ax=b$ and $Ay=b$, then $A(x-y)=0$, and multiplying by $A^{-1}$ gives $x=y$. Explicitly,

$$
A^{-1}=\frac{1}{4-2k}
\begin{pmatrix}
4 & -2 \\
-k & 1 \\
\end{pmatrix}.
$$

**3. The case $k=2$.** Now $\det A=0$ and

$$
A=
\begin{pmatrix}
1 & 2 \\
2 & 4 \\
\end{pmatrix},
$$

where the second row is twice the first row. The system $Ax=b$ with $b=(b_1,\ b_2)^T$ reads

**System**

$$
\begin{cases}
x_1+2x_2=b_1, \\
2x_1+4x_2=b_2.
\end{cases}
$$

Subtract twice the first equation from the second:

$$
0=b_2-2b_1.
$$

- If $b_2=2b_1$, the second equation is a consequence of the first. The system reduces to one equation $x_1+2x_2=b_1$ with two unknowns, which has infinitely many solutions.
- If $b_2\neq 2b_1$, the system is contradictory and has no solution.

**4. An example with infinitely many solutions.** Take $b=(1,\ 2)^T$. Then $b_2=2b_1$, and the system is

$$
\begin{cases}
x_1+2x_2=1, \\
2x_1+4x_2=2.
\end{cases}
$$

The second equation is twice the first one. The solutions are $x_1=1-2s$, $x_2=s$ for every real $s$.

**5. An example with no solution.** Take $b=(1,\ 3)^T$. Then $b_2=3\neq 2=2b_1$, and the system is

$$
\begin{cases}
x_1+2x_2=1, \\
2x_1+4x_2=3.
\end{cases}
$$

Doubling the first equation gives $2x_1+4x_2=2$, which contradicts the second equation $2x_1+4x_2=3$. There is no solution.

### Property / method

For a square matrix $A$:

- if $\det A\neq 0$, the system $Ax=b$ has exactly one solution for every $b$;
- if $\det A=0$, the system never has exactly one solution: for each $b$ it has either no solution or infinitely many, and which case occurs depends on $b$.

### Verification

For $k=2$ and $b=(1,\ 2)^T$ the vector $x=(1,\ 0)^T$ (the case $s=0$) satisfies

$$
\begin{pmatrix}
1 & 2 \\
2 & 4 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
0 \\
\end{pmatrix}=
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix},
$$

and so does the vector $x=(-1,\ 1)^T$ (the case $s=1$):

$$
\begin{pmatrix}
1 & 2 \\
2 & 4 \\
\end{pmatrix}
\begin{pmatrix}
-1 \\
1 \\
\end{pmatrix}=
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}.
$$

Two different solutions confirm that the solution is not unique. For $k=0$, for instance, $\det A=4\neq 0$, and the system has a unique solution for every $b$.
