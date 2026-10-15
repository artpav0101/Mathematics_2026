## Exercise 2. Addition and Scalar Multiplication
 
```math
A=\begin{pmatrix}1 & 2\\-1 & 3\end{pmatrix},\qquad
B=\begin{pmatrix}4 & -2\\0 & 5\end{pmatrix}
```
 
### Result
 
```math
A+B=\begin{pmatrix}5 & 0\\-1 & 8\end{pmatrix},\qquad
A-B=\begin{pmatrix}-3 & 4\\-1 & -2\end{pmatrix},\qquad
3A-2B=\begin{pmatrix}-5 & 10\\-3 & -1\end{pmatrix}.
```
 
### Main steps
 
Operations are done entry by entry.
 
```math
A+B=\begin{pmatrix}1+4 & 2+(-2)\\-1+0 & 3+5\end{pmatrix}=\begin{pmatrix}5 & 0\\-1 & 8\end{pmatrix}
```
 
```math
A-B=\begin{pmatrix}1-4 & 2-(-2)\\-1-0 & 3-5\end{pmatrix}=\begin{pmatrix}-3 & 4\\-1 & -2\end{pmatrix}
```
 
```math
3A=\begin{pmatrix}3 & 6\\-3 & 9\end{pmatrix},\qquad
2B=\begin{pmatrix}8 & -4\\0 & 10\end{pmatrix},\qquad
3A-2B=\begin{pmatrix}3-8 & 6+4\\-3-0 & 9-10\end{pmatrix}=\begin{pmatrix}-5 & 10\\-3 & -1\end{pmatrix}.
```
 
### Property / method
 
Addition and scalar multiplication are defined entrywise: $`(A+B)_{ij}=a_{ij}+b_{ij}`$ and $`(cA)_{ij}=c\,a_{ij}`$.
 
**Why the sizes must match.** The entry $`(i,j)`$ of $`A+B`$ is $`a_{ij}+b_{ij}`$. If $`A`$ and $`B`$ have different sizes, some position $`(i,j)`$ exists in one matrix but not in the other, so there is nothing to add. Addition is defined only when both matrices have the same number of rows and the same number of columns.
 
### Verification
 
- $`(A+B)+(A-B)=2A`$:
```math
\begin{pmatrix}5 & 0\\-1 & 8\end{pmatrix}+\begin{pmatrix}-3 & 4\\-1 & -2\end{pmatrix}=\begin{pmatrix}2 & 4\\-2 & 6\end{pmatrix}=2A.\ \checkmark
```
 
- Trace check: $`\mathrm{tr}(3A-2B)=3\mathrm{tr}A-2\mathrm{tr}B=3\cdot 4-2\cdot 9=-6`$, and the diagonal of the result gives $`-5+(-1)=-6`$. $`\checkmark`$
---
