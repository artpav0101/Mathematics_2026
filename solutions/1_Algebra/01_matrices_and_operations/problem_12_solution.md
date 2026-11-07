## Question 

### Exercise 12. Formula for a Matrix Power
Let

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}.
$$

Compute $A^2$, $A^3$, and $A^4$, and use them to formulate a conjecture for $A^n$. Then do not stop after checking one more case: assume the formula is true for $n$, multiply by $A$, and explain why you obtain exactly the formula for $n+1$.

> **Why this exercise:** teaches how to recognize a pattern and formulate a generalization from several computations.

## Solution

For

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

the powers are

$$
A^2=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad
A^3=
\begin{pmatrix}
1 & 3 \\
0 & 1 \\
\end{pmatrix},\qquad
A^4=
\begin{pmatrix}
1 & 4 \\
0 & 1 \\
\end{pmatrix}.
$$

The conjecture, proved below by induction, is

$$
A^n=
\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix},\qquad n=1,2,3,\ldots
$$

### Main steps

**1. The power $A^2$.**

$$
A^2=AA=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot 1+1\cdot 0 & 1\cdot 1+1\cdot 1 \\
0\cdot 1+1\cdot 0 & 0\cdot 1+1\cdot 1 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}.
$$

**2. The power $A^3$.** Multiply the previous power by $A$:

$$
A^3=A^2A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot 1+2\cdot 0 & 1\cdot 1+2\cdot 1 \\
0\cdot 1+1\cdot 0 & 0\cdot 1+1\cdot 1 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 3 \\
0 & 1 \\
\end{pmatrix}.
$$

**3. The power $A^4$.**

$$
A^4=A^3A=
\begin{pmatrix}
1 & 3 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot 1+3\cdot 0 & 1\cdot 1+3\cdot 1 \\
0\cdot 1+1\cdot 0 & 0\cdot 1+1\cdot 1 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 4 \\
0 & 1 \\
\end{pmatrix}.
$$

**4. The pattern and the conjecture.** In every power the diagonal entries are $1$, the entry below the diagonal is $0$, and the entry in position $(1,2)$ equals the exponent: $1,\ 2,\ 3,\ 4$ for $A,\ A^2,\ A^3,\ A^4$. This suggests

$$
A^n=
\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix}.
$$

**5. Proof by induction.** Checking further cases (for example $A^5$) would only add more evidence. A proof needs an argument that works for every $n$.

*Base case.* For $n=1$ the formula gives the matrix with first row $(1,\ 1)$ and second row $(0,\ 1)$. This is $A$ itself, so the formula is true for $n=1$.

*Induction step.* Assume that the formula holds for some $n$:

$$
A^n=
\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix}.
$$

Multiply by $A$ and use $A^{n+1}=A^nA$:

$$
A^{n+1}=A^nA=
\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot 1+n\cdot 0 & 1\cdot 1+n\cdot 1 \\
0\cdot 1+1\cdot 0 & 0\cdot 1+1\cdot 1 \\
\end{pmatrix}=
\begin{pmatrix}
1 & n+1 \\
0 & 1 \\
\end{pmatrix}.
$$

### Why this is exactly the formula for $n+1$

Compare the result with the formula

$$
\begin{pmatrix}
1 & m \\
0 & 1 \\
\end{pmatrix}
$$

in which the exponent $m$ is replaced by $n+1$. The entries $1$, $0$, $0$, $1$ do not depend on the exponent, and they are reproduced unchanged: multiplication by $A$ does not alter the first column $(1,\ 0)^T$, and the second row of $A^n$ is $(0,\ 1)$. The only entry that depends on the exponent is the one in position $(1,2)$, and there

$$
1\cdot 1+n\cdot 1=n+1.
$$

In words: multiplying by $A$ adds the first column of $A^n$ to its second column, that is, it adds $1$ to the entry $n$. So passing from $n$ to $n+1$ changes the formula exactly by replacing $n$ with $n+1$, and nothing else. Since the statement is true for $n=1$ and the truth for $n$ implies the truth for $n+1$, it is true for all $n=1,2,3,\ldots$

### Property / method

Proof by induction consists of two parts: the base case and the step "if the statement holds for $n$, then it holds for $n+1$". The computed powers $A^2,A^3,A^4$ are used only to guess the formula. The induction step is what turns the guess into a theorem.

### Verification

The formula also gives $A^0=I$ for $n=0$, as it should.

An independent derivation uses Exercise 11. Write $A=I+N$ with

$$
N=
\begin{pmatrix}
0 & 1 \\
0 & 0 \\
\end{pmatrix},\qquad
N^2=
\begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix}.
$$

The matrices $I$ and $N$ commute, so the binomial theorem applies. All terms with $N^2,N^3,\ldots$ vanish, hence

$$
A^n=(I+N)^n=I+nN=
\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix},
$$

in agreement with the formula.
