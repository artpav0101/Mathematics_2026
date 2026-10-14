## Exercise 8. Row Operations and Their Reversibility

```math
A=\begin{pmatrix}1 & 2 & -1\\2 & 4 & 1\\-1 & 1 & 3\end{pmatrix}
```

### Result

After the three operations:

```math
\begin{pmatrix}1 & 2 & -1\\0 & 3 & 2\\0 & 0 & 3\end{pmatrix}.
```

### Main steps

**Step 1:** $`R_2\leftarrow R_2-2R_1`$. The new row 2 is $`(2-2,\ 4-4,\ 1+2)=(0,0,3)`$.

```math
\begin{pmatrix}1 & 2 & -1\\0 & 0 & 3\\-1 & 1 & 3\end{pmatrix}
```

**Step 2:** $`R_3\leftarrow R_3+R_1`$. The new row 3 is $`(-1+1,\ 1+2,\ 3-1)=(0,3,2)`$.

```math
\begin{pmatrix}1 & 2 & -1\\0 & 0 & 3\\0 & 3 & 2\end{pmatrix}
```

**Step 3:** interchange $`R_2`$ and $`R_3`$.

```math
\begin{pmatrix}1 & 2 & -1\\0 & 3 & 2\\0 & 0 & 3\end{pmatrix}
```

### Reversing each operation

| Operation | Reverse operation |
|:----------|:------------------|
| $`R_2\leftarrow R_2-2R_1`$ | $`R_2\leftarrow R_2+2R_1`$ |
| $`R_3\leftarrow R_3+R_1`$ | $`R_3\leftarrow R_3-R_1`$ |
| $`R_2\leftrightarrow R_3`$ | $`R_2\leftrightarrow R_3`$ (a swap undoes itself) |

### Property / method

The three elementary row operations are replacement ($`R_i\leftarrow R_i+cR_j`$), scaling by $`c\neq0`$, and interchange. Each one is **reversible**, and the reverse is again an elementary operation. This is why row operations preserve the solution set of a linear system and why elimination is a safe procedure. To undo a sequence of operations, apply the reverses in the **opposite order**.

### Verification

Start from the final matrix and undo the steps in reverse order:

1. Swap $`R_2,R_3`$ gives $`\begin{pmatrix}1 & 2 & -1\\0 & 0 & 3\\0 & 3 & 2\end{pmatrix}`$.
2. $`R_3\leftarrow R_3-R_1`$: $`(0,3,2)-(1,2,-1)=(-1,1,3)`$.
3. $`R_2\leftarrow R_2+2R_1`$: $`(0,0,3)+(2,4,-2)=(2,4,1)`$.

This gives back exactly $`A`$. $`\checkmark`$

Determinant check: $`\det A=1(12-1)-2(6+1)+(-1)(2+4)=11-14-6=-9`$. Replacement operations do not change the determinant and one swap flips its sign, so the final matrix should have determinant $`+9`$. It is upper triangular with diagonal product $`1\cdot3\cdot3=9`$. $`\checkmark`$

---
