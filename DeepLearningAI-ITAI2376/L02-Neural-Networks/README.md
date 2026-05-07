# Lab 01 - Image Classification

## Overview
This project demonstrates image classification using a pre-trained deep learning model (VGG16). The model is capable of identifying objects in images by using features learned from the ImageNet dataset.

## Objective
The goal of this lab is to understand how pre-trained convolutional neural networks (CNNs) can be used for image recognition without training a model from scratch.

## Tools & Technologies
- Python
- TensorFlow / Keras
- VGG16 (ImageNet pre-trained model)
- NumPy
- Matplotlib
- PIL (Pillow)
- Jupyter Notebook

## How It Works
1. Load a pre-trained VGG16 model
2. Upload an image
3. Resize and preprocess the image (224x224)
4. Convert image into numerical array
5. Feed image into the model
6. Get top 3 predictions with confidence scores

## Key Concepts Learned
- Transfer learning
- Image preprocessing for CNNs
- Pre-trained deep learning models
- Image classification pipeline

## Results
The model successfully predicts objects in images with high accuracy. For example, a cat image was classified as "Egyptian cat" with high confidence (~90%).

## Example Output
- Egyptian cat – 90%
- Tabby cat – 5%
- Lynx – 2%

## Conclusion
This lab shows how powerful pre-trained models like VGG16 are for image recognition tasks. Proper preprocessing is essential for accurate predictions.
