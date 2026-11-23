# Exercise 12. Homogeneous System
 
## Question
 
Solve
 
```math
\begin{cases}
x+2y-z=0, \\
2x+4y-2z=0, \\
x-y+2z=0.
\end{cases}
```
 
Give all solutions in parametric form and explain why $(0,0,0)$ always satisfies a homogeneous system.
 
> **Why this exercise:** shows the special case of a system with a zero right-hand side without introducing additional theory.
 
## Solution
 
For a homogeneous system the right-hand column stays $0$ under all row operations, so we may reduce just $A$:
 
```math
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & -2 \\
1 & -1 & 2
\end{pmatrix}
\xrightarrow[R_3 - R_1]{R_2 - 2R_1}
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 0 \\
0 & -3 & 3
\end{pmatrix}
\xrightarrow{R_2\leftrightarrow R_3}
\begin{pmatrix}
1 & 2 & -1 \\
0 & -3 & 3 \\
0 & 0 & 0
\end{pmatrix}
```
 
Two pivots (columns of $x$, $y$), three unknowns ⇒ one free variable, $z = s$.
 
- $-3y + 3s = 0 \Rightarrow y = s$,
- $x + 2s - s = 0 \Rightarrow x = -s$.
```math
\boxed{(x,y,z) = (-s,\ s,\ s) = s\,(-1,\,1,\,1),\quad s\in\mathbb{R}}
```
 
The solution set is a line through the origin.
 
**Check (general $s$):**
$-s + 2s - s = 0$ ✓; $-2s + 4s - 2s = 0$ ✓; $-s - s + 2s = 0$ ✓.
 
**Why $(0,0,0)$ always works.** In a homogeneous system every equation has the form $a_1x_1 + \dots + a_nx_n = 0$. Putting all unknowns equal to $0$ makes every term $a_i\cdot 0 = 0$, so each left side is $0$, matching the right side. In matrix form: $A\mathbf{0} = \mathbf{0}$ for every matrix $A$. Consequently, a homogeneous system is **never inconsistent** — it has either only the trivial solution or infinitely many (as here, $s = 0$ gives the trivial one).
 
---
