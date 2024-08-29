# Lab: Linear Algebra - Matrices


## Q1

Suppose a matrics A has size $2 \times 3$, B has size $1 \times 3$ and C has size $3 \times 3$.
Please answer the below questions

### Q1a

Is the produce AB possible?  If so, what is its size?

<details>
<summary>Answer</summary>

No, they are the wrong sizes since the number of columns in A doesn't match the number of rows in B.

</details>

### Q1b

Is the product $BC$ possible?  If so what is its size?

<details>
<summary>Answer</summary>

Yes, the resulting matrix would be $1 \times 3$

</details>

### Q1c

If C has an inverse, what is its size?

<details>
<summary>Answer</summary>

It would be the same size as $C$, so $3 \times 3$

</details>

### Q1d 

What is the size of $A^{-1}$?

<details>
<summary>Answer</summary>

Since $A$ is not a square matrix, no inverse is possible.

</details>

### Q1e

What is the size of $(BC)^{T}$?

<details>
<summary>Answer</summary>
As we know from [Q1b](#q1b), the size of $BC$ is $1 \times 3$, so it's transpose would be $3 \times 1$.

</details>

### Q1f

Does it make sense to write $C^3$?  What does it mean?

<details>
<summary>Answer</summary>

Extrapolating from what we usually use the notation for, this probably means to multiple C by itself multiple times.
Since $C$ is a square matrix multiplication by itself is possible and result in a matrix of the same size -- and still square!
Therefore, this should be possible!

</details>