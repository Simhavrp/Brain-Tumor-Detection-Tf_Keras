# Brain-Tumor-Detection-Tf_Keras
This project aims to classify brain MRI images into two categories: with tumor (positive) and without tumor (negative). The CNN model is trained to automatically detect brain tumors from MRI images.

Cropping Brain Contours:

The crop_brain_contour function isolates the brain region in an MRI image by converting the image to grayscale, applying Gaussian blur, thresholding the image, eroding and dilating to remove small blobs, finding contours, and cropping the image around the largest contour.

The load_data function reads images from specified directories, crops the brain region, resizes images to a consistent size, and normalizes pixel values. Images with a tumor are labeled as 1 and without as 0. The data is shuffled to ensure random distribution.

The split_data function splits the data into training, validation, and testing sets.

# Model Architecture:

The CNN model is built using Keras with several layers including:

Input layer

ZeroPadding2D

Convolutional layer with 32 filters

BatchNormalization

ReLU activation

MaxPooling2D

Flatten

Fully connected layer with sigmoid activation for binary classification

Training:

The model is trained using the Adam optimizer and binary cross-entropy loss. The training process includes callbacks for TensorBoard and model checkpointing.

After training, the model's performance can be visualized using training and validation metrics. Metrics such as training loss, validation loss, training accuracy, and validation accuracy are plotted to evaluate the model's performance.
