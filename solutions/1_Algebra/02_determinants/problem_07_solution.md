## Question

### Exercise 7. Using Properties Instead of Recomputing
Suppose that for a $3\times3$ matrix, $\det A=-4$. Compute

$$
\det(2A),\qquad \det(A^T),\qquad \det(A^2),\qquad \det(-A).
$$

Justify each answer using the appropriate property.

> **Why this exercise:** teaches how to use determinant properties instead of repeating a full calculation.

## Solution

For a $3\times3$ matrix $A$ with $\det A=-4$:

$$
\det(2A)=-32,\qquad
\det(A^T)=-4,\qquad
\det(A^2)=16,\qquad
\det(-A)=4.
$$

### Main steps

The matrix $A$ has size $n=3$ and $\det A=-4$.

**1. $\det(2A)$.** Multiplying the whole matrix by a number $c$ multiplies each of the $n$ rows by $c$. Each row multiplication multiplies the determinant by $c$, so

$$
\det(cA)=c^n\det A.
$$

With $c=2$ and $n=3$:

$$
\det(2A)=2^3\cdot(-4)=8\cdot(-4)=-32.
$$

**2. $\det(A^T)$.** Transposition does not change the determinant:

$$
\det(A^T)=\det A=-4.
$$

**3. $\det(A^2)$.** The determinant of a product is the product of the determinants:

$$
\det(A^2)=\det(A\cdot A)=\det A\cdot\det A=(-4)^2=16.
$$

**4. $\det(-A)$.** This is the case $c=-1$ of the rule in step 1:

$$
\det(-A)=(-1)^3\det A=-(-4)=4.
$$

### Property / method

The properties used, for $n\times n$ matrices:

- $\det(cA)=c^n\det A$ (each of the $n$ rows is multiplied by $c$);
- $\det(A^T)=\det A$;
- $\det(AB)=\det A\cdot\det B$;
- in particular $\det(A^k)=(\det A)^k$.

A common mistake is to write $\det(2A)=2\det A$. This is wrong for $n\geq 2$: the factor $2$ appears once for every row.

### Verification

Take the diagonal matrix $D=\mathrm{diag}(-4,\ 1,\ 1)$, which is $3\times3$ and has $\det D=-4$. Then:

- $2D=\mathrm{diag}(-8,\ 2,\ 2)$ has determinant $-8\cdot 2\cdot 2=-32$;
- $D^T=D$ has determinant $-4$;
- $D^2=\mathrm{diag}(16,\ 1,\ 1)$ has determinant $16$;
- $-D=\mathrm{diag}(4,\ -1,\ -1)$ has determinant $4\cdot(-1)\cdot(-1)=4$.

All four values agree with the results above.
