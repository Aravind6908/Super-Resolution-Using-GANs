# Super-Resolution of Images Using GANs

This project demonstrates the use of Generative Adversarial Networks (GANs) for image super-resolution. The goal is to upscale low-resolution images to high-resolution versions, enhancing their quality and detail. The implementation is based on Super-Resolution GANs (SRGANs) and employs modern techniques like adversarial training, perceptual loss, and VGG-based feature extraction.

## Features
- **Generator**: A convolutional neural network (CNN) that upscales low-resolution images.
- **Discriminator**: A CNN that distinguishes between real and generated high-resolution images.
- **Loss Functions**:
  - Adversarial Loss: Ensures generated images are realistic.
  - VGG Loss: Focuses on high-level features and textures.
  - MSE Loss (optional): Measures pixel-wise differences.

## Key Components
1. **Data Loading and Preprocessing**:
   - High-resolution images are used as targets.
   - Low-resolution images are downscaled versions of high-resolution images.
   - Augmentation techniques include cropping, flipping, and rotation.

2. **Model Architecture**:
   - **Generator**: Contains convolutional layers, residual blocks, and upsampling layers.
   - **Discriminator**: Classifies real vs. fake images using convolutional layers.

3. **Training**:
   - Uses adversarial training to improve image quality.
   - Periodically saves checkpoints and generated images for monitoring.

4. **Evaluation**:
   - Generates high-resolution images from test data.
   - Visualizes results using the `plot_examples` function.

## Datasets
This project utilizes publicly available datasets for training and evaluation:

1. [NTIRE2017 Dataset](https://github.com/LimBee/NTIRE2017)
2. [DIV2K Dataset for Super-Resolution](https://www.kaggle.com/datasets/takihasan/div2k-dataset-for-super-resolution/data)

## Prerequisites
- Python 3.x
- Required Libraries:
  - `torch`
  - `torchvision`
  - `numpy`
  - `matplotlib`

