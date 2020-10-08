# Satellite to Map GAN
Computational Intelligence Course Project at Faculty of Mathematics

## Description

__satellite-to-map-gan__ is a Generative Adversarial Network, or GAN, model designed for general purpose image-to-image translation, in this case specialized for translating satellite image to map

The GAN architecture is comprised of a generator model for outputting new plausible synthetic images, and a discriminator model that classifies images as real (from the dataset) or fake (generated). The discriminator model is updated directly, whereas the generator model is updated via the discriminator model. As such, the two models are trained simultaneously in an adversarial process where the generator seeks to better fool the discriminator and the discriminator seeks to better identify the counterfeit images.

Model is a type of conditional GAN, or cGAN, where the generation of the output image is conditional on an input, in this case, a source image. The discriminator is provided both with a source image and the target image and must determine whether the target is a plausible transformation of the source image.

![architecture](info/architecture.png)
___

## Usage

The dataset is provided on the Berkley University website and can be downloaded as a 255-megabyte zip file.
* [Download Maps Dataset (maps.tar.gz)](http://efrosgans.eecs.berkeley.edu/pix2pix/datasets/maps.tar.gz)

Download the dataset and unzip it into your current working directory. This will create a directory called “maps” with the following structure:
`maps`<br>
`├── train`<br>
`└── val`<br>
Then, run `prepare_data.py` to compress and prepare downloaded images for training, and `test_preparation.py` to check if all went well.

Training is done by running `train.py` file and all trained models are stored in `models` folder alongside with the example of translation quality at the given time.

Running the `translate_random_picture.py` will select a random image from the training dataset, translate it to a Google map, and plot the result compared to the expected image.
