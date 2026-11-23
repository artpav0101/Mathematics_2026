# Exercise 9. A System from a Sum Condition
 
## Question
 
Find numbers $x,y$ satisfying
 
```math
x+y=10,\qquad 2x+5y=32.
```
 
Solve the system and explain geometrically why the solution is unique.
 
> **Why this exercise:** reinforces the transition from two linear conditions to the intersection point of two lines.
 
## Solution
 
```math
\left(\begin{array}{cc|c}
1 & 1 & 10 \\
2 & 5 & 32
\end{array}\right)
\xrightarrow{R_2 - 2R_1}
\left(\begin{array}{cc|c}
1 & 1 & 10 \\
0 & 3 & 12
\end{array}\right)
```
 
$3y = 12 \Rightarrow y = 4$; $x = 10 - 4 = 6$.
 
```math
\boxed{(x,y) = (6,\,4)}
```
 
Check: $6 + 4 = 10$ ✓, $2\cdot6 + 5\cdot4 = 12 + 20 = 32$ ✓.
 
**Geometric explanation.** Each equation is a line in the plane:
 
- $x + y = 10 \iff y = 10 - x$, slope $-1$;
- $2x + 5y = 32 \iff y = \tfrac{32}{5} - \tfrac25 x$, slope $-\tfrac25$.
The slopes differ, so the lines are not parallel; two non-parallel lines in a plane intersect in **exactly one point**, here $(6,4)$. Algebraically this shows up as two pivots after elimination, or $\det\begin{pmatrix}1&1\\2&5\end{pmatrix} = 5 - 2 = 3 \neq 0$.
 
---
