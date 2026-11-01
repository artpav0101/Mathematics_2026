# Exercise 12. Formula for a Matrix Power

## Given

$$
A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}
$$

Compute $A^2$, $A^3$, and $A^4$, and use them to formulate a conjecture for $A^n$. Then prove the formula using mathematical induction.

## Solution

### 1. Calculate $A^2$

By definition:

$$
A^2 = A \cdot A
$$

$$
A^2 =
\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}
\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}
$$

Multiplying the matrices:

$$
A^2 = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}
$$

### 2. Calculate $A^3$

$$
A^3 = A^2 \cdot A
$$

$$
A^3 =
\begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}
\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}
$$

Multiplying:

$$
A^3 = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}
$$

### 3. Calculate $A^4$

$$
A^4 = A^3 \cdot A
$$

$$
A^4 =
\begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}
\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}
$$

Multiplying:

$$
A^4 = \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}
$$

### 4. Formulate a Conjecture

Looking at the first four powers:

$$
A^1 = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}
$$

$$
A^2 = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}
$$

$$
A^3 = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}
$$

$$
A^4 = \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}
$$

We observe that:

- The diagonal entries always remain equal to $1$.
- The lower-left entry always remains $0$.
- The upper-right entry increases by $1$ with each multiplication.

Therefore, we conjecture that:

$$
A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}
$$

for every positive integer $n$.

### 5. Proof by Mathematical Induction

We will prove that:

$$
A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}
$$

for every positive integer $n$.

**Base Case: $n = 1$**

For $n = 1$:

$$
A^1 = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}
$$

This is exactly the original matrix $A$.

Therefore, the formula holds for $n = 1$.

**Inductive Hypothesis**

Assume that the formula holds for some positive integer $n$:

$$
A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}
$$

**Inductive Step**

We need to prove that the formula also holds for $n+1$.

By the definition of matrix powers:

$$
A^{n+1} = A^n \cdot A
$$

Substituting the inductive hypothesis:

$$
A^{n+1} =
\begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}
\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}
$$

Multiplying the matrices:

$$
A^{n+1} =
\begin{pmatrix}
1 \cdot 1 + n \cdot 0 & 1 \cdot 1 + n \cdot 1 \\
0 \cdot 1 + 1 \cdot 0 & 0 \cdot 1 + 1 \cdot 1
\end{pmatrix}
$$

Simplifying:

$$
A^{n+1} = \begin{pmatrix} 1 & n+1 \\ 0 & 1 \end{pmatrix}
$$

This is exactly the proposed formula with $n$ replaced by $n+1$.

Therefore, the formula holds for $n+1$ whenever it holds for $n$.

**Conclusion**

Since the formula holds for the base case and the inductive step is valid, by mathematical induction:

$$
\boxed{A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}}
$$

for every positive integer $n$.

## Final Answer

The first three calculated powers are:

$$
A^2 = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix},
\quad
A^3 = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix},
\quad
A^4 = \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}
$$

The general formula is:

$$
\boxed{A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}}
$$

where $n$ is any positive integer.

## Key Insight

Each multiplication by $A$ increases the upper-right entry by exactly $1$, while the other three entries remain unchanged.

Mathematical induction allows us to prove that this pattern holds for every positive integer, rather than just the first few powers.
