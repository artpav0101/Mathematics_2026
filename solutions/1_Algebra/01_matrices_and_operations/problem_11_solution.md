# Exercise 11. When Do Matrices Commute?

## Given

$$
A = \begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix},
\qquad
B = \begin{pmatrix}
a & b \\
c & d
\end{pmatrix}.
$$

Find the conditions on $a,b,c,d$ under which $AB = BA$. Describe the general form of all such matrices $B$.

## Solution

To determine when the matrices commute, we calculate both products $AB$ and $BA$, then set them equal.

### 1. Calculate $AB$

$$
AB =
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
$$

Multiplying the matrices:

$$
AB =
\begin{pmatrix}
a+c & b+d \\
c & d
\end{pmatrix}.
$$

### 2. Calculate $BA$

$$
BA =
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix}
$$

Multiplying the matrices:

$$
BA =
\begin{pmatrix}
a & a+b \\
c & c+d
\end{pmatrix}.
$$

### 3. Set $AB = BA$

Equating the two products:

$$
\begin{pmatrix}
a+c & b+d \\
c & d
\end{pmatrix}
=
\begin{pmatrix}
a & a+b \\
c & c+d
\end{pmatrix}.
$$

Comparing corresponding entries gives:

$$
\begin{cases}
a+c = a, \\
b+d = a+b, \\
c = c, \\
d = c+d.
\end{cases}
$$

Simplifying the equations:

$$
\begin{cases}
c = 0, \\
d = a.
\end{cases}
$$

Therefore, the necessary and sufficient conditions are:

$$
\boxed{c=0,\qquad d=a}.
$$

### 4. General Form of Matrix $B$

Substituting these conditions into the original matrix:

$$
B =
\begin{pmatrix}
a & b \\
0 & a
\end{pmatrix}.
$$

Thus, all matrices that commute with $A$ have the following general form:

$$
\boxed{
B =
\begin{pmatrix}
a & b \\
0 & a
\end{pmatrix},
\qquad a,b \in \mathbb{R}.
}
$$

## Final Answer

The matrices $A$ and $B$ commute if and only if:

$$
\boxed{c=0,\qquad d=a}.
$$

The general form of all such matrices is:

$$
\boxed{
B =
\begin{pmatrix}
a & b \\
0 & a
\end{pmatrix}.
}
$$

## Key Insight

Matrix multiplication is generally **not commutative**, meaning that $AB \neq BA$.

However, certain matrices do commute. In this exercise, matrix $B$ must have equal diagonal entries and a zero lower-left entry.

The values of $a$ and $b$ can be arbitrary, meaning there are infinitely many matrices that commute with $A$.
