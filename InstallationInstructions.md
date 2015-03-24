**10/30/2009 - The current bundled versions segfault! It is necessary to:
1) use the most up to date version of the code (ie by checking it out through svn).
2) add 'deeptorch/analysis' in the list of packages in the file Torch3/Linux.cfg**

# If you have never used Torch3 #

  * Download the [archive](http://deeptorch.googlecode.com/files/Torch3_and_deeptorch_0.1_release.tar.gz) containing Torch3 and deeptorch source code.
  * Read carefully the Torch3 installation [instructions](http://www.torch.ch/documentation.php)
  * Modify the provided `Linux.cfg` configuration file to add the packages from torch that you need (including `deeptorch`, presumably).
  * Run `xmake` as per the Torch3 installation instructions.

# If you have a working installation of Torch3 #

  * Download the [Torch3 patch file](http://deeptorch.googlecode.com/files/patchfile), which contains the modifications that we made to the [Torch 3.1](http://www.torch.ch/downloads.php) release in order to accommodate our code. This patch file was generated using `diff -ur new_torch_folder old_torch_folder`
  * ChangesToTorch describes these changes.
  * Copy it in your Torch3 folder and `cd` to it.
  * Run `patch -p1 < patchfile`. `patch` might complain, just say `y` instead of `n`.
  * Download [deeptorch](http://deeptorch.googlecode.com/files/deeptorch_current_release.tar.gz), unpack it in your Torch3 folder and modify the configuration file specific to your system (`Linux.cfg` or etc.) to add the `deeptorch` package to the list of packages.

# In both cases #

  * Using `xmake`. you should compile one of the files in `deeptorch/mains` (say, `stacked_autoencoder_main.cc`) and execute it. You will need to specify 3 files containing the training, validation and test data as well as several required hyperparameters (number of hidden units, for instance).
  * Same data can be downloaded from BenchmarkDatasets
  * If the package is installed correctly, the program should run successfully and will create a directory whose name contains the list oif parameters and their values. Inside the directory, there will be several files containing various values measured during the execution (classification errors, reconstruction errors, etc).