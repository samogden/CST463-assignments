This lab is a little unsatisfying because you don't get great results
from CIFAR images on VGG16.  This seems to be because CIFAR images are
much lower resolution than imagenet images.

Alternatives:
- use examples in Chollet section 8.3.1

- use a different data set of images.  Or, even prepare a small set of
  images randomly collected from the web, and provide it to the class.
  Or, even take some images.

- use only a couple of layers from VGG, lock the weights, and then
  train on CIFAR, and see how well that works.)
