# Exercise 8. Two Systems with the Same Coefficient Matrix
 
## Question
 
Solve by elimination the two systems
 
```math
\begin{cases}
2x+y=5, \\
x-y=1,
\end{cases}
```
 
```math
\begin{cases}
2x+y=1, \\
x-y=4.
\end{cases}
```
 
Compare the successive elimination steps. Which part of the calculation is the same in both cases, and why?
 
> **Why this exercise:** shows the role of the coefficient matrix independently of the right-hand side.
 
## Solution
 
Both systems have $A = \begin{pmatrix}2 & 1\\ 1 & -1\end{pmatrix}$; only $b$ differs: $b_1 = (5,1)^T$, $b_2 = (1,4)^T$. We use the same row operations for both: first $R_1 \leftrightarrow R_2$ (pivot $1$), then $R_2 - 2R_1 \to R_2$.
 
**System 1:**
 
```math
\left(\begin{array}{cc|c}
2 & 1 & 5 \\
1 & -1 & 1
\end{array}\right)
\xrightarrow{R_1\leftrightarrow R_2}
\left(\begin{array}{cc|c}
1 & -1 & 1 \\
2 & 1 & 5
\end{array}\right)
\xrightarrow{R_2-2R_1}
\left(\begin{array}{cc|c}
1 & -1 & 1 \\
0 & 3 & 3
\end{array}\right)
```
 
$3y = 3 \Rightarrow y = 1$; $x = 1 + y = 2$. **Solution $(2,\,1)$.**
Check: $2\cdot2+1 = 5$ ✓, $2-1 = 1$ ✓.
 
**System 2:**
 
```math
\left(\begin{array}{cc|c}
2 & 1 & 1 \\
1 & -1 & 4
\end{array}\right)
\xrightarrow{R_1\leftrightarrow R_2}
\left(\begin{array}{cc|c}
1 & -1 & 4 \\
2 & 1 & 1
\end{array}\right)
\xrightarrow{R_2-2R_1}
\left(\begin{array}{cc|c}
1 & -1 & 4 \\
0 & 3 & -7
\end{array}\right)
```
 
$3y = -7 \Rightarrow y = -\tfrac73$; $x = 4 + y = \tfrac53$. **Solution $\left(\tfrac53,\,-\tfrac73\right)$.**
Check: $2\cdot\tfrac53 - \tfrac73 = \tfrac{10-7}{3} = 1$ ✓, $\tfrac53 + \tfrac73 = 4$ ✓.
 
**Comparison.**
 
- The choice of row operations (the swap, the multiplier $2$) and the resulting left part $\begin{pmatrix}1 & -1\\ 0 & 3\end{pmatrix}$ are **identical** in both cases.
- Only the right-hand column changes: $(1,5)\to(1,3)$ versus $(4,1)\to(4,-7)$.
**Why:** the multipliers are chosen to create zeros in the coefficient matrix, so they depend only on $A$, never on $b$. The right-hand side is just carried along. Therefore both systems can be solved in one pass:
 
```math
\left(\begin{array}{cc|cc}
2 & 1 & 5 & 1 \\
1 & -1 & 1 & 4
\end{array}\right)
\longrightarrow
\left(\begin{array}{cc|cc}
1 & -1 & 1 & 4 \\
0 & 3 & 3 & -7
\end{array}\right).
```
 
This is exactly the idea behind reusing a factorization (or an inverse) for many right-hand sides.
 
---
