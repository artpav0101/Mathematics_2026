## Exercise 9. Composing Transformations

```math
S=\begin{pmatrix}2 & 0\\0 & 1\end{pmatrix},\qquad
R=\begin{pmatrix}0 & -1\\1 & 0\end{pmatrix},\qquad
x=\begin{pmatrix}1\\2\end{pmatrix}
```

### Result

```math
RSx=\begin{pmatrix}-2\\2\end{pmatrix},\qquad
SRx=\begin{pmatrix}-4\\1\end{pmatrix},\qquad RSx\neq SRx.
```

### Main steps

**$`RSx`$ (scale first, then rotate).** In $`RSx=R(Sx)`$ the matrix closest to $`x`$ acts first.

```math
Sx=\begin{pmatrix}2\\2\end{pmatrix},\qquad
R(Sx)=\begin{pmatrix}0\cdot2-1\cdot2\\1\cdot2+0\cdot2\end{pmatrix}=\begin{pmatrix}-2\\2\end{pmatrix}.
```

**$`SRx`$ (rotate first, then scale).**

```math
Rx=\begin{pmatrix}0\cdot1-1\cdot2\\1\cdot1+0\cdot2\end{pmatrix}=\begin{pmatrix}-2\\1\end{pmatrix},\qquad
S(Rx)=\begin{pmatrix}-4\\1\end{pmatrix}.
```

### Geometric explanation

- $`S`$ stretches the plane by a factor of 2 in the $`x`$-direction only.
- $`R`$ rotates the plane by $`90^\circ`$ counterclockwise.

If you **stretch first**, the stretched direction is then rotated: the horizontal stretch ends up as a *vertical* stretch. If you **rotate first**, the horizontal stretch is applied *after* the rotation, so it stays horizontal.

Test on the basis vectors:

| Vector | $`RS`$ (scale, then rotate) | $`SR`$ (rotate, then scale) |
|:------:|:-------------------------:|:-------------------------:|
| $`e_1=(1,0)`$ | $`(0,2)`$ | $`(0,1)`$ |
| $`e_2=(0,1)`$ | $`(-1,0)`$ | $`(-2,0)`$ |

Under $`RS`$ the unit circle becomes an ellipse that is long in the vertical direction. Under $`SR`$ it becomes an ellipse that is long in the horizontal direction. These are different transformations, so the order matters.

### Property / method

The product $`RS`$ represents "first $`S`$, then $`R`$": $`(RS)x=R(Sx)`$. Composition of transformations corresponds to matrix multiplication, and since $`RS\neq SR`$ in general, the order of composition matters.

### Verification

Compute the products directly:

```math
RS=\begin{pmatrix}0 & -1\\2 & 0\end{pmatrix},\qquad
SR=\begin{pmatrix}0 & -2\\1 & 0\end{pmatrix}.
```

```math
RSx=\begin{pmatrix}0\cdot1-1\cdot2\\2\cdot1+0\cdot2\end{pmatrix}=\begin{pmatrix}-2\\2\end{pmatrix},\qquad
SRx=\begin{pmatrix}0\cdot1-2\cdot2\\1\cdot1+0\cdot2\end{pmatrix}=\begin{pmatrix}-4\\1\end{pmatrix}.\ \checkmark
```

---
