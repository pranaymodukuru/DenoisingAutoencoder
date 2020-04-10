# DenoisingAutoencoder

## Removing noise from scanned noisy Office documents using Convolutional Denoising Autoencoder

The Denoising Autoencoder is an extension of a classical Autoencoder,  which aims to do some spatial operation on input to match the given output. Generally an Autoencoder is trained to copy the inputs, in order to learn latent features in lower dimensional space. An Autoencoder finds its applications in dimensionality reduction.

A Denoising Autoencoder follows similar principle but they try to remove noise from the input images. These find applications in computer vision to remove noise from a noisy stream on images.

### 1. Problem Statement
Can a denoising autoencoder be used to remove stains, footprints, marks resulting from folding or wrinkles from scanned documents containing text.

![picture alt](https://github.com/pranaymodukuru/DenoisingAutoencoder/blob/master/denoiser.jpg "Denoising")

### 2. Data Description

The data used in this project is obtained from [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/index.php). The data used is [NoisyOffice](https://archive.ics.uci.edu/ml/datasets/NoisyOffice) Dataset.

The dataset consists of 18 ground truth images, and 72 noisy images i.e. each clear image simulated with 4 kinds of noise (4*18 = 72). The 72 noisy images divided into training, validation and testing sets. The 4 kinds of noises which are simulated are folded sheets, wrinkled sheets, coffee stains, and footprints. There three different fonts used in the given scanned documents, which also has different foot note sizes and emphasis.

#### Clean Document
![picture alt](https://github.com/pranaymodukuru/DenoisingAutoencoder/blob/master/imgs/data_exp.png "Clean document")

#### Document with noise
![picture alt](https://github.com/pranaymodukuru/DenoisingAutoencoder/blob/master/imgs/stains.png "Document with noise")


### 3. Approach

A Convolutional Denoising Autoencoder has been trained to remove noise from the noisy scanned documents. The evaluation metric used here is Mean Squared Error (MSE) to compare how far is the denoised image from the ground truth.

### 4. Results

#### Coffee stain removed
![picture alt](https://github.com/pranaymodukuru/DenoisingAutoencoder/blob/master/imgs/coffe_cleaned.png "Coffee stain cleaned")

#### Folds removed
![picture alt](https://github.com/pranaymodukuru/DenoisingAutoencoder/blob/master/imgs/folds_cleaned.png "Folds removed")

#### Wrinkles removed
![picture alt](https://github.com/pranaymodukuru/DenoisingAutoencoder/blob/master/imgs/wrinkles_cleaned.png "Wrinkles removed")

#### Footmarks removed
![picture alt](https://github.com/pranaymodukuru/DenoisingAutoencoder/blob/master/imgs/footmark_cleaned.png "Footmarks cleaned")

### 5. References
1. https://archive.ics.uci.edu/ml/datasets/NoisyOffice
