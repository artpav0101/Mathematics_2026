# Exercise 7. Choosing a Method Deliberately
 
## Question
 
Do not solve all of the following systems completely. For each situation, choose the method that best uses its structure and justify your choice:
 
1. one system with a triangular coefficient matrix
```math
\begin{cases}
2x-y=3, \\
4y=8;
\end{cases}
```
 
2. three systems $Ax=b_i$ with the same invertible matrix $A$, when $A^{-1}$ is already known;
3. one $3\times3$ system for which the inverse matrix is not given and the goal is only to find one solution vector.
For case 1, carry out the chosen method completely. For cases 2 and 3, describe the plan and indicate which part of the computation would be reusable or unnecessary. Do not judge a method by its name alone — refer to the number of right-hand sides and the structure of the matrix.
 
> **Why this exercise:** practices choosing a method based on the structure of the problem instead of solving another small system by two methods.
 
## Solution
 
### Case 1 — triangular matrix: back substitution
 
The coefficient matrix $\begin{pmatrix}2 & -1\\ 0 & 4\end{pmatrix}$ is already upper triangular, i.e. elimination has effectively been done. Any further elimination, computing an inverse, or using Cramer's rule would be wasted work. **Back substitution** is the natural choice:
 
- From $4y = 8$: $y = 2$.
- Substitute into $2x - y = 3$: $2x - 2 = 3 \Rightarrow x = \tfrac52$.
```math
\boxed{(x,y) = \left(\tfrac52,\ 2\right)}
```
 
Check: $2\cdot\tfrac52 - 2 = 5 - 2 = 3$ ✓, $4\cdot 2 = 8$ ✓.
 
### Case 2 — three right-hand sides, $A^{-1}$ known: multiply by the inverse
 
Plan: compute $x_i = A^{-1} b_i$ for $i = 1,2,3$ (or all at once as $A^{-1}\,[\,b_1\ b_2\ b_3\,]$).
 
- **Reusable:** $A^{-1}$ — the expensive part (essentially a full elimination on $A$) has already been paid for and serves all three right-hand sides.
- **Unnecessary:** any elimination on $A$. Each solution costs only one matrix–vector product (for an $n\times n$ matrix, $n^2$ multiplications; for $3\times 3$, just 9).
- Re-running Gaussian elimination three times would repeat the same row operations on $A$ three times for nothing.
### Case 3 — one system, no inverse given: Gaussian elimination
 
Plan: form the augmented matrix $(A \mid b)$, reduce to row echelon form, back-substitute.
 
- **Unnecessary:** computing $A^{-1}$. Finding the inverse means eliminating on $(A \mid I)$, i.e. solving three systems at once, to then use it for only one right-hand side — roughly three times the needed work. Cramer's rule needs four $3\times3$ determinants, also more than one elimination.
- **Nothing to reuse** here, since there is just one right-hand side; elimination done directly on $(A\mid b)$ gives the answer with the least work, and as a bonus it immediately reveals if the system is inconsistent or has free variables.
**Summary of the principle:** the cost that depends only on $A$ (elimination / inverse) is worth paying separately only when it is reused across several right-hand sides or is already available; special structure (triangular form) means part of that cost is already done.
 
---
