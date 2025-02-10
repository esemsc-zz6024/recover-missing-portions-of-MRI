# recover-missing-portions-of-MRI
## Project description

The goal of project is to solve an imputation problem: we will create a neural network architecture that learns how to recover missing portions of an image.

This is an important problem in magnetic resonance imaging (MRI), where patient scans are often limited to a few areas to avoid lengthy scanning times.

In particular, we are going to focus on images of human heads. We have managed to gain access to one hundred images of patient's heads but, unfortunately, these images have a significant portion of missing information. Your goal during the assessment is to design a neural network that can recover these missing portions.

This project do not have access to the labels for the images we want to recover, so I had a bit creative to obtain a workable dataset on which to train our neural network.

The corrupted images that we want to recover are contained in the numpy file `test_set.npy` of this repository. The file contains 100 patient images with a size of 64x64 pixels.

The architecture that you design in this assessment should use the artificially-generated dataset in order to recover the missing information in the images contained in `test_set.npy`.

## Dataset
This project have access to a generative model that has been trained to produce realistic-looking MRI images of patient's heads. So I used the provided image-generation network to create a dataset of brain images as the training dataset which is called 'train_data_3000.pt'. This training dataset includes 3000 samples.

## Network construction
Unet combined with multi-head self-attention mechanism

## Model performance
| **Dataset** | **LOSS** | **SSIM** |
| :------------------ | :---: | :---: |
| *training* | 0.0003 | 0.9568 |
| *val* | 0.0004 | 0.9507 |











