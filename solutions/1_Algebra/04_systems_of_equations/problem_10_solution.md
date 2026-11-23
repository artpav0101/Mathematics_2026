# Exercise 10. A Polynomial Through Three Points
 
## Question
 
Find a polynomial $p(x)=ax^2+bx+c$ whose graph passes through $(0,1)$, $(1,3)$, and $(2,9)$. Reduce the problem to a system of equations and check the result by substituting all three points.
 
> **Why this exercise:** shows that finding unknown coefficients can be reduced to solving a linear system.
 
## Solution
 
The condition "the graph passes through $(x_0, y_0)$" means $p(x_0) = y_0$. Here the unknowns are the coefficients $a, b, c$, and each condition is linear in them:
 
```math
\begin{cases}
p(0) = c = 1, \\
p(1) = a + b + c = 3, \\
p(2) = 4a + 2b + c = 9.
\end{cases}
\qquad
\left(\begin{array}{ccc|c}
0 & 0 & 1 & 1 \\
1 & 1 & 1 & 3 \\
4 & 2 & 1 & 9
\end{array}\right)
```
 
Substituting $c = 1$:
 
```math
\begin{cases}
a + b = 2, \\
4a + 2b = 8
\end{cases}
\xrightarrow{R_2 - 2R_1}
\begin{cases}
a + b = 2, \\
2a = 4
\end{cases}
```
 
So $a = 2$, $b = 0$, $c = 1$:
 
```math
\boxed{p(x) = 2x^2 + 1}
```
 
**Check:**
 
- $p(0) = 0 + 1 = 1$ ✓
- $p(1) = 2 + 1 = 3$ ✓
- $p(2) = 8 + 1 = 9$ ✓
The solution is unique because the three $x$-values are distinct (the coefficient matrix has three pivots), so exactly one parabola of this form passes through the three points.
 
---
