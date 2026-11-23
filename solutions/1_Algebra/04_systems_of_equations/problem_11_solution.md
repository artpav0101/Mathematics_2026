# Exercise 11. A Parameter in a System of Three Equations
 
## Question
 
Analyze the number of solutions depending on $t$:
 
```math
\begin{cases}
x+y+z=1, \\
x+ty+z=2, \\
x+y+tz=3.
\end{cases}
```
 
Use elimination and separately analyze the parameter values for which a standard calculation step ceases to be valid.
 
> **Why this exercise:** develops parametric analysis while still relying only on elimination.
 
## Solution
 
```math
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 1 \\
1 & t & 1 & 2 \\
1 & 1 & t & 3
\end{array}\right)
\xrightarrow[R_3 - R_1]{R_2 - R_1}
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 1 \\
0 & t-1 & 0 & 1 \\
0 & 0 & t-1 & 2
\end{array}\right)
```
 
These steps are valid for all $t$ (the pivot used is the constant $1$). The matrix is already in echelon form, and the remaining step is to **divide by $t - 1$**, which is only allowed when $t \neq 1$.
 
### Case $t \neq 1$
 
```math
y = \frac{1}{t-1},\qquad z = \frac{2}{t-1},\qquad x = 1 - y - z = 1 - \frac{3}{t-1} = \frac{t-4}{t-1}.
```
 
Three pivots ⇒ **exactly one solution**:
 
```math
\boxed{(x,y,z) = \left(\frac{t-4}{t-1},\ \frac{1}{t-1},\ \frac{2}{t-1}\right)}
```
 
Spot check with $t = 2$: $(x,y,z) = (-2,\,1,\,2)$:
$-2+1+2 = 1$ ✓, $-2+2\cdot1+2 = 2$ ✓, $-2+1+2\cdot2 = 3$ ✓.
 
### Case $t = 1$ (the division step fails)
 
Substitute $t = 1$ into the echelon form instead of dividing:
 
```math
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 1 \\
0 & 0 & 0 & 1 \\
0 & 0 & 0 & 2
\end{array}\right)
```
 
Rows 2 and 3 say $0 = 1$ and $0 = 2$ — contradictions. **No solution.** (Directly: for $t=1$ all three equations have the same left side $x+y+z$ but different right sides $1, 2, 3$.)
 
### Summary
 
| $t$ | Number of solutions |
|---|---|
| $t \neq 1$ | exactly one |
| $t = 1$ | none |
 
The case "infinitely many solutions" **never occurs**: the only value that destroys pivots ($t=1$) simultaneously produces nonzero right-hand sides in the zero rows. (Consistently, $\det A = (t-1)^2$, which vanishes only at $t=1$.)
 
---
