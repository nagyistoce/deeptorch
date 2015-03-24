This is an extension of the [Torch3](http://www.torch.ch/introduction.php) Machine Learning library for handling various types of [Deep Architectures](http://www.iro.umontreal.ca/~lisa/pointeurs/TR1312.pdf) and modifications to the standard Multi-layer Perceptrons:

  * Handles an arbitrary number of fully-connected sigmoidal layers
  * Unsupervised learning of MLPs using various reconstruction costs. Greedy layer-wise learning is available as well.
  * An implementation of the [Stacked Denoising Autoencoders](http://www-etud.iro.umontreal.ca/~larocheh/publications/icml-2008-denoising-autoencoders.pdf)
  * A preliminary implementation of [collective learning idea](http://www.iro.umontreal.ca/~bengioy/yoshua_en/research_files/collective.html), whereby a pair of networks are trained in parallel and are communicating with each other.

If you're new to this page, be sure to check out the following wiki pages:

  * InstallationInstructions
  * UsageManual
  * BackgroundInformation
  * RelevantPublications
  * BenchmarkDatasets
  * [FAQ](http://code.google.com/p/deeptorch/wiki/FAQ)

Math and diagrams describing the algorithms implemented in the code are forthcoming.