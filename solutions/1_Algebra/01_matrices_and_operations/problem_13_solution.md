## Exercise 13. A Recurrence Written in Matrix Form

### Result

For

$$
F=
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}
$$

the powers are

$$
F^2=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix},\qquad
F^3=
\begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix},\qquad
F^4=
\begin{pmatrix}
5 & 3 \\
3 & 2 \\
\end{pmatrix},\qquad
F^5=
\begin{pmatrix}
8 & 5 \\
5 & 3 \\
\end{pmatrix}.
$$

Denote the numbers of the sequence $0,1,1,2,3,5,8,\ldots$ by $f_0=0$, $f_1=1$, $f_2=1$, $f_3=2$, $f_4=3$, $f_5=5$, $f_6=8$, with $f_{n+1}=f_n+f_{n-1}$. Then

$$
F^n=
\begin{pmatrix}
f_{n+1} & f_n \\
f_n & f_{n-1} \\
\end{pmatrix},\qquad n\geq 1.
$$

Moreover,

$$
F
\begin{pmatrix}
a \\
b \\
\end{pmatrix}=
\begin{pmatrix}
a+b \\
a \\
\end{pmatrix}.
$$

### Main steps

**1. The power $F^2$.**

$$
F^2=FF=
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot 1+1\cdot 1 & 1\cdot 1+1\cdot 0 \\
1\cdot 1+0\cdot 1 & 1\cdot 1+0\cdot 0 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}.
$$

**2. The power $F^3=F^2F$.**

$$
F^3=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
2\cdot 1+1\cdot 1 & 2\cdot 1+1\cdot 0 \\
1\cdot 1+1\cdot 1 & 1\cdot 1+1\cdot 0 \\
\end{pmatrix}=
\begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix}.
$$

**3. The power $F^4=F^3F$.**

$$
F^4=
\begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
3\cdot 1+2\cdot 1 & 3\cdot 1+2\cdot 0 \\
2\cdot 1+1\cdot 1 & 2\cdot 1+1\cdot 0 \\
\end{pmatrix}=
\begin{pmatrix}
5 & 3 \\
3 & 2 \\
\end{pmatrix}.
$$

**4. The power $F^5=F^4F$.**

$$
F^5=
\begin{pmatrix}
5 & 3 \\
3 & 2 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
5\cdot 1+3\cdot 1 & 5\cdot 1+3\cdot 0 \\
3\cdot 1+2\cdot 1 & 3\cdot 1+2\cdot 0 \\
\end{pmatrix}=
\begin{pmatrix}
8 & 5 \\
5 & 3 \\
\end{pmatrix}.
$$

**5. Comparison with the sequence.** The entries of the powers are consecutive numbers of the sequence $0,1,1,2,3,5,8,\ldots$:

- $F^2$ has entries $f_3,f_2,f_2,f_1=2,1,1,1$;
- $F^3$ has entries $f_4,f_3,f_3,f_2=3,2,2,1$;
- $F^4$ has entries $f_5,f_4,f_4,f_3=5,3,3,2$;
- $F^5$ has entries $f_6,f_5,f_5,f_4=8,5,5,3$.

The relationship is

$$
F^n=
\begin{pmatrix}
f_{n+1} & f_n \\
f_n & f_{n-1} \\
\end{pmatrix}.
$$

The matrix is symmetric, the off-diagonal entries are both $f_n$, and the diagonal entries are the neighbours $f_{n+1}$ and $f_{n-1}$. The case $n=1$ also fits: the formula gives the rows $(f_2,\ f_1)=(1,\ 1)$ and $(f_1,\ f_0)=(1,\ 0)$, which is the matrix $F$.

**6. Why the pattern persists.** Multiply a symmetric matrix with entries $x$, $y$, $y$, $z$ by $F$:

$$
\begin{pmatrix}
x & y \\
y & z \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
x+y & x \\
y+z & y \\
\end{pmatrix}.
$$

For $x=f_{n+1}$, $y=f_n$, $z=f_{n-1}$ this gives

$$
F^{n+1}=F^nF=
\begin{pmatrix}
f_{n+1}+f_n & f_{n+1} \\
f_n+f_{n-1} & f_n \\
\end{pmatrix}=
\begin{pmatrix}
f_{n+2} & f_{n+1} \\
f_{n+1} & f_n \\
\end{pmatrix},
$$

because $f_{n+1}+f_n=f_{n+2}$ and $f_n+f_{n-1}=f_{n+1}$. This is the formula for $n+1$. Together with the case $n=1$, it proves the formula for all $n\geq 1$ by induction.

**7. One recurrence step as a matrix product.** For a vector with arbitrary entries $a$ and $b$,

$$
F
\begin{pmatrix}
a \\
b \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot a+1\cdot b \\
1\cdot a+0\cdot b \\
\end{pmatrix}=
\begin{pmatrix}
a+b \\
a \\
\end{pmatrix}.
$$

If $a$ and $b$ are two consecutive terms of the sequence, $a=f_{n+1}$ and $b=f_n$, then

$$
F
\begin{pmatrix}
f_{n+1} \\
f_n \\
\end{pmatrix}=
\begin{pmatrix}
f_{n+1}+f_n \\
f_{n+1} \\
\end{pmatrix}=
\begin{pmatrix}
f_{n+2} \\
f_{n+1} \\
\end{pmatrix}.
$$

The first row of $F$ creates the sum of the two consecutive terms, which is the new term $f_{n+2}$. The second row of $F$ copies the first component $f_{n+1}$ into the second position, so that it is kept for the next step. The pair $(f_{n+1},\ f_n)$ is replaced by the pair $(f_{n+2},\ f_{n+1})$, which is one step of the recurrence.

Repeating the step $n$ times from the starting pair $(f_1,\ f_0)=(1,\ 0)$ gives

$$
F^n
\begin{pmatrix}
1 \\
0 \\
\end{pmatrix}=
\begin{pmatrix}
f_{n+1} \\
f_n \\
\end{pmatrix},
$$

which is the first column of $F^n$, as seen in the computed powers above.

### Property / method

A recurrence with two previous terms, $f_{n+1}=f_n+f_{n-1}$, is a linear step that acts on a pair of numbers. Writing the step as a matrix $F$ turns $n$ steps into the single power $F^n$. This is the basic idea behind computing recurrences by repeated squaring of a matrix.

### Verification

The rule $F^{m+n}=F^mF^n$ gives an independent check of $F^5$:

$$
F^5=F^2F^3=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
2\cdot 3+1\cdot 2 & 2\cdot 2+1\cdot 1 \\
1\cdot 3+1\cdot 2 & 1\cdot 2+1\cdot 1 \\
\end{pmatrix}=
\begin{pmatrix}
8 & 5 \\
5 & 3 \\
\end{pmatrix}.
$$

Also, $\det F=1\cdot 0-1\cdot 1=-1$, so $\det F^5=(-1)^5=-1$, and indeed $\det F^5=8\cdot 3-5\cdot 5=24-25=-1$.
