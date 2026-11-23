# Exercise 5. Row Echelon Form and Number of Solutions
 
## Question
 
For the augmented matrix
 
```math
\left(\begin{array}{ccc|c}
1 & 2 & -1 & 3 \\
0 & 1 & 2 & 1 \\
0 & 0 & 0 & 0
\end{array}\right)
```
 
determine the number of solutions and write them in parametric form. Explain how you know how many variables may be chosen freely.
 
> **Why this exercise:** teaches how to read information about solutions directly from row echelon form.
 
## Solution
 
Let the unknowns be $x_1, x_2, x_3$.
 
- There is **no** row of the form $(0\ 0\ 0 \mid c)$ with $c\neq 0$, so the system is **consistent**.
- Pivots are in columns 1 and 2 ⇒ $x_1, x_2$ are pivot (basic) variables.
- Column 3 has no pivot ⇒ $x_3$ is free.
```math
\#\text{free variables} = \#\text{unknowns} - \#\text{pivots} = 3 - 2 = 1.
```
 
Since at least one variable is free and the system is consistent, there are **infinitely many solutions**.
 
Let $x_3 = t$:
 
- Row 2: $x_2 + 2t = 1 \Rightarrow x_2 = 1 - 2t$,
- Row 1: $x_1 + 2(1-2t) - t = 3 \Rightarrow x_1 = 3 - 2 + 4t + t = 1 + 5t$.
```math
\boxed{(x_1,x_2,x_3) = (1+5t,\ 1-2t,\ t),\quad t\in\mathbb{R}}
\qquad
\begin{pmatrix}x_1\\x_2\\x_3\end{pmatrix} = \begin{pmatrix}1\\1\\0\end{pmatrix} + t\begin{pmatrix}5\\-2\\1\end{pmatrix}.
```
 
**Check (general $t$):** row 1: $(1+5t) + 2(1-2t) - t = 1 + 2 + 5t - 4t - t = 3$ ✓; row 2: $(1-2t) + 2t = 1$ ✓.
 
**Why exactly one free variable:** each nonzero row of the echelon form "uses up" one unknown by fixing a pivot variable in terms of the variables to its right. Two independent equations fix two of the three unknowns; the remaining one can be chosen arbitrarily.
 
---
