# Exercise 6. A System with a Parameter — Which Cases Actually Occur?
 
## Question
 
Analyze, depending on the parameter $a$, the system
 
```math
\begin{cases}
x+y=2, \\
ax+ay=4.
\end{cases}
```
 
Among the three possibilities — exactly one solution, infinitely many solutions, no solution — determine which actually occur and for which values of $a$. If one type cannot occur, explain why.
 
> **Why this exercise:** teaches how to analyze a parameter without assuming in advance that all theoretically possible cases must occur in a specific system.
 
## Solution
 
```math
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
a & a & 4
\end{array}\right)
\xrightarrow{R_2 - aR_1}
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
0 & 0 & 4 - 2a
\end{array}\right)
```
 
(The step $R_2 - aR_1$ is valid for every $a$ — we never divide by $a$.)
 
The second row says $0 = 4 - 2a$.
 
| Case | Second row | Conclusion |
|---|---|---|
| $a = 2$ | $0 = 0$ | consistent, $y$ free ⇒ **infinitely many** solutions: $(x,y) = (2-s,\ s)$, $s\in\mathbb{R}$ |
| $a \neq 2$ (including $a = 0$) | $0 = 4-2a \neq 0$ | **no solution** |
 
Remark on $a = 0$: the second equation becomes $0 = 4$, a contradiction — it falls into the "no solution" case.
 
**"Exactly one solution" never occurs.** For every $a$, the second row of the coefficient matrix is $a$ times the first: $(a, a) = a\,(1,1)$. So elimination always produces a zero row on the left side, and at most one pivot is available for two unknowns. Equivalently,
 
```math
\det\begin{pmatrix}1 & 1\\ a & a\end{pmatrix} = a - a = 0 \quad\text{for all } a.
```
 
A unique solution would require two pivots (nonzero determinant), which is impossible here. Geometrically, both equations describe lines of slope $-1$ (when $a\neq 0$): they are either the same line ($a=2$) or parallel ($a\neq 2$), never crossing at a single point.
 
---
