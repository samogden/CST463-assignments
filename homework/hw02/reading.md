# HW2: Reading: Dimensionality reduction

## Purpose

Dimensionality reduction is one of the most important unsupervised machine learning methods.
It's also important conceptually because of its connection to neural nets.

## Instructions

Read Chapter 8 of our text 'Hands-on machine learning with Scikit-Learn, Keras, and Tensorflow'.  
Feel free to skim the "LLE" section.  
Some of the questions below are based on class lectures.
Note that in Equation 8-1 of the Geron text, the principal components are the columns, while with Scikit-Learn's PCA(), the principal components are the rows.

Answer the following questions by editing the file [dim-red.txt](dim-red.txt) with a text editor.  
Be sure that you save your edited file as a .txt file -- not a pdf file, Word file, etc.

## Questions

### Q1
On average, if you two points randomly in a 1000-dimensional unit hypercube, about how far apart will they be?

### Q2

Does basic PCA (not kernel PCA) do a good job when reducing the "swiss roll" from 3 dimensions to 2?
### Q3

Suppose your data set has m rows and n columns (each column is a feature).  If you apply PCA to the data, what is the length of a principal component?

### Q4

We can get the total variance of a data set by adding up the variance of each feature.  Is the total variance affected by a change in basis?   (In other words, by changing the vectors we use to describe the data.)


### Q5

When you use Scikit-Learn's PCA class, is it necessary to first zero-center the data?   This is done on each feature column by subtracting the average value of the column from each value in the column.
    Submission.  Submit your edited dim-red.txt on Canvas.
