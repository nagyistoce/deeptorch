# MNIST #

As described [here](http://yann.lecun.com/exdb/mnist/), this is the standard digit classification benchmark. The archive containing the training, validation and test file can be downloaded from [here](http://www-etud.iro.umontreal.ca/~erhandum/files/mnist.tar.gz). The archive contains 3 files, each of them having 785 columns (28x28 grayscale pixel values followed by the label, 0 to 9):

  1. `mnist_train.txt`: 50,000 examples
  1. `mnist_valid.txt`: 10,000 examples
  1. `mnist_test.txt`: 10,000 examples

`mnist_test.txt` contains the same examples as the official test file.

# Flick-10,50,500 #

Image classification dataset:

  * Description with samples
  * Script to scrape the data
  * Links to downloadable versions (Torch and non-Torch)