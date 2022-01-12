# denoising-autoencoder
A convolutional autoencoder for denoising images.

The input images used here is a subset of malayalam handwritten characters, whole dataset available [here](https://drive.google.com/file/d/0B1eLyjUeuERZSkFpUlpLZVJYWkk/view?resourcekey=0-MlMJGG31g8S9O-BFfIrlRw). Input images are clean, Salt and Pepper noise is then added to the images, and the convolutional autoencoder model trained upon this noisy data to be mapped to its respective clean images.
The noise is added to 300 images from each of the 15 characters (total 4500 images) using the function random_noise from skimage. The images which were initially 86x86x3 are reshaped to 64x64x1. The train and validation split is done in the ratio 80:20. After training, the model was tested on images not involved in training/validation as well.
Summary of the symmetric structure of the constructed convolutional autoencoder and details of the results obtained can be found [here](https://github.com/naveena-as/denoising-autoencoder/blob/main/Summary.pdf).
