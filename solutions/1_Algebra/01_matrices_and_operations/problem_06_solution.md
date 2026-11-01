## Exercise 6. Transpose

```math
A=\begin{pmatrix}1 & 2 & 3\\4 & 5 & 6\end{pmatrix},\qquad
B=\begin{pmatrix}1 & 0\\2 & 1\\-1 & 3\end{pmatrix}
```

### Result

```math
A^T=\begin{pmatrix}1 & 4\\2 & 5\\3 & 6\end{pmatrix},\qquad
B^T=\begin{pmatrix}1 & 2 & -1\\0 & 1 & 3\end{pmatrix},\qquad
AB=\begin{pmatrix}2 & 11\\8 & 23\end{pmatrix}.
```

### Main steps

Transposing swaps rows and columns: $`(A^T)_{ij}=a_{ji}`$.

Product $`AB`$ (a $`2\times3`$ times a $`3\times2`$ gives $`2\times2`$):

```math
AB=\begin{pmatrix}
1\cdot1+2\cdot2+3\cdot(-1) & 1\cdot0+2\cdot1+3\cdot3\\
4\cdot1+5\cdot2+6\cdot(-1) & 4\cdot0+5\cdot1+6\cdot3
\end{pmatrix}=\begin{pmatrix}2 & 11\\8 & 23\end{pmatrix}.
```

Left side:

```math
(AB)^T=\begin{pmatrix}2 & 8\\11 & 23\end{pmatrix}.
```

Right side ($`B^T`$ is $`2\times3`$, $`A^T`$ is $`3\times2`$, so the product is $`2\times2`$):

```math
B^TA^T=\begin{pmatrix}
1\cdot1+2\cdot2+(-1)\cdot3 & 1\cdot4+2\cdot5+(-1)\cdot6\\
0\cdot1+1\cdot2+3\cdot3 & 0\cdot4+1\cdot5+3\cdot6
\end{pmatrix}=\begin{pmatrix}2 & 8\\11 & 23\end{pmatrix}.
```

### Property / method

```math
(AB)^T=B^TA^T
```

The transpose **reverses the order** of the factors. The reason is that entry $`(i,j)`$ of $`(AB)^T`$ is $`(AB)_{ji}=\sum_k a_{jk}b_{ki}`$. This equals $`\sum_k (B^T)_{ik}(A^T)_{kj}`$, which is entry $`(i,j)`$ of $`B^TA^T`$.

### Verification

$`(AB)^T=\begin{pmatrix}2 & 8\\11 & 23\end{pmatrix}=B^TA^T`$. $`\checkmark`$

---
