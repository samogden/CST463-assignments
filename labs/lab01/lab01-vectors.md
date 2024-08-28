#! Lab: Linear Algebra - Vectors

In the problems below we'll use these vectors, which I will write in text as (2,-1), (-1,2), and (1,0).

```math
v = \begin{bmatrix}
2 \\
-1
\end{bmatrix}

w = \begin{bmatrix}
-1 \\
2
\end{bmatrix}

b = \begin{bmatrix}
1 \\
0
\end{bmatrix}
```


## Q1
Draw $v$ and $w$ as arrows in a 2-axis coordinate system (like we did in lecture).  Draw $v + w$.  Draw $v - w$.

## Q2
What is the result of this linear combination of vectors v and w (defined in the previous problem)?  
```math
2v - w$
```

Give your answer as a vector, and also draw it.

## Q3
Is there a linear combination of $v$ and $w$ that gives the vector $(1,0)$ ?  In other words, is there a value $b$ and a value $c$ such that $bv + cw = (1, 0)$ ?

## Q4
For every point in 2-dimensional space, can the point be expressed as the linear combination of $v$ and $w$?  

## Q5
Here is an equation involving vectors:
$x(1,-1) + y(0, 3) = (-1, 4)$
Can you write this instead as a system of 2 linear equations?  (In other words, 2 linear equations, one above the other.)

## Q6
What is the dot product of $v$ and $w$?

## Q7
What is the dot product of $w$ and $v$?

## Q8
What is the (Euclidean) norm of $v$?

## Q9
What is the normalized version of $v$?

## Q10
Write your own NumPy function that will return the dot product of two vectors:

```python
def dot_prod(u, v):
# your code
```

Compare the result of your function with your answers to problems 6 and 7.

## Q11
It is interesting that $`||u|| = \sqrt{u \cdot u}`$ .  Prove this is true, using the relationship between dot product and cosine, and remember the value of cosine(0).  It's not hard -- work with your lab mate.

## Q12
Without googling, what's the dot product of two perpendicular vectors?
Check out this 3blue1brown video: [Essence of linear algebra, chapter 1](https://youtu.be/fNk_zzaMoSs)
