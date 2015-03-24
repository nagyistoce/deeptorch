| _What's the difference between an auto-encoder and an auto-associator?_ |
|:------------------------------------------------------------------------|

We use these terms interchangeably.

| _Is this a Torch implementation of Deep Belief Networks (by Geoff Hinton et al.)?_ |
|:-----------------------------------------------------------------------------------|

No, these are two different strategies for training deep networks that have some similarities. It is not trivial to modify our code in order to obtain DBNs.

| _Is an auto-encoder basically the same thing as a Restricted Boltzmann Machine?_ |
|:---------------------------------------------------------------------------------|

Though the look the same, RBMs and auto-encoders are quite different beasts. An RBM is a generative model of the data, in which the conditional distribution of the hiddens given the inputs happens to be factorial (i.e. very much tractable). For Bernoulli hidden units, this distribution is basically a sigmoid, like the hidden units of a neural network.

This is where the similarities end. An auto-encoder is trained using a backprop + reconstruction cost (mean-squared error or cross-entropy). An RBM is usually trained using Contrastive Divergence, an approximation to the true gradient of the likelihood (which cannot be computed tractably).

| _Who's behind this project?_ |
|:-----------------------------|

  * [Pierre-Antoine Manzagol](http://www-etud.iro.umontreal.ca/~manzagop) (University of Montreal)
  * [Dumitru Erhan](http://dumitru.erhan.googlepages.com) (University of Montreal)
  * [Samy Bengio](http://bengio.abracadoudou.com/) (Google Inc.)
  * [Yoshua Bengio](http://www.iro.umontreal.ca/~bengioy) (University of Montreal)