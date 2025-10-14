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

I trained a CycleGAN for 2 epochs on the Monet dataset. The model learned to transform photographs into Monet-style paintings by using **cycle consistency loss** to maintain content while transferring Monet's artistic style. After training, I generated predictions on some test images and submitted to it Kaggle for the competition. 

The CycleGAN architecture was effective for this unpaired image translation task. The generator successfully captured impressionist characteristics like soft brushstrokes and color palettes. The discriminators helped ensure generated images looked realistic in the target domain.

Challenges to training this model included the dataset imbalance (with the dataset having 300 Monet painting samples vs 7000 regular photos) and extremely long and lagging training times. I initially tried training 25 but had to bump down to 5 and finally to 2 due to the compute requirements and the system stopping and glitching. Future improvements could include training for more epochs, data augmentation, or adjusting the cycle consistency loss weight.
