# Exercise 4. Infinitely Many Solutions
 
## Question
 
Solve
 
```math
\begin{cases}
x+y+z=2, \\
2x+2y+2z=4, \\
x-y+z=0.
\end{cases}
```
 
Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point really satisfies the system.
 
> **Why this exercise:** shows the case of multiple solutions and teaches a simple parametric description.
 
## Solution
 
```math
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 2 \\
2 & 2 & 2 & 4 \\
1 & -1 & 1 & 0
\end{array}\right)
\xrightarrow[R_3 - R_1]{R_2 - 2R_1}
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 2 \\
0 & 0 & 0 & 0 \\
0 & -2 & 0 & -2
\end{array}\right)
\xrightarrow{R_2 \leftrightarrow R_3}
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 2 \\
0 & -2 & 0 & -2 \\
0 & 0 & 0 & 0
\end{array}\right)
```
 
The row $0 = 0$ carries no information (equation 2 is just twice equation 1).
Pivots are in the columns of $x$ and $y$; the column of $z$ has no pivot, so **$z$ is the free variable**. Let $z = t$, $t \in \mathbb{R}$.
 
- $-2y = -2 \Rightarrow y = 1$,
- $x + y + z = 2 \Rightarrow x = 2 - 1 - t = 1 - t$.
```math
\boxed{(x,y,z) = (1-t,\ 1,\ t),\quad t\in\mathbb{R}}
\qquad\text{equivalently}\qquad
\begin{pmatrix}x\\y\\z\end{pmatrix} = \begin{pmatrix}1\\1\\0\end{pmatrix} + t\begin{pmatrix}-1\\0\\1\end{pmatrix}.
```
 
The solution set is a line in $\mathbb{R}^3$: infinitely many solutions.
 
**Check for $t = 2$:** the point is $(-1,\,1,\,2)$.
 
- $x+y+z = -1+1+2 = 2$ ✓
- $2x+2y+2z = -2+2+4 = 4$ ✓
- $x-y+z = -1-1+2 = 0$ ✓
---
