# Monet Style Transfer with CycleGAN

This project uses a CycleGAN to transform photographs into Monet-style paintings. Built for a Kaggle competition on generative adversarial networks.

## Project Overview

I used a CycleGAN architecture to perform unpaired image to image translation, converting regular photos into images that mimic the impressionist painting style of Claude Monet.

## Dataset

- 300 Monet paintings (256 x 256 RGB)
- 7038 normal photographs (256 x 256 RGB)
- Source: Kaggle GAN Competition

## Model Architecture

**CycleGAN Components:**
- Two Generators (U-Net architecture w/ skip connections)
- Two Discriminators (PatchGAN)
- Cycle consistency loss for reversible transformations
- Identity loss for color preservation

**Training:**
- 2 epochs
- Adam optimizer (learning rate: 2e - 4)
- Batch size: 1

## Results

I sucessly trained the model and the generator was able to apply the Monet-style characteristics to the nomral photos.

