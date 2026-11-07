## Question 

### Exercise 11. When Do Matrices Commute?
Given

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}.
$$

Find the conditions on $a,b,c,d$ under which $AB=BA$. Describe the general form of all such matrices $B$.

> **Why this exercise:** deepens the idea of noncommutativity by finding the conditions under which commutativity does hold.

## Solution

For

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad
B=
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}
$$

the equality $AB=BA$ holds if and only if

$$
c=0,\qquad d=a,
$$

with $a$ and $b$ arbitrary. The general form of all such matrices is

$$
B=
\begin{pmatrix}
a & b \\
0 & a \\
\end{pmatrix}=aI+b
\begin{pmatrix}
0 & 1 \\
0 & 0 \\
\end{pmatrix}.
$$

### Main steps

**1. The product $AB$.** Each entry is the dot product of a row of $A$ with a column of $B$:

$$
AB=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot a+1\cdot c & 1\cdot b+1\cdot d \\
0\cdot a+1\cdot c & 0\cdot b+1\cdot d \\
\end{pmatrix}=
\begin{pmatrix}
a+c & b+d \\
c & d \\
\end{pmatrix}.
$$

**2. The product $BA$.**

$$
BA=
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
a\cdot 1+b\cdot 0 & a\cdot 1+b\cdot 1 \\
c\cdot 1+d\cdot 0 & c\cdot 1+d\cdot 1 \\
\end{pmatrix}=
\begin{pmatrix}
a & a+b \\
c & c+d \\
\end{pmatrix}.
$$

**3. The condition $AB=BA$.** Two matrices are equal exactly when all their corresponding entries are equal. Comparing the entries in positions $(1,1)$, $(1,2)$, $(2,1)$, $(2,2)$ gives

$$
\begin{aligned}
a+c &= a, \\
b+d &= a+b, \\
c &= c, \\
d &= c+d.
\end{aligned}
$$

**4. Solving the equations.**

- Position $(1,1)$: $a+c=a$ gives $c=0$.
- Position $(1,2)$: $b+d=a+b$ gives $d=a$.
- Position $(2,1)$: $c=c$ is always true and gives no condition.
- Position $(2,2)$: $d=c+d$ gives $c=0$, which is the condition already found.

Hence all four equations hold if and only if

$$
c=0\quad\mathrm{and}\quad d=a.
$$

The entries $a$ and $b$ are not restricted.

**5. The general form of $B$.** Substituting $c=0$ and $d=a$:

$$
B=
\begin{pmatrix}
a & b \\
0 & a \\
\end{pmatrix},\qquad a,b\ \mathrm{arbitrary}.
$$

These are exactly the upper triangular matrices whose two diagonal entries are equal. The set is a family with two free parameters. Since

$$
\begin{pmatrix}
a & b \\
0 & a \\
\end{pmatrix}=a
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}+b
\begin{pmatrix}
0 & 1 \\
0 & 0 \\
\end{pmatrix},
$$

every such matrix is also a linear combination of $I$ and $A$:

$$
B=(a-b)\,I+b\,A.
$$

### Property / method

Matrix multiplication is not commutative, so $AB=BA$ is a genuine condition on $B$. A systematic way to find it is to compute both products with unknown entries and compare entries, as above.

The same result follows from a shortcut. Write $A=I+N$, where

$$
N=
\begin{pmatrix}
0 & 1 \\
0 & 0 \\
\end{pmatrix}.
$$

Since $IB=BI=B$, we get $AB-BA=NB-BN$, so $AB=BA$ if and only if $NB=BN$. Here

$$
NB=
\begin{pmatrix}
c & d \\
0 & 0 \\
\end{pmatrix},\qquad
BN=
\begin{pmatrix}
0 & a \\
0 & c \\
\end{pmatrix}.
$$

Equality of these matrices requires $c=0$, $d=a$, $0=0$ and $0=c$, which is the same condition as before.

### Verification

For

$$
B=
\begin{pmatrix}
a & b \\
0 & a \\
\end{pmatrix}
$$

both products are equal:

$$
AB=
\begin{pmatrix}
a+0 & b+a \\
0 & a \\
\end{pmatrix}=
\begin{pmatrix}
a & a+b \\
0 & a \\
\end{pmatrix},\qquad
BA=
\begin{pmatrix}
a & a+b \\
0 & 0+a \\
\end{pmatrix}=
\begin{pmatrix}
a & a+b \\
0 & a \\
\end{pmatrix}.
$$

**A numerical example.** For $a=2$, $b=3$ let

$$
B=
\begin{pmatrix}
2 & 3 \\
0 & 2 \\
\end{pmatrix}.
$$

Then both products are the same matrix:

$$
AB=BA=
\begin{pmatrix}
2 & 5 \\
0 & 2 \\
\end{pmatrix}.
$$

**A matrix that does not commute.** Let

$$
B=
\begin{pmatrix}
1 & 0 \\
1 & 1 \\
\end{pmatrix}.
$$

Here $c=1\neq 0$, so the condition fails, and indeed

$$
AB=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}\neq
\begin{pmatrix}
1 & 1 \\
1 & 2 \\
\end{pmatrix}=BA.
$$
