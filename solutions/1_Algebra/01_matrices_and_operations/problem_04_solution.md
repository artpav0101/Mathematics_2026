## Exercise 4. Matrix Multiplication and Noncommutativity

```math
A=\begin{pmatrix}1 & 2\\0 & 1\end{pmatrix},\qquad
B=\begin{pmatrix}2 & 0\\3 & 1\end{pmatrix}
```

### Result

```math
AB=\begin{pmatrix}8 & 2\\3 & 1\end{pmatrix},\qquad
BA=\begin{pmatrix}2 & 4\\3 & 7\end{pmatrix},\qquad AB\neq BA.
```

### Main steps

Entry $`(i,j)`$ of a product is (row $`i`$ of the left factor) $`\cdot`$ (column $`j`$ of the right factor).

```math
AB=\begin{pmatrix}1\cdot2+2\cdot3 & 1\cdot0+2\cdot1\\0\cdot2+1\cdot3 & 0\cdot0+1\cdot1\end{pmatrix}=\begin{pmatrix}8 & 2\\3 & 1\end{pmatrix}
```

```math
BA=\begin{pmatrix}2\cdot1+0\cdot0 & 2\cdot2+0\cdot1\\3\cdot1+1\cdot0 & 3\cdot2+1\cdot1\end{pmatrix}=\begin{pmatrix}2 & 4\\3 & 7\end{pmatrix}
```

### Property / method

Matrix multiplication is **not commutative**: in general $`AB\neq BA`$, even when both products exist and have the same size. Here the two products are different matrices. For numbers, $`ab=ba`$ always. For matrices, the order of the factors matters. (Matrix multiplication is still associative and distributes over addition.)

### Verification

- $`\det(AB)=8\cdot1-2\cdot3=2`$ and $`\det A\cdot\det B=1\cdot2=2`$. $`\checkmark`$
- $`\det(BA)=2\cdot7-4\cdot3=2`$. $`\checkmark`$ (The determinants agree, but the matrices do not.)
- Entry check: $`(AB)_{11}=8`$ but $`(BA)_{11}=2`$, so the matrices differ at least in this entry.

---
