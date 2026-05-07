# CNN Image Classification – Puppy vs Bagel

## Overview
This project uses Convolutional Neural Networks (CNNs) to classify images as either a puppy or a bagel using a binary classification model. It explores both custom CNN architecture and transfer learning using pre-trained models such as ResNet50 and MobileNetV2.

---

## Problem Statement
The goal is to build a deep learning model that can accurately distinguish between visually similar classes (puppies vs bagels), demonstrating how CNNs extract meaningful features from images.

---

## Approach and Methodology
- Built a custom CNN from scratch using TensorFlow/Keras
- Applied convolutional layers, pooling layers, and dense layers
- Used data augmentation to improve generalization
- Applied transfer learning using ResNet50 and MobileNetV2
- Fine-tuned pre-trained models for improved performance
- Compared results between custom CNN and transfer learning models

---

## Results and Evaluation
- Custom CNN achieved baseline performance
- Transfer learning significantly improved accuracy
- MobileNetV2 provided faster training with lower memory usage
- ResNet50 achieved higher accuracy but required more compute

---

## Key Learnings
- CNNs are effective for image feature extraction
- Transfer learning improves performance on small datasets
- Fine-tuning pre-trained models can boost accuracy
- Model selection depends on compute vs performance trade-offs

---

## Files in This Project
- cnn_model.ipynb → Main implementation notebook
- results/ → Training graphs and evaluation outputs
- images/ → Sample predictions and visuals
