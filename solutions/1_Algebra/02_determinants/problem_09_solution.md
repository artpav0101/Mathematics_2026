## Question 

### Exercise 9. Area and the Determinant
The vectors

$$
u=
\begin{pmatrix}
3 \\
1 \\
\end{pmatrix},\qquad v=
\begin{pmatrix}
1 \\
4 \\
\end{pmatrix}
$$

span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.

> **Why this exercise:** gives the determinant a geometric interpretation and distinguishes its sign from the value of the area.

## Solution

The parallelogram spanned by

$$
u=
\begin{pmatrix}
3 \\
1 \\
\end{pmatrix},\qquad
v=
\begin{pmatrix}
1 \\
4 \\
\end{pmatrix}
$$

has area $11$. The determinant $\det(u\ v)=11$ for the order $u,v$ and $\det(v\ u)=-11$ for the reversed order. The sign changes; the area does not.

### Main steps

**1. The matrix of the two vectors.** Place $u$ and $v$ as columns:

$$
M=
\begin{pmatrix}
3 & 1 \\
1 & 4 \\
\end{pmatrix}.
$$

**2. The determinant.**

$$
\det M=3\cdot 4-1\cdot 1=12-1=11.
$$

**3. The area.** The area of the parallelogram spanned by $u$ and $v$ is the absolute value of this determinant:

$$
S=\lvert\det M\rvert=11.
$$

**4. Reversed order.** Now place $v$ first and $u$ second:

$$
M'=
\begin{pmatrix}
1 & 3 \\
4 & 1 \\
\end{pmatrix},\qquad
\det M'=1\cdot 1-3\cdot 4=1-12=-11.
$$

**5. What changes and what does not.** The matrix $M'$ is obtained from $M$ by swapping two columns, so the determinant changes sign: $\det M'=-\det M$. The parallelogram is the same set of points in the plane, so its area is still

$$
S=\lvert -11\rvert=11.
$$

### Property / method

For two vectors $u,v$ in the plane, $\lvert\det(u\ v)\rvert$ is the area of the parallelogram they span. The sign of $\det(u\ v)$ carries additional information: it is positive when the rotation from $u$ to $v$ (through the smaller angle) is counterclockwise, and negative when it is clockwise. Reversing the order of the vectors reverses this orientation, hence the sign, but not the shape of the parallelogram.

Here $\det(u\ v)=11>0$, so $v$ lies counterclockwise from $u$. Indeed, $u$ points at a small angle above the $x$-axis, while $v$ points at a much larger angle.

### Verification

The parallelogram has vertices $(0,0)$, $(3,1)$, $(4,5)$, $(1,4)$ where $(4,5)=u+v$. The diagonal from $P=(3,1)$ to $Q=(1,4)$ cuts it into two congruent triangles, one of which has vertices $O=(0,0)$, $P$, $Q$. Compute the area of this triangle by subtracting three corner right triangles from its bounding rectangle $[0,3]\times[0,4]$, whose area is $3\cdot 4=12$.

- The corner at $(3,0)$ has legs $3$ and $1$ and area $\frac12\cdot 3\cdot 1=1.5$.
- The corner at $(3,4)$ has legs $3$ and $2$ and area $\frac12\cdot 3\cdot 2=3$.
- The corner at $(0,4)$ has legs $4$ and $1$ and area $\frac12\cdot 4\cdot 1=2$.

The triangle area is $12-(1.5+3+2)=5.5$, so the parallelogram area is $2\cdot 5.5=11$. This agrees with $\lvert\det M\rvert$.
