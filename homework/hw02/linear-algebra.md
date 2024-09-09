# HW2: Linear Algebra

## Purpose
The purpose of this assignment is to help you strengthen your skills in linear algebra, which is a foundation for machine learning.

## Instructions
Please answer the following questions by editing the file [linear-algebra.txt](linear-algebra.txt).  

When answering, use the notation of `[[1,2],[3,4]]` for a 2x2 matrix with values 1,2 in the first row and values 3,4 in the second row, and write `[1, 5, 2]` for a column vector.  

Use this notation yourself when providing answers or the grading script will mark your answer incorrect.

For numbers, please use simplified fractions, not decimal numbers.


## Questions

### Q1
Every linear combination of vectors 
$`\begin{bmatrix} 1 & -2 & 1 \end{bmatrix}`$ 
and 
$`\begin{bmatrix} 0 & 1 & -1 \end{bmatrix}`$
has components that add to ______?  (The "components" of a vector are the elements of the vector.)


### Q2
What is the dot product of vectors 
$`\begin{bmatrix} 1 & 3 & -2 \end{bmatrix}`$
and 
$`\begin{bmatrix} 0 & 2 & 5 \end{bmatrix}`$
?


### Q3
Suppose vector 
$`r = \begin{bmatrix} 2 & -1 \end{bmatrix}`$ 
and vector 
$`s = \begin{bmatrix} -1 & 2 \end{bmatrix}`$
.  
Then what is the vector $x$ (of length 2) such that it has the dot products $` x \cdot r = 1`$ and $` x \cdot s = 0`$?


### Q4
Let matrix 
$`A = \begin{bmatrix}1 & 3 & 1 \\ 0 & 1 & 0 \\ 1 & 1 & 2 \end{bmatrix}`$
and
$`B = \begin{bmatrix}2 & -5 & -1 \\ 0 & 1 & 1 \\ -1 & 2 & 1 \end{bmatrix}`$

What is $`AB`$?


### Q5

$`A = \begin{bmatrix} 1 & 2 & 4 \\ 2 & 0 & 1 \end{bmatrix}`$
and
$`B = \begin{bmatrix} 3 \\ 1 \\ 1 \end{bmatrix}`$

What is $`AB`$?


### Q6

(Yes/No)  
Matrix multiplication is not defined for all pairs of vectors. Are $`AA^{T}`$ and $`A^{T}A`$ defined for any matrix A?


### Q7
If the size of matrix $`A`$ is $`m`$ by $`n`$, then what is the size of $`A^{T} A`$?  (In providing your answer, you would write `7 x 3` if the size were 7 by 3.)


### Q8

Suppose we have the following equations:

```math
\displaylines{
x + 2y + 3z = 0 \\

2x + 5y + 2z = 4 \\

6x - 3y + z = 2 \\
}
```

These equations can be written in matrix form as an equation $Ax = b$. 
What is the coefficient matrix $`A`$?


### Q9

What is a 3 by 3 matrix $`A`$ that would subtract 4 times row 1 from row 2 of matrix $`B`$ when A is multiplied by B?  
(Matrix $`B`$ is also a 3 x 3 matrix.  To provide your answer, just give the matrix $`A`$.)


### Q10

Suppose
$`u = \begin{bmatrix} 2  \\ 1 \end{bmatrix}`$,
$`v = \begin{bmatrix} -1 \\ 3 \end{bmatrix}`$,
and matrix $A$ such that
$`Au = \begin{bmatrix} 5 & 6 \end{bmatrix}`$
and
$`Av = \begin{bmatrix} 2 & 0 \end{bmatrix}`$
.

If
$`w = \begin{bmatrix} -1, 4 \end{bmatrix}`$
then what is $`Aw`$?

Provide a vector.
