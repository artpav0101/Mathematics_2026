Exercise 12. Formula for a Matrix Power

Given

A=\begin{pmatrix}1 & 1\\0 & 1\end{pmatrix}

Compute $A^2$, $A^3$, and $A^4$, formulate a conjecture for $A^n$, and prove the formula using mathematical induction.

Main steps

1. Calculate $A^2$.

By definition:

A^2=A\cdot A
A^2=
\begin{pmatrix}1 & 1\\0 & 1\end{pmatrix}
\begin{pmatrix}1 & 1\\0 & 1\end{pmatrix}
=
\begin{pmatrix}1 & 2\\0 & 1\end{pmatrix}.

2. Calculate $A^3$.

A^3=A^2\cdot A
A^3=
\begin{pmatrix}1 & 2\\0 & 1\end{pmatrix}
\begin{pmatrix}1 & 1\\0 & 1\end{pmatrix}
=
\begin{pmatrix}1 & 3\\0 & 1\end{pmatrix}.

3. Calculate $A^4$.

A^4=A^3\cdot A
A^4=
\begin{pmatrix}1 & 3\\0 & 1\end{pmatrix}
\begin{pmatrix}1 & 1\\0 & 1\end{pmatrix}
=
\begin{pmatrix}1 & 4\\0 & 1\end{pmatrix}.

4. Formulate a conjecture.

Looking at the first four powers:

A^1=\begin{pmatrix}1 & 1\\0 & 1\end{pmatrix},
\quad
A^2=\begin{pmatrix}1 & 2\\0 & 1\end{pmatrix},
A^3=\begin{pmatrix}1 & 3\\0 & 1\end{pmatrix},
\quad
A^4=\begin{pmatrix}1 & 4\\0 & 1\end{pmatrix}.

We observe the following pattern:

* The diagonal entries always remain equal to $1$.
* The lower-left entry always remains equal to $0$.
* The upper-right entry increases by $1$ with each multiplication.

Therefore, we conjecture that:

\boxed{A^n=\begin{pmatrix}1 & n\\0 & 1\end{pmatrix}}

for every positive integer $n$.

Proof by mathematical induction

We will prove that the conjectured formula holds for every positive integer $n$.

1. Base case: $n=1$.

For $n=1$, the formula gives:

A^1=\begin{pmatrix}1 & 1\\0 & 1\end{pmatrix}.

This is exactly the original matrix $A$. Therefore, the formula holds for $n=1$.

2. Inductive hypothesis.

Assume that the formula is true for some positive integer $n$:

A^n=\begin{pmatrix}1 & n\\0 & 1\end{pmatrix}.

3. Inductive step: prove the formula for $n+1$.

We need to show that:

A^{n+1}=\begin{pmatrix}1 & n+1\\0 & 1\end{pmatrix}.

By the definition of matrix powers:

A^{n+1}=A^n\cdot A.

Substituting the inductive hypothesis:

A^{n+1}=
\begin{pmatrix}1 & n\\0 & 1\end{pmatrix}
\begin{pmatrix}1 & 1\\0 & 1\end{pmatrix}.

Multiplying the matrices:

A^{n+1}=
\begin{pmatrix}
1\cdot1+n\cdot0 & 1\cdot1+n\cdot1\\
0\cdot1+1\cdot0 & 0\cdot1+1\cdot1
\end{pmatrix}.

Simplifying:

A^{n+1}=
\begin{pmatrix}1 & n+1\\0 & 1\end{pmatrix}.

This is exactly the proposed formula with $n$ replaced by $n+1$.

Therefore, if the formula holds for $n$, it also holds for $n+1$.

4. Conclusion.

Since the formula holds for the base case $n=1$ and the inductive step is valid, by mathematical induction:

\boxed{A^n=\begin{pmatrix}1 & n\\0 & 1\end{pmatrix}}

for every positive integer $n$.

Result

The first three calculated powers are:

A^2=\begin{pmatrix}1 & 2\\0 & 1\end{pmatrix},
\quad
A^3=\begin{pmatrix}1 & 3\\0 & 1\end{pmatrix},
\quad
A^4=\begin{pmatrix}1 & 4\\0 & 1\end{pmatrix}.

The general formula is:

\boxed{A^n=\begin{pmatrix}1 & n\\0 & 1\end{pmatrix}},
\qquad n\geq1.

Property / method

Mathematical induction is a proof technique consisting of two essential steps:

* Base case: Verify that the statement is true for the first value, usually $n=1$.
* Inductive step: Assume the statement is true for $n$ and prove that it must also be true for $n+1$.

If both steps are established, the statement holds for all positive integers.

Verification

The inductive step confirms the pattern:

\begin{pmatrix}1 & n\\0 & 1\end{pmatrix}
\begin{pmatrix}1 & 1\\0 & 1\end{pmatrix}
=
\begin{pmatrix}1 & n+1\\0 & 1\end{pmatrix}.

Each multiplication increases the upper-right entry by exactly $1$, while the other three entries remain unchanged.

This proves that the conjectured formula works for every positive integer, not just the first few powers.
