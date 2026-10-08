### Exercise 2. Gaussian Elimination — One Solution

**Problem.** Solve using Gaussian elimination:

$$
\begin{cases}
x+y+z=6, \\
2x-y+z=3, \\
x+2y-z=2.
\end{cases}
$$

After solving, substitute the result into all equations and check consistency.

**Solution**

**Augmented matrix**

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
2 & -1 & 1 & \mid & 3 \\
1 & 2 & -1 & \mid & 2 \\
\end{pmatrix}
$$

**Step 1.** Eliminate $x$ from rows 2 and 3 using $R_2-2R_1$ and $R_3-R_1$.

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & -3 & -1 & \mid & -9 \\
0 & 1 & -2 & \mid & -4 \\
\end{pmatrix}
$$

**Step 2.** Swap rows 2 and 3 to obtain a convenient pivot.

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & 1 & -2 & \mid & -4 \\
0 & -3 & -1 & \mid & -9 \\
\end{pmatrix}
$$

**Step 3.** Eliminate $y$ from row 3 using $R_3+3R_2$.

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & 1 & -2 & \mid & -4 \\
0 & 0 & -7 & \mid & -21 \\
\end{pmatrix}
$$

**Back substitution**

From the third row:

$$
-7z=-21 \quad\Rightarrow\quad z=3
$$

From the second row:

$$
y-2z=-4 \quad\Rightarrow\quad y=-4+6=2
$$

From the first row:

$$
x+y+z=6 \quad\Rightarrow\quad x=6-2-3=1
$$

**Answer**

$$
(x,y,z)=(1,2,3)
$$

**Check in all equations**

$$
\begin{aligned}
x+y+z &= 1+2+3 = 6 \\
2x-y+z &= 2-2+3 = 3 \\
x+2y-z &= 1+4-3 = 2 \\
\end{aligned}
$$

All three equations are satisfied, so the system is consistent and has the unique solution $(1,2,3)$.
