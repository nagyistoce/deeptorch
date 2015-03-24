# Introduction #

Two main programs are being provided. A straighforward implementation of denoising stacked auto-encoders, called `stacked_autoencoder_main`, implements fully connected neural networks with an arbitrary (=size of your RAM) number of layers and hidden units. It does pre-training of these networks using the unsupervised **denoising criterion** (see RelevantPublications for more info on that).

A more experimental model is `mentoring`, which is a basic implementation of the collective learning idea, described in BackgroundInformation. In this case, only two networks are trained, one after another, with a communication phase in between.

# `stacked_autoencoder_main.cc` #

A program can can do the following steps (in this sequence):

  1. Train in a layer-wise fashion a stacked denoising auto-encoder.
  1. Train jointly **all** the layers of the said autoencoder
  1. Train jointly **all** the layers of the said autoencoder with, optionally, a supervised criterion added to the training at the same time.
  1. Optimize the network via supervised backprop.

All these steps are optional. Note that the model can easily be transformed into a regular Multi-Layer Perceptron by simply setting the variables `max_iteru_lwu`, `max_iter_uc` and `max_iter_ac` to 0. This will have the effect of initializing the weights of the network to some small random values and performing supervised backprop for `max_iter_sc` epochs.

# `mentoring.cc` #

A program can can do the following steps (in this sequence):

  1. Train jointly **all** the layers of a stacked denoising auto-encoder (the **mentor**).
  1. Optimize the **mentor** via supervised backprop.
  1. Minimize a communication cost between **mentor** and the **student**. The latter is a stacked denoising auto-encoder with the same architecture as the **mentor**. During this phase, the **mentor**'s weights are fixed, except for those that are used for communicating with the student. The student's weights are optimized using backprop and a combination of unsupervised and supervised learning
  1. Train the **student** using the supervised cost.


# Postprocessing scripts #

  * Python

  * Matlab

# Advanced usage #