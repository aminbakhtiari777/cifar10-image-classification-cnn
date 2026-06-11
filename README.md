# CIFAR-10 Image Classification using Convolutional Neural Networks (CNN)

## Project Overview

This project applies a Convolutional Neural Network (CNN) to classify color images from the CIFAR-10 dataset.

The goal is to learn the fundamentals of computer vision, convolutional layers, feature extraction, and image classification using deep learning.

## Dataset

CIFAR-10 Dataset

The dataset contains 60,000 color images of size 32x32 pixels.

Training samples: 50,000

Testing samples: 10,000

Classes:

* Airplane
* Automobile
* Bird
* Cat
* Deer
* Dog
* Frog
* Horse
* Ship
* Truck

## Data Preprocessing

The images were normalized using:

```python
x_train = x_train.astype("float32") / 255.0
x_test = x_test.astype("float32") / 255.0
```

Pixel values were scaled from the range [0,255] to [0,1].

## CNN Architecture

* Conv2D (32 filters, 3x3, ReLU)
* MaxPooling2D (2x2)
* Conv2D (64 filters, 3x3, ReLU)
* MaxPooling2D (2x2)
* Flatten
* Dense (128 neurons, ReLU)
* Dense (10 neurons, Softmax)

## Model Compilation

Optimizer:

* Adam

Loss Function:

* Sparse Categorical Crossentropy

Metric:

* Accuracy

## Results

Test Accuracy:

83%

## Key Learning Outcomes

* Computer Vision Fundamentals
* RGB Image Representation
* Image Normalization
* Convolutional Neural Networks (CNN)
* Conv2D Layers
* MaxPooling Layers
* Flatten Layer
* Softmax Classification
* Model Evaluation
* Deep Learning Workflow

## Important Observation

A fully connected neural network loses spatial information after flattening the image.

CNN preserves spatial relationships between pixels and therefore performs significantly better for image classification tasks.

## Saved Model

The trained model was saved using:

```python
model.save("cifar10_cnn_model.keras")
```

## Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Matplotlib
* Scikit-Learn
