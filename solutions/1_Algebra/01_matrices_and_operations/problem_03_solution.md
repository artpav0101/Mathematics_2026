## Exercise 3. When Can Matrices Be Multiplied?

Sizes: $`A_{2\times3},\ B_{3\times4},\ C_{4\times2},\ D_{2\times2}`$.

### Result

| Product | Sizes | Inner numbers equal? | Defined? | Size of result |
|:-------:|:-----:|:--------------------:|:--------:|:--------------:|
| $`AB`$ | $`2\times3`$ and $`3\times4`$ | $`3=3`$ | Yes | $`2\times4`$ |
| $`BA`$ | $`3\times4`$ and $`2\times3`$ | $`4\neq2`$ | No | n/a |
| $`BC`$ | $`3\times4`$ and $`4\times2`$ | $`4=4`$ | Yes | $`3\times2`$ |
| $`CB`$ | $`4\times2`$ and $`3\times4`$ | $`2\neq3`$ | No | n/a |
| $`AC`$ | $`2\times3`$ and $`4\times2`$ | $`3\neq4`$ | No | n/a |
| $`CA`$ | $`4\times2`$ and $`2\times3`$ | $`2=2`$ | Yes | $`4\times3`$ |
| $`AD`$ | $`2\times3`$ and $`2\times2`$ | $`3\neq2`$ | No | n/a |
| $`DA`$ | $`2\times2`$ and $`2\times3`$ | $`2=2`$ | Yes | $`2\times3`$ |

### Property / method

The product $`XY`$ is defined exactly when

```math
\#\text{columns of }X=\#\text{rows of }Y .
```

If $`X`$ is $`m\times n`$ and $`Y`$ is $`n\times p`$, then $`XY`$ is $`m\times p`$. The reason: entry $`(i,j)`$ of $`XY`$ is the sum $`\sum_{k=1}^{n}x_{ik}y_{kj}`$, which pairs the $`n`$ entries of row $`i`$ of $`X`$ with the $`n`$ entries of column $`j`$ of $`Y`$. If the counts differ, some entry has no partner.

### Verification

- Chain consistency: $`ABC`$ would be $`(2\times4)(4\times2)=2\times2`$, which agrees with the fact that $`AB`$ is $`2\times4`$ and $`C`$ is $`4\times2`$.
- The example shows that $`AB`$ can be defined while $`BA`$ is not. Matrix multiplication cannot be commutative in general.

---
