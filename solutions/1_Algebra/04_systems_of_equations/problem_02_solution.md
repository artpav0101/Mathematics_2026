# Exercise 2. Gaussian Elimination — One Solution
 
## Question
 
Solve using Gaussian elimination:
 
```math
\begin{cases}
x+y+z=6, \\
2x-y+z=3, \\
x+2y-z=2.
\end{cases}
```
 
After solving, substitute the result into all equations and check consistency.
 
> **Why this exercise:** introduces the basic method for solving a system and builds the habit of checking the result.
 
## Solution
 
Augmented matrix:
 
```math
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
2 & -1 & 1 & 3 \\
1 & 2 & -1 & 2
\end{array}\right)
```
 
**Step 1** — eliminate $x$ below the first pivot: $R_2 - 2R_1 \to R_2$, $R_3 - R_1 \to R_3$:
 
```math
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & -3 & -1 & -9 \\
0 & 1 & -2 & -4
\end{array}\right)
```
 
**Step 2** — swap $R_2 \leftrightarrow R_3$ (to get pivot $1$):
 
```math
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & 1 & -2 & -4 \\
0 & -3 & -1 & -9
\end{array}\right)
```
 
**Step 3** — $R_3 + 3R_2 \to R_3$:
 
```math
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & 1 & -2 & -4 \\
0 & 0 & -7 & -21
\end{array}\right)
```
 
**Back substitution:**
 
- $-7z = -21 \Rightarrow z = 3$,
- $y - 2z = -4 \Rightarrow y = -4 + 6 = 2$,
- $x + y + z = 6 \Rightarrow x = 6 - 2 - 3 = 1$.
```math
\boxed{(x,y,z) = (1,\,2,\,3)}
```
 
**Check:**
 
| Equation | Left side | Right side |
|---|---|---|
| $x+y+z$ | $1+2+3=6$ | $6$ ✓ |
| $2x-y+z$ | $2-2+3=3$ | $3$ ✓ |
| $x+2y-z$ | $1+4-3=2$ | $2$ ✓ |
 
All three equations hold, so the system is consistent with the unique solution $(1,2,3)$.
 
---
