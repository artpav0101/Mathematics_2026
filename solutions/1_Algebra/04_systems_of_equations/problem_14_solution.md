# Exercise 14. A Small Change in the Right-Hand Side
 
## Question
 
Compare the systems
 
```math
\begin{cases}
x+y=2, \\
2x-y=1, \\
3x=3
\end{cases}
```
 
and
 
```math
\begin{cases}
x+y=2, \\
2x-y=1, \\
3x=3.1.
\end{cases}
```
 
Check the consistency of each system and explain why a small change in one number can change the type of the system.
 
> **Why this exercise:** shows the difference between a consistent and an inconsistent system without introducing new theory.
 
## Solution
 
Use a general right-hand side $c$ in the third equation and eliminate once:
 
```math
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
2 & -1 & 1 \\
3 & 0 & c
\end{array}\right)
\xrightarrow[R_3 - 3R_1]{R_2 - 2R_1}
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
0 & -3 & -3 \\
0 & -3 & c - 6
\end{array}\right)
\xrightarrow{R_3 - R_2}
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
0 & -3 & -3 \\
0 & 0 & c - 3
\end{array}\right)
```
 
**First system ($c = 3$):** last row $0 = 0$. From $-3y = -3$: $y = 1$, then $x = 1$.
Consistent, **unique solution $(1,1)$**. Check: $1+1 = 2$ ✓, $2-1 = 1$ ✓, $3\cdot1 = 3$ ✓.
 
**Second system ($c = 3.1$):** last row $0 = 0.1$ — a contradiction. **Inconsistent, no solution.**
Directly: the first two equations alone force $(x,y) = (1,1)$ (adding them gives $3x = 3$), but the third requires $x = \tfrac{3.1}{3} \approx 1.033$.
 
**Why a tiny change matters.** There are 3 equations but only 2 unknowns. The left side of equation 3 is the sum of the left sides of equations 1 and 2: $(x+y) + (2x - y) = 3x$. Hence the system can be consistent only if the right sides obey the same relation: $c = 2 + 1 = 3$. This is an **exact** condition — any deviation, however small, violates it.
 
Geometrically, the three equations are three lines in the plane. For $c = 3$ all three pass through the common point $(1,1)$. Changing $3$ to $3.1$ shifts the vertical line $x = 1$ to $x \approx 1.033$; the three lines now form a small triangle with no common point. Consistency of an over-determined system is a "knife-edge" property: it is not about how big the change is, but whether the required relation between right-hand sides holds exactly.
 
---
