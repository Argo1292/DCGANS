DCGAN - Deep Convolutional Generative Adversarial Network
This repository contains the implementation of a Deep Convolutional Generative Adversarial Network (DCGAN) for generating realistic face images using the CelebA dataset. The project is implemented in PyTorch and supports both training and fine-tuning of the GAN model.

Table of Contents
Installation
Dataset
Model Architecture
Training
Fine-Tuning
Generating Images
Results
Acknowledgments
Installation
Ensure you have Python and PyTorch installed with CUDA support (if available). Then, install the required dependencies:

pip install torch torchvision tqdm matplotlib
Dataset
The CelebA dataset is used for training the GAN model. The dataset should be in a ZIP file named celeba.zip inside the base_dir directory. The script will automatically extract the dataset if it is not already extracted.

Model Architecture
The DCGAN consists of:

Generator: A neural network with transposed convolution layers to generate realistic face images from random noise.
Discriminator: A convolutional neural network that classifies images as real or fake.
Training
To train the DCGAN model from scratch, run the script:

python train.py
The training process involves:

Initializing the models
Using Binary Cross Entropy (BCE) loss
Optimizing with Adam optimizer
Training for multiple epochs (default: 3 epochs)
The generated images and trained models (generator.pth, discriminator.pth) will be saved in the output directory.

Fine-Tuning
To fine-tune a pre-trained model for additional epochs, run:

python fine_tune.py
This script loads pre-trained model weights and trains the network for an additional 10 epochs by default.

Generating Images
To generate new face images using the trained generator:

python generate.py
The script generates and saves sample images in the generated folder. The images will also be displayed using Matplotlib.

Results
Generated images will be saved in the output and generated directories. The quality of images improves as the model is trained for more epochs.

Acknowledgments
This implementation is based on the DCGAN paper: Radford et al., "Unsupervised Representation Learning with Deep Convolutional Generative Adversarial Networks"
Dataset: CelebA - Large-scale CelebFaces Attributes Dataset
