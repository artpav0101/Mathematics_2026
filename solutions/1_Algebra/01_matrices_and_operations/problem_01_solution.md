## Exercise 1. Matrix Size and Entries
 
```math
A=\begin{pmatrix} 2 & -1 & 3 \\ 0 & 4 & 5 \end{pmatrix},\qquad
B=\begin{pmatrix} 1 & 0 \\ -2 & 3 \\ 4 & 1 \end{pmatrix}
```
 
### Result
 
- $`A`$ is $`2\times 3`$ and $`B`$ is $`3\times 2`$.
- $`a_{12}=-1`$, $`a_{23}=5`$, $`b_{21}=-2`$, $`b_{32}=1`$.
- Second row of $`A`$: $`(0,\ 4,\ 5)`$. First column of $`B`$: $`\begin{pmatrix}1\\-2\\4\end{pmatrix}`$.
### Main steps
 
1. **Sizes.** Count rows, then columns. $`A`$ has 2 rows and 3 columns. $`B`$ has 3 rows and 2 columns.
2. **Entries.** The entry $`x_{ij}`$ lies in row $`i`$ and column $`j`$:
   - $`a_{12}`$: row 1, column 2 of $`A`$ gives $`-1`$.
   - $`a_{23}`$: row 2, column 3 of $`A`$ gives $`5`$.
   - $`b_{21}`$: row 2, column 1 of $`B`$ gives $`-2`$.
   - $`b_{32}`$: row 3, column 2 of $`B`$ gives $`1`$.
3. **Row and column.**
```math
\text{row}_2(A)=\begin{pmatrix}0 & 4 & 5\end{pmatrix},\qquad
\text{col}_1(B)=\begin{pmatrix}1\\-2\\4\end{pmatrix}.
```
 
### Property / method
 
A matrix of size $`m\times n`$ has $`m`$ rows and $`n`$ columns (rows first). The index pair $`(i,j)`$ means "row $`i`$, column $`j`$". A row is a $`1\times n`$ matrix and a column is an $`m\times 1`$ matrix.
 
### Verification
 
- The row of $`A`$ has 3 entries, matching the 3 columns of $`A`$. The column of $`B`$ has 3 entries, matching the 3 rows of $`B`$.
- Entry counts: $`2\cdot 3=6`$ entries in $`A`$ and $`3\cdot 2=6`$ entries in $`B`$, as in the displayed arrays.
