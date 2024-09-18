# Lab: Logistic Regression

## Questions

### Q1
Explain, in your own words, how to implement logistic regression with gradient descent.  Write it down.

### Q2
  
What is the value of the sigmoid function for input 0?

### Q3
  

The cost function for logistic regression starts with a factor of 1/m.  What difference would it make if we removed it?

### Q4
  

Using NumPy, write a function that will give log loss for a single prediction p and single target y.  Test that your function is correct.

### Q5
  

Using NumPy, write a function that will give log loss for an array of predictions and an array of target variables.  Test that your function is correct using the example we covered in the lecture.


### Q6
  

Are the following two functions equal?  Either prove they are, or give an input value on which they are different.

```math

\frac{1}{1 + e^{-t}} \stackrel{?}{=} \frac{e^t}{e^t + 1}

```


### Q7
  

If you still have time, write the complete loss function for binary logistic regression (in other words, a version of the loss function that includes the training data X,y as variables).
 