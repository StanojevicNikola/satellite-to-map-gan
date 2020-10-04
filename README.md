# Satellite to Map GAN
Project for Computational Intelligence Course, Faculty of Mathematics

## Description

__satellite-to-map-gan__ is a Generative Adversarial Network, or GAN, model designed for general purpose image-to-image translation, in this case specialized for translating satellite image to map

The GAN architecture is comprised of a generator model for outputting new plausible synthetic images, and a discriminator model that classifies images as real (from the dataset) or fake (generated). The discriminator model is updated directly, whereas the generator model is updated via the discriminator model. As such, the two models are trained simultaneously in an adversarial process where the generator seeks to better fool the discriminator and the discriminator seeks to better identify the counterfeit images.

Model is a type of conditional GAN, or cGAN, where the generation of the output image is conditional on an input, in this case, a source image. The discriminator is provided both with a source image and the target image and must determine whether the target is a plausible transformation of the source image.

![architecture](architecture.png)
___

## Usage

The dataset is provided on the Berkley University website and can be downloaded as a 255-megabyte zip file.
* [Download Maps Dataset (maps.tar.gz)](http://efrosgans.eecs.berkeley.edu/pix2pix/datasets/maps.tar.gz)
