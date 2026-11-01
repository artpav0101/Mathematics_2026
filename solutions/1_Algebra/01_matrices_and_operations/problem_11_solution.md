### Solution: Exercise 11. When Do Matrices Commute?

To find the conditions under which the matrices commute, we must calculate both $AB$ and $BA$, set them equal to each other, and solve for $a$, $b$, $c$, and $d$.

**1. Calculate $AB$:**

$$
AB = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} a & b \\ c & d \end{pmatrix} = \begin{pmatrix} 1\cdot a + 1\cdot c & 1\cdot b + 1\cdot d \\ 0\cdot a + 1\cdot c & 0\cdot b + 1\cdot d \end{pmatrix} = \begin{pmatrix} a+c & b+d \\ c & d \end{pmatrix}
$$

**2. Calculate $BA$:**

$$
BA = \begin{pmatrix} a & b \\ c & d \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} a\cdot 1 + b\cdot 0 & a\cdot 1 + b\cdot 1 \\ c\cdot 1 + d\cdot 0 & c\cdot 1 + d\cdot 1 \end{pmatrix} = \begin{pmatrix} a & a+b \\ c & c+d \end{pmatrix}
$$

**3. Equate $AB$ and $BA$:**

For $AB = BA$, their corresponding matrix entries must be identical:

$$
\begin{pmatrix} a+c & b+d \\ c & d \end{pmatrix} = \begin{pmatrix} a & a+b \\ c & c+d \end{pmatrix}
$$

This yields the following system of linear equations:

$$
\begin{aligned}
a + c &= a \implies c = 0 \\
b + d &= a + b \implies d = a \\
c &= c \\
d &= c + d \implies c = 0
\end{aligned}
$$

**4. Conditions and General Form:**

The equations dictate that $c = 0$ and $a = d$. There are no restrictions on $b$, meaning it can be any scalar. 

Therefore, the general form of all such matrices $B$ that commute with $A$ is:

$$
B = \begin{pmatrix} a & b \\ 0 & a \end{pmatrix}
$$
