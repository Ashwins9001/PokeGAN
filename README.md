# PokeGAN

## Details
Generative Adversarial Network trained on dataset of Pokemon images, uses combination of discriminator and generator networks trained against each other. Generator produces images and assigns real class label to all. Discriminator trained seperately to classify whether an image is fake or real, then its weights are frozen and it is used alongsider generator. Discriminator takes generated images and classifies them, due to generator always classifying images as real, lots of error produced initially to significantly change model weights. ReLU activation function used to ensure model weights don't change drastically. Eventually generator weights are adjusted until it can produce better samples, at which point generator can be used solely to create unique new Pokemon.

## Overview
- [x] Create and train discriminator
- [x] Create and train generator
- [x] Create and train GAN
- [x] Sample from GAN for testing
- [x] Train GAN on colour images
- [x] Improve training results
- [x] Improve image resolution
