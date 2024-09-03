# Lab: Gradient Boosting


## Instructions

Please answer the questions below

## Questions

### Q1

Please answer the following questions by replacing `[blank]` with the appropriate answer

In gradient boosting, the first predictor trains on `[blank1]`,
the second predictor trains on `[blank2]`
the prediction of the ensemble on a training instance is `[blank3]`

<details><summary>Answer</summary>

The first predictor trains on `the plain training data`, 
the second predictor trains on `the same data, but with the target values replaced by the residual errors from the the output of the first predictor on the training data`, 
and the ensemble prediction on a training instance is `the sum of the predictions of the base predictors on that instance`.

</details>

### Q2

Are all predictors in gradiant boosting the same type?

<details><summary>Answer</summary>

In practice they typically are, but in theory they are not limited to being only of a single type.

</details>

### Q3

How does gradient boosting work with classification tasks?

<details><summary>Answer</summary>

You generally would predict probabilities and then use those in a loss function.

</details>

### Q4

Name one hyperparameter  used with gradient boosting.

<details><summary>Answer</summary>

See the slides and the [documentation](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.GradientBoostingRegressor.html#sklearn.ensemble.GradientBoostingRegressor) for details

</details>

### Q5

In the slide "finding the optimal number of trees", why wasn't grid search used instead?

<details><summary>Answer</summary>

We want to look inside the algorithm during the training of base predictors -- this couldn’t be done with regular grid search.  To be more specific, consider how staged_predict() works.  Suppose it has produced predictions for the case of 50 predictors, and wants to produce a prediction for the case of 51 predictors.  It simply adds one more predictor to the ensemble, and then produces the predictions from the new ensemble.  If you were doing grid search instead, a gradient boosting ensemble of 50 predictors would be built, predictions made from it, and then a completely new ensemble of 51 predictors would be built (as opposed to just adding one more predictor to the ensemble of 50).

</details>

### Q6

Using the [starter notebook](starter_notebook.ipynb), use gradient boosting for regression using the build-in diabeters dataset. 
First, build training and test sets.
Try a few times with different hyperparameter values.
Compare your results with a single tree regressor.

### Q7

If you still have time, use a grid search to find good hyperparameter values.  How well did it do?