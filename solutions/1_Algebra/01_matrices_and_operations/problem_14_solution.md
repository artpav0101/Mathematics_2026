## Exercise 14. Rotation Matrices

### Result

For

$$
R(\theta)=
\begin{pmatrix}
\cos\theta & -\sin\theta \\
\sin\theta & \cos\theta \\
\end{pmatrix}
$$

the product of two rotation matrices is

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos(\alpha+\beta) & -\sin(\alpha+\beta) \\
\sin(\alpha+\beta) & \cos(\alpha+\beta) \\
\end{pmatrix}=R(\alpha+\beta).
$$

Geometrically, a rotation through $\beta$ followed by a rotation through $\alpha$ is a single rotation through $\alpha+\beta$.

### Main steps

**1. The product.** Each entry is the dot product of a row of $R(\alpha)$ with a column of $R(\beta)$:

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos\alpha & -\sin\alpha \\
\sin\alpha & \cos\alpha \\
\end{pmatrix}
\begin{pmatrix}
\cos\beta & -\sin\beta \\
\sin\beta & \cos\beta \\
\end{pmatrix}.
$$

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos\alpha\cos\beta-\sin\alpha\sin\beta & -\cos\alpha\sin\beta-\sin\alpha\cos\beta \\
\sin\alpha\cos\beta+\cos\alpha\sin\beta & -\sin\alpha\sin\beta+\cos\alpha\cos\beta \\
\end{pmatrix}.
$$

**2. The angle-sum formulas.**

$$
\begin{aligned}
\cos(\alpha+\beta) &= \cos\alpha\cos\beta-\sin\alpha\sin\beta, \\
\sin(\alpha+\beta) &= \sin\alpha\cos\beta+\cos\alpha\sin\beta.
\end{aligned}
$$

**3. Identification of the entries.**

- Position $(1,1)$: $\cos\alpha\cos\beta-\sin\alpha\sin\beta=\cos(\alpha+\beta)$.
- Position $(1,2)$: $-\cos\alpha\sin\beta-\sin\alpha\cos\beta=-(\sin\alpha\cos\beta+\cos\alpha\sin\beta)=-\sin(\alpha+\beta)$.
- Position $(2,1)$: $\sin\alpha\cos\beta+\cos\alpha\sin\beta=\sin(\alpha+\beta)$.
- Position $(2,2)$: $-\sin\alpha\sin\beta+\cos\alpha\cos\beta=\cos(\alpha+\beta)$.

**4. Conclusion.** Substituting these four values,

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos(\alpha+\beta) & -\sin(\alpha+\beta) \\
\sin(\alpha+\beta) & \cos(\alpha+\beta) \\
\end{pmatrix}=R(\alpha+\beta).
$$

### Geometric explanation

The matrix $R(\theta)$ rotates every vector of the plane about the origin through the angle $\theta$, counterclockwise for $\theta>0$. Its columns show where the basis vectors $e_1=(1,\ 0)^T$ and $e_2=(0,\ 1)^T$ go:

$$
R(\theta)e_1=
\begin{pmatrix}
\cos\theta \\
\sin\theta \\
\end{pmatrix},\qquad
R(\theta)e_2=
\begin{pmatrix}
-\sin\theta \\
\cos\theta \\
\end{pmatrix}.
$$

The product $R(\alpha)R(\beta)$ acts on a vector $v$ as $R(\alpha)\bigl(R(\beta)v\bigr)$: first rotate through $\beta$, then through $\alpha$. Two successive rotations about the same point add their angles, so the combined transformation is the rotation through $\alpha+\beta$, whose matrix is $R(\alpha+\beta)$.

For example, the vector $e_1$ lies at the angle $0$. After $R(\beta)$ it lies at the angle $\beta$, and after the further rotation $R(\alpha)$ it lies at the angle $\alpha+\beta$. Thus its image is $(\cos(\alpha+\beta),\ \sin(\alpha+\beta))^T$, which is exactly the first column of $R(\alpha+\beta)$.

In this sense the angle-sum formulas for sine and cosine are the algebraic form of the geometric fact that rotations compose by adding angles. Matrix multiplication and the geometry of the plane are consistent.

### Property / method

Composition of transformations corresponds to matrix multiplication. Rotations of the plane form a special family: the product of two of them is again a rotation, and the angles add. Since $\alpha+\beta=\beta+\alpha$, the result also shows that

$$
R(\alpha)R(\beta)=R(\beta)R(\alpha),
$$

so rotations about the same point commute, in contrast to general matrices.

### Verification

Take $\alpha=30^\circ$ and $\beta=60^\circ$. Then

$$
R(30^\circ)=
\begin{pmatrix}
\frac{\sqrt3}{2} & -\frac12 \\
\frac12 & \frac{\sqrt3}{2} \\
\end{pmatrix},\qquad
R(60^\circ)=
\begin{pmatrix}
\frac12 & -\frac{\sqrt3}{2} \\
\frac{\sqrt3}{2} & \frac12 \\
\end{pmatrix}.
$$

Their product is

$$
R(30^\circ)R(60^\circ)=
\begin{pmatrix}
\frac{\sqrt3}{4}-\frac{\sqrt3}{4} & -\frac34-\frac14 \\
\frac14+\frac34 & -\frac{\sqrt3}{4}+\frac{\sqrt3}{4} \\
\end{pmatrix}=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}=R(90^\circ),
$$

in agreement with $30^\circ+60^\circ=90^\circ$. Another check: two rotations through $90^\circ$ give

$$
R(90^\circ)R(90^\circ)=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
-1 & 0 \\
0 & -1 \\
\end{pmatrix}=R(180^\circ).
$$
