## Exercise 10. Columns of a Matrix Product

```math
A=\begin{pmatrix}1 & 2 & 0\\0 & 1 & 1\end{pmatrix},\qquad
B=\begin{pmatrix}1 & 2\\-1 & 0\\3 & 1\end{pmatrix},\qquad
b_1=\begin{pmatrix}1\\-1\\3\end{pmatrix},\quad b_2=\begin{pmatrix}2\\0\\1\end{pmatrix}
```

### Result

```math
Ab_1=\begin{pmatrix}-1\\2\end{pmatrix},\qquad
Ab_2=\begin{pmatrix}2\\1\end{pmatrix},\qquad
AB=\begin{pmatrix}-1 & 2\\2 & 1\end{pmatrix}.
```

### Main steps

**1. The products $`Ab_1`$ and $`Ab_2`$.**

```math
Ab_1=\begin{pmatrix}1\cdot1+2\cdot(-1)+0\cdot3\\0\cdot1+1\cdot(-1)+1\cdot3\end{pmatrix}=\begin{pmatrix}-1\\2\end{pmatrix},\qquad
Ab_2=\begin{pmatrix}1\cdot2+2\cdot0+0\cdot1\\0\cdot2+1\cdot0+1\cdot1\end{pmatrix}=\begin{pmatrix}2\\1\end{pmatrix}.
```

**2. The product $`AB`$** ($`2\times3`$ times $`3\times2`$ gives $`2\times2`$), computed directly from rows of $`A`$ and columns of $`B`$:

```math
AB=\begin{pmatrix}
1\cdot1+2\cdot(-1)+0\cdot3 & 1\cdot2+2\cdot0+0\cdot1\\
0\cdot1+1\cdot(-1)+1\cdot3 & 0\cdot2+1\cdot0+1\cdot1
\end{pmatrix}=\begin{pmatrix}-1 & 2\\2 & 1\end{pmatrix}.
```

**3. Comparison.** The first column of $`AB`$ is $`(-1,2)^T=Ab_1`$ and the second column is $`(2,1)^T=Ab_2`$. So

```math
AB=\begin{pmatrix}Ab_1 & Ab_2\end{pmatrix}.
```

### Why the columns of $`AB`$ are $`Ab_1`$ and $`Ab_2`$

By definition, $`(AB)_{ij}=\sum_k a_{ik}b_{kj}`$. Fix $`j`$ and let $`i`$ run over the rows. The $`j`$-th column of $`AB`$ is then the vector with entries $`\sum_k a_{ik}b_{kj}`$, and these are precisely the entries of $`A`$ times the vector $`(b_{1j},\dots,b_{nj})^T`$, which is the $`j`$-th column $`b_j`$ of $`B`$. Hence

```math
\text{col}_j(AB)=A\,\text{col}_j(B).
```

Each column of $`B`$ is transformed by $`A`$ independently of the other columns.

### Property / method

Matrix multiplication can be viewed **column by column**: $`AB=A\begin{pmatrix}b_1&\cdots&b_p\end{pmatrix}=\begin{pmatrix}Ab_1&\cdots&Ab_p\end{pmatrix}`$. Combined with Exercise 5, each column of $`AB`$ is a linear combination of the columns of $`A`$ with weights taken from the matching column of $`B`$.

### Verification

Using the column-combination view for $`b_1=(1,-1,3)^T`$:

```math
Ab_1=1\begin{pmatrix}1\\0\end{pmatrix}-1\begin{pmatrix}2\\1\end{pmatrix}+3\begin{pmatrix}0\\1\end{pmatrix}=\begin{pmatrix}1-2+0\\0-1+3\end{pmatrix}=\begin{pmatrix}-1\\2\end{pmatrix}.\ \checkmark
```

The direct computation of $`AB`$ and the column-by-column computation agree. $`\checkmark`$





