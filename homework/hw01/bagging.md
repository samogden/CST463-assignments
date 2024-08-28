# Reading: Bagging and Random Forests

Reminder:
Please review homework honor policy before beginning.

## Purpose

Bagging and random forest are two of the most important ensemble methods.
In this assignment you will develop a deeper understand of them.

## Instructions

Read chapter 7 of our text `Hands-on Machine Learning with Scikit-Learn, Keras, and Tensorflow` up to, but not including, the `Boosting` section.

Answer the following questions by editing the file [bagging.txt] with a text editor.
Be sure that you save your editted file as a `.txt` file -- not a pdf file, Word file, etc.

## Questions

### Q1

You train a voting classifier with three classifiers.   
The problem is a binary classification problem (classes A and B).  
On a test example, classifier 1 predicts class A with probability 0.75, classifier 2 predicts class A with probability 0.45, and classifier 3 predicts class A with probability 0.40.

With hard voting, what class is predicted by the ensemble, A or B?

### Q2
Using the information in [Q1](#Q1), with soft voting, what class is predicted by the ensemble, A or B?

### Q3
(T/F)  With a bagging ensemble, the base predictors should be of different types.  
For example, not all of the base predictors should use KNN.

### Q4
There is an ensemble method that is like bagging except that the training data is sampled without replacement.  What is this method called?

- a. boosting
- b. pasting
- c. random subspaces

### Q5
(T/F) In a random forest classifier, all the base classifiers are trained using the same training data set.

### Q6
In picking a supervised learning algorithm, would you prefer higher variance or lower variance?
- a. higher
- b. lower


