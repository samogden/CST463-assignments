# Lab: CNN - borrowing layers

In this lab we'll try using a pretrained CNN to predict the class of an image.  Specifically, we'll try to classify CIFAR10 images using the VGG16 CNN, which was trained on ImageNet data (a famous collection of images with millions of images, 1000 classes).

Please work with your team.   Create a notebook and follow the steps below.  Here are some useful imports:

```python
import numpy as np
import matplotlib.pyplot as plt
from tensorflow.keras.applications.vgg16 import VGG16
from tensorflow.keras.applications.imagenet_utils import decode_predictions
from tensorflow.keras.utils import plot_model
from tensorflow.keras.datasets import cifar10
import tensorflow as tf

```

## Q1 
Make an instance of a VGG16 model.  It should be trained on ImageNet data.

<details><summary>Answer</summary>

`model = VGG16()`.  I believe all the defaults are okay.

</details>

## Q2
Do a model summary().  How many dense layers are there at the end of the model?

<details><summary>Answer</summary>

There are two large dense layers before the final dense layer used for classification.

</details>

## Q3 
Plot the model using plot_model() .

## Q4 
Load the CIFAR10 data.

```python
from tensorflow.keras.datasets import cifar10
(X_train, y_train), (X_test, y_test) = cifar10.load_data()
```

## Q5
Get 100 images from X_train, and name them X_sample.  Get the labels for the same images and name them y_sample.

<details><summary>Answer</summary>

```python
idx = np.random.choice(X_train.shape[0], 100)
X_sample = X_train[idx]
y_sample = y_train[idx]
```

</details>

## Q6
Print the first 10 values of y_sample.  Refer to https://keras.io/api/datasets/cifar10/ to understand what they mean.

## Q7 
Print a couple of the images in X_sample using plt.imshow().

## Q8 
Resize the images to 224 x 224 using tf.image.resize.

```python
import tensorflow as tf
X_sample_resized = tf.image.resize(X_sample, (224,224), antialias=True)
```


## Q9
Can you plot the resized images?  Figure out what to do to plot them.  Hint: the error message is very helpful.  If you're low on time, see the hint.

<details><summary>Hint</summary>
`X_sample_resized = np.array(X_sample_resized)/255`

</details>

## Q10
Compute predictions for 100 CIFAR samples, and save the result in sample_predications.  What is the shape of sample predictions?

## Q11
Are the predictions correct?  To find the name of the object for each imagenet class label, use decode_predictions() (see imports).   For the case of CIFAR10, see https://keras.
io/api/datasets/cifar10/ for a description of each class label.
