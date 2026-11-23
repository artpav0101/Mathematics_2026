# Exercise 1. From a System to a Matrix
 
## Question
 
Write the system
 
```math
\begin{cases}
2x-y+z=4, \\
x+3y-2z=1, \\
3x+y+z=7.
\end{cases}
```
 
in the form $Ax=b$.
Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.
 
> **Why this exercise:** teaches how to move between a system of equations and matrix notation.
 
## Solution
 
**Coefficient matrix** (row $i$ holds the coefficients of $x, y, z$ in equation $i$, in that order):
 
```math
A=\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1
\end{pmatrix}
```
 
**Vector of unknowns** and **right-hand side**:
 
```math
\mathbf{x}=\begin{pmatrix} x \\ y \\ z \end{pmatrix},
\qquad
b=\begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}.
```
 
So the system is
 
```math
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1
\end{pmatrix}
\begin{pmatrix} x \\ y \\ z \end{pmatrix}
=
\begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}.
```
 
**Why rows correspond to equations.** The product $A\mathbf{x}$ is computed row by row: entry $i$ of $A\mathbf{x}$ is (row $i$ of $A$) $\cdot\ \mathbf{x}$. For example,
 
- row 1: $(2,-1,1)\cdot(x,y,z) = 2x - y + z$, and setting it equal to $b_1 = 4$ gives equation 1;
- row 2: $(1,3,-2)\cdot(x,y,z) = x + 3y - 2z = 1$, equation 2;
- row 3: $(3,1,1)\cdot(x,y,z) = 3x + y + z = 7$, equation 3.
Each **column** of $A$ belongs to one unknown (column 1 ↔ $x$, column 2 ↔ $y$, column 3 ↔ $z$). A missing variable would appear as a $0$ in its column.
 
The augmented matrix is
 
```math
\left(\begin{array}{ccc|c}
2 & -1 & 1 & 4 \\
1 & 3 & -2 & 1 \\
3 & 1 & 1 & 7
\end{array}\right).
```
 
---
