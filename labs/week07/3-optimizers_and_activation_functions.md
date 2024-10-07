# Lab: Optimizers and activation functions
Be sure to work with your lab team.

## Steps

### 1
Using the code from the previous lab, use the [diamonds data set](../../datasets/diamonds.csv) with price as the target value.  
Use all numeric columns of the dataset (except for price) as the predictors.

You don't need to create a separate test set, but use a validation split when training your neural net in model.fit()

### 2 
First, spend a few minutes deciding on how many hidden layers to use, and the number of neurons in each hidden layer. 

### 3
Next, try playing with these things:
    - optimizer: see https://keras.io/api/optimizers/
    - activation functions: https://keras.io/api/layers/activations/
    - learning rate  (we've already seen how to do this)
Take note of your results with various combinations of the parameters.

### 4
If you have time, also try to add batch normalization.  This is a little tricky, because it's usually suggested to use batch normalization between the summation part of the neuron and the activation part of the neuron.
    https://keras.io/api/layers/normalization_layers/batch_normalization/
