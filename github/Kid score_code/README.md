# Metrics for Evaluating GANs (Pytorch)

The following GAN metrics are implemented:

Kernel Inception Distance (KID)


## Usage

Requirements:
- python3
- pytorch
- torchvision
- numpy
- scipy
- scikit-learn

To compute the KID score between two datasets with features extracted from inception net:

* Ensure that you have saved both datasets as numpy files (`.npy`) in channels-first format, i.e. `(no. of images, channels, height, width)`

```
python kid_score.py --true path/to/real/images.npy --fake path/to/gan/generated.npy --gpu ID

```
Expected output: KID score of real and synthetic images.
Expected run time for demo on a "normal" desktop computer: Several minutes.


