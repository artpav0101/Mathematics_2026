### Exercise 1. From a System to a Matrix
Write the system

$$
\begin{cases}
2x-y+z=4, \\
x+3y-2z=1, \\
3x+y+z=7.
\end{cases}
$$

in the form $Ax=b$.
Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.

> **Why this exercise:** teaches how to move between a system of equations and matrix notation.

#### Solution

**Step 1: Read off the coefficients.**
Write the coefficients of $x$, $y$, $z$ in each equation (a missing or implicit coefficient is $1$, a minus sign gives $-1$):

| Equation | coeff. of $x$ | coeff. of $y$ | coeff. of $z$ | right-hand side |
|---|---|---|---|---|
| 1 | $2$ | $-1$ | $1$ | $4$ |
| 2 | $1$ | $3$ | $-2$ | $1$ |
| 3 | $3$ | $1$ | $1$ | $7$ |

**Step 2: Assemble the objects.**

- Coefficient matrix:
$$
A=\begin{pmatrix}
2 & -1 & 1\\
1 & 3 & -2\\
3 & 1 & 1
\end{pmatrix}
$$

- Vector of unknowns:
$$
x=\begin{pmatrix}x\\ y\\ z\end{pmatrix}
$$

- Right-hand side vector:
$$
b=\begin{pmatrix}4\\ 1\\ 7\end{pmatrix}
$$

**Step 3: The system in matrix form.**

$$
\begin{pmatrix}
2 & -1 & 1\\
1 & 3 & -2\\
3 & 1 & 1
\end{pmatrix}
\begin{pmatrix}x\\ y\\ z\end{pmatrix}
=
\begin{pmatrix}4\\ 1\\ 7\end{pmatrix},
\qquad\text{i.e.}\qquad Ax=b.
$$

**Step 4: Rows correspond to equations.**
The $i$-th entry of $Ax$ is the dot product of the $i$-th row of $A$ with the vector of unknowns:

$$
\begin{aligned}
\text{Row 1: } & (2,-1,1)\cdot(x,y,z)=2x-y+z=4,\\
\text{Row 2: } & (1,3,-2)\cdot(x,y,z)=x+3y-2z=1,\\
\text{Row 3: } & (3,1,1)\cdot(x,y,z)=3x+y+z=7.
\end{aligned}
$$

So multiplying out $Ax$ and setting it equal to $b$ entry by entry returns exactly the original three equations: row $i$ of $A$ holds the coefficients of equation $i$, and entry $i$ of $b$ is its right-hand side. Columns correspond to unknowns: column 1 holds all coefficients of $x$, column 2 of $y$, column 3 of $z$.

**Answer:** $Ax=b$ with $A$, $x$, $b$ as above.
