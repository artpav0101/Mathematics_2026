# Exercise 15. Classifying Three Systems
 
## Question
 
For each of the following systems, perform only as much elimination as necessary to recognize its type:
 
**System 1**
 
```math
\begin{cases}
x+y=2, \\
x-y=0,
\end{cases}
```
 
**System 2**
 
```math
\begin{cases}
x+y=2, \\
2x+2y=4,
\end{cases}
```
 
**System 3**
 
```math
\begin{cases}
x+y=2, \\
2x+2y=5.
\end{cases}
```
 
For each, justify the classification: one solution, infinitely many solutions, or no solution.
 
> **Why this exercise:** brings together the three basic cases and requires recognizing them from the structure after elimination.
 
## Solution
 
One elimination step each is enough.
 
**System 1:**
 
```math
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
1 & -1 & 0
\end{array}\right)
\xrightarrow{R_2 - R_1}
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
0 & -2 & -2
\end{array}\right)
```
 
Two pivots for two unknowns, no contradictory row ⇒ **exactly one solution**. (Finishing: $y = 1$, $x = 1$; lines with slopes $-1$ and $1$ cross at $(1,1)$.)
 
**System 2:**
 
```math
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
2 & 2 & 4
\end{array}\right)
\xrightarrow{R_2 - 2R_1}
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
0 & 0 & 0
\end{array}\right)
```
 
Row $0 = 0$: consistent, only one pivot, $y$ free ⇒ **infinitely many solutions**, $(x,y) = (2 - s,\ s)$, $s\in\mathbb{R}$. (The second equation is the first multiplied by 2 — the same line.)
 
**System 3:**
 
```math
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
2 & 2 & 5
\end{array}\right)
\xrightarrow{R_2 - 2R_1}
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
0 & 0 & 1
\end{array}\right)
```
 
Row $0 = 1$: contradiction ⇒ **no solution**. (Parallel distinct lines $x+y=2$ and $x+y=2.5$.)
 
### Summary
 
| System | Echelon form shows | Type | Geometry |
|---|---|---|---|
| 1 | a pivot in every column | one solution | lines cross |
| 2 | zero row $0 = 0$, free variable | infinitely many | same line |
| 3 | row $0 = c$, $c \neq 0$ | none | parallel lines |
 
Systems 2 and 3 have the **same coefficient matrix**; their different types come only from the right-hand side — the same effect seen in Exercises 6 and 14.
