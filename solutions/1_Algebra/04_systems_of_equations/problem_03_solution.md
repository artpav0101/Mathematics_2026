# Exercise 3. Inconsistent System
 
## Question
 
Solve or show that the system is inconsistent:
 
```math
\begin{cases}
x+2y=3, \\
2x+4y=7.
\end{cases}
```
 
Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.
 
> **Why this exercise:** teaches how to recognize that a system has no solution without guessing.
 
## Solution
 
```math
\left(\begin{array}{cc|c}
1 & 2 & 3 \\
2 & 4 & 7
\end{array}\right)
\xrightarrow{R_2 - 2R_1}
\left(\begin{array}{cc|c}
1 & 2 & 3 \\
0 & 0 & 1
\end{array}\right)
```
 
The second row reads
 
```math
0\cdot x + 0\cdot y = 1 \quad\Longleftrightarrow\quad 0 = 1,
```
 
which is false for every choice of $x, y$. Hence **the system is inconsistent (no solution)**.
 
**Interpretation.** The left side of equation 2 is exactly twice the left side of equation 1: $2x+4y = 2(x+2y)$. If equation 1 held, then $2x+4y$ would have to equal $2\cdot 3 = 6$, but equation 2 demands $7$. The two conditions contradict each other.
 
Geometrically, both equations describe lines with slope $-\tfrac12$:
$y = \tfrac32 - \tfrac12 x$ and $y = \tfrac74 - \tfrac12 x$. They are **parallel and distinct**, so they never meet.
 
**General signal:** a row of the form $(0\ 0\ \cdots\ 0 \mid c)$ with $c \neq 0$ in the echelon form always means "no solution".
 
---
