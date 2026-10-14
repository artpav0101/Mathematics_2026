## Exercise 7. Identity Matrix, Zero Matrix, and Powers

```math
A=\begin{pmatrix}2 & 1\\0 & 2\end{pmatrix}
```

### Result

```math
AI=IA=A,\qquad A+0=A,\qquad
A^2=\begin{pmatrix}4 & 4\\0 & 4\end{pmatrix},\qquad
A^3=\begin{pmatrix}8 & 12\\0 & 8\end{pmatrix}.
```

### Main steps

With $`I=\begin{pmatrix}1&0\\0&1\end{pmatrix}`$ and $`0=\begin{pmatrix}0&0\\0&0\end{pmatrix}`$:

```math
AI=\begin{pmatrix}2\cdot1+1\cdot0 & 2\cdot0+1\cdot1\\0\cdot1+2\cdot0 & 0\cdot0+2\cdot1\end{pmatrix}=A,\qquad
IA=A,\qquad A+0=A.
```

```math
A^2=A\cdot A=\begin{pmatrix}2\cdot2+1\cdot0 & 2\cdot1+1\cdot2\\0\cdot2+2\cdot0 & 0\cdot1+2\cdot2\end{pmatrix}=\begin{pmatrix}4 & 4\\0 & 4\end{pmatrix}
```

```math
A^3=A^2A=\begin{pmatrix}4 & 4\\0 & 4\end{pmatrix}\begin{pmatrix}2 & 1\\0 & 2\end{pmatrix}=\begin{pmatrix}8 & 4+8\\0 & 8\end{pmatrix}=\begin{pmatrix}8 & 12\\0 & 8\end{pmatrix}
```

### Property / method

- $`I`$ is the **multiplicative identity**: $`AI=IA=A`$ (it plays the role of the number $`1`$).
- $`0`$ is the **additive identity**: $`A+0=A`$ (it plays the role of the number $`0`$).

**Pattern in the powers.** The diagonal entries are $`2,4,8`$, that is $`2^n`$. The upper-right entries are $`1,4,12`$, that is $`n\cdot2^{n-1}`$. So

```math
A^n=\begin{pmatrix}2^n & n\,2^{n-1}\\0 & 2^n\end{pmatrix}.
```

**Why.** Write $`A=2I+N`$ with $`N=\begin{pmatrix}0&1\\0&0\end{pmatrix}`$. Then $`N^2=0`$, and $`2I`$ commutes with $`N`$, so the binomial theorem leaves only two terms:

```math
A^n=(2I+N)^n=2^nI+n\,2^{n-1}N .
```

### Verification

- The formula gives $`A^1=\begin{pmatrix}2&1\\0&2\end{pmatrix}`$, $`A^2=\begin{pmatrix}4&4\\0&4\end{pmatrix}`$, $`A^3=\begin{pmatrix}8&12\\0&8\end{pmatrix}`$. $`\checkmark`$
- Alternative order: $`AA^2=\begin{pmatrix}2&1\\0&2\end{pmatrix}\begin{pmatrix}4&4\\0&4\end{pmatrix}=\begin{pmatrix}8&12\\0&8\end{pmatrix}`$. $`\checkmark`$
- $`\det(A^3)=64=(\det A)^3=4^3`$. $`\checkmark`$

---
