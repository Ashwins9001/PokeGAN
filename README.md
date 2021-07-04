# PokeGAN

<p align="center">
  <img src="https://github.com/Ashwins9001/PokeGAN/blob/main/Gen_Samples/PyTorch/iteration-200.png" />
</p>

## Model Architecture and Functionality
Deep Convolutional Generative Adversarial Network trained on dataset of Pokemon images, uses combination of discriminator and generator networks trained against each other. Generator produces images and assigns real class label to all. Discriminator trained seperately to classify whether an image is fake or real, then its weights are frozen and it is used alongsider generator. Discriminator takes generated images and classifies them, due to generator always classifying images as real, lots of error produced initially to significantly change model weights. ReLU activation function used to ensure model weights don't change drastically. Eventually generator weights are adjusted until it can produce better samples, at which point generator can be used solely to create unique new Pokemon.

## Model Improvements and Design Process
Initially used GAN-implementation in Keras to produce single-channel (red) colour images of the Pokemon. In retrospect a very bad idea given pixel intensities for a single color channel aren't representative of how some Pokemon actually look. Attempted to change Keras architecture to generate RGB images of Pokemon, however ran into issues with tensor dimensionality when producing generator. 

Switched over to PyTorch implementation of GAN for RGB images of Pokemon. Designing tensor dimensionality of discriminator and generator much easier in PyTorch. Generated images show the general form and colours but lack resolution and take a long time to train. 

Training GANs is very taxing due to two networks being compared and no single cost function indicative of training improvement and convergence. Often to evaluate model performance, must check if generated images are sufficient manually. In future can attempt different architecture or try tuning hyperparameters.

## Overview
- [x] Create and train discriminator
- [x] Create and train generator
- [x] Create and train GAN
- [x] Sample from GAN for testing
- [x] Train GAN on colour images
- [x] Improve training results
- [x] Improve image resolution
