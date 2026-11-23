# Exercise 13. Does Every Equation Add New Information?
 
## Question
 
Consider the system
 
```math
x_1+x_2=10,\qquad x_2+x_3=8,\qquad x_1-x_3=2.
```
 
Solve it and check whether all three equations are independently necessary to describe the solution set. If one follows from the others, show this by calculation.
 
> **Why this exercise:** teaches how to recognize redundant equations within a system.
 
## Solution
 
```math
\left(\begin{array}{ccc|c}
1 & 1 & 0 & 10 \\
0 & 1 & 1 & 8 \\
1 & 0 & -1 & 2
\end{array}\right)
\xrightarrow{R_3 - R_1}
\left(\begin{array}{ccc|c}
1 & 1 & 0 & 10 \\
0 & 1 & 1 & 8 \\
0 & -1 & -1 & -8
\end{array}\right)
\xrightarrow{R_3 + R_2}
\left(\begin{array}{ccc|c}
1 & 1 & 0 & 10 \\
0 & 1 & 1 & 8 \\
0 & 0 & 0 & 0
\end{array}\right)
```
 
The third row became $0 = 0$: the system is consistent and $x_3$ is free. Let $x_3 = t$:
 
- $x_2 = 8 - t$,
- $x_1 = 10 - x_2 = 2 + t$.
```math
\boxed{(x_1,x_2,x_3) = (2+t,\ 8-t,\ t),\quad t\in\mathbb{R}}
```
 
Check: $(2+t)+(8-t) = 10$ ✓; $(8-t)+t = 8$ ✓; $(2+t)-t = 2$ ✓.
 
**Redundancy.** The elimination steps show $R_3 - R_1 + R_2 = 0$, i.e. $R_3 = R_1 - R_2$. Explicitly:
 
```math
(x_1 + x_2) - (x_2 + x_3) = 10 - 8 \quad\Longrightarrow\quad x_1 - x_3 = 2,
```
 
which is exactly equation 3. So any $(x_1,x_2,x_3)$ satisfying equations 1 and 2 automatically satisfies equation 3. **The three equations are not independent**: only two of them carry information, and any two of them describe the same solution set (each equation is a combination of the other two, e.g. $R_1 = R_2 + R_3$, $R_2 = R_1 - R_3$). Removing one equation does not change the solution set.
 
---
