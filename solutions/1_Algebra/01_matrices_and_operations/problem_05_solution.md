## Exercise 5. Matrix Times Vector

```math
A=\begin{pmatrix}2 & -1\\1 & 3\end{pmatrix},\qquad
x=\begin{pmatrix}4\\2\end{pmatrix}
```

### Result

```math
Ax=\begin{pmatrix}6\\10\end{pmatrix}=4\begin{pmatrix}2\\1\end{pmatrix}+2\begin{pmatrix}-1\\3\end{pmatrix}.
```

### Main steps

**Row-by-row:**

```math
Ax=\begin{pmatrix}2\cdot4+(-1)\cdot2\\1\cdot4+3\cdot2\end{pmatrix}=\begin{pmatrix}6\\10\end{pmatrix}.
```

**As a linear combination of columns.** Let $`a_1=\begin{pmatrix}2\\1\end{pmatrix}`$ and $`a_2=\begin{pmatrix}-1\\3\end{pmatrix}`$ be the columns of $`A`$. The coefficients are the entries of $`x`$:

```math
Ax=4a_1+2a_2=\begin{pmatrix}8\\4\end{pmatrix}+\begin{pmatrix}-2\\6\end{pmatrix}=\begin{pmatrix}6\\10\end{pmatrix}.
```

### Property / method

For $`A=\begin{pmatrix}a_1 & \cdots & a_n\end{pmatrix}`$ and $`x=(x_1,\dots,x_n)^T`$,

```math
Ax=x_1a_1+x_2a_2+\cdots+x_na_n .
```

So $`Ax`$ always lies in the span of the columns of $`A`$, and the entries of $`x`$ are the weights.

### Verification

The two computations (row-by-row and column combination) give the same vector $`(6,10)^T`$. $`\checkmark`$

---
