# Lab: Siamese networks

Please work with your team.   For a Siamese network you will probably want to generate training batches on the fly, using a batch generator.
## Questions
### Q1
Modify your CIFAR10 model so that it uses a batch generation function.

Check the [Keras documentation for fit()](https://www.tensorflow.org/api_docs/python/tf/keras/Model#fit).  An easy option is to just create a Python generator function that returns a batch.  Keras' fit() method will work with Python generators.  

I recommend that you start by writing a `function make_batch()` that, given X and y, returns X_batch, y_batch.  
Then write a Python generator batch_generator() that calls it.

Check to make sure `make_batch()` works.  
Then modify your `.fit()` call to provide batch_generator in place of the training data.

You can also use your batch_generator to generate validation data.


<details><summary>Hint</summary>

For the make_batch() function, a simple approach is like this:
```python
def make_batch(X, y, batch_size):
  rows = np.random.choice(X.shape[0], batch_size)
  return X[rows], y[rows]
```

You can choose to use replace=True or replace=Fase in the random.choice() call.

For the batch_generator() function, this works:
```python
def batch_generator(X, y, batch_size=32):
  while True:
    yield make_batch(X, y, batch_size)
```

For the `.fit()` call, you can do something like:
`.fit(batch_generator(X_train, y_train), steps_per_epoch=32, …)`


</details>


### Q2
If you achieve this, try adding data augmentation to your batch generator.
