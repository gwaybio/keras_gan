# Generative Adversarial Networks using Keras

*Gregory Way, University of Pennsylvania*
*Genomics and Computational Biology*

## Overview

In the following repository, I implement a traditional generative
adversarial network (GAN) using two multilayer perceptrons (MLP)
that define the generator and discriminator class. I build a model
that can generate somewhat realistic
[MNIST examples](http://yann.lecun.com/exdb/mnist/).
The architecture I use is very similar to the MLP GAN proposed by
[Goodfellow et al. 2014](https://arxiv.org/abs/1406.2661 "GAN Paper").

Essentially, a GAN plays a minmax game that pits a generative model
against a discriminative model. The generative model is trained to
draw examples from the data generating distribution and the
discriminative model is trained to detect if a given sample is real
or fake. Once both models are tuned, then the generative model can
quickly generate new and realistic samples from a random uniform
input distribution. In practice, the model trains reasonably fast
but is quite instable.

Generally, I have found batch normalization
([Ioffe and Szegedy 2015](https://arxiv.org/abs/1502.03167)) to be
essential to the training process. Without batch normalization, all
of my generated images looked exactly the same; a phenomenon also
observed by [Salimans et al. 2016](https://arxiv.org/abs/1606.03498).

## Architecture

Generator
Discriminator

* Parameters
  * Epochs:
  * Batch size: 
  * Optimizer:
    * Learning rate:
    * Learning rate decay:

## Results

Random example of MNIST images

![MNIST images](figures/random_MNIST_examples.png?raw=true)  

Random noise vectors of untrained generator

![z vector noise](figures/random_z_vectors.png?raw=true)  

Early GAN training process - shown are fixed `z` for 500 epochs
(image is every 25 epochs).

![early training](figures/training_process.gif?raw=true)  

Random generated results

## Other Keras GAN repositories

Many of the functions and strategies I use are inspired by other
GAN models also implemented in Keras:

| User | Link to Repo | Model |
| ---- | ------------ | ----- |
| @osh | https://github.com/osh/KerasGAN | CNN |
| @jacobgil | https://github.com/jacobgil/keras-dcgan | CNN |
| @phreeza | https://github.com/phreeza/keras-GAN | CNN/MLP |
| @rajahkumarmp | https://github.com/rajathkumarmp/DCGAN | CNN |

If I am missing any, please add to this list!
