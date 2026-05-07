# L05 RNNs vs Transformers vs Vision Transformers

## Overview
This project explores and compares three major deep learning architectures: Recurrent Neural Networks (RNNs), Transformer-based models (BERT), and Vision Transformers (ViT). The goal is to understand their performance differences, training behavior, and practical use cases across text and image tasks.

---

## Problem Statement
The objective of this lab is to implement and compare multiple deep learning architectures in order to analyze their strengths and weaknesses in sequence modeling and image classification tasks.

---

## Models Implemented
- Vanilla RNN (from scratch)
- GRU (Gated Recurrent Unit)
- LSTM (baseline model provided in lab)
- DistilBERT (Transformer-based NLP model)
- Vision Transformer (ViT)

---

## Approach and Methodology
- Implemented RNN-based models for text classification
- Built GRU and Vanilla RNN architectures from scratch
- Fine-tuned pre-trained Transformer (BERT)
- Fine-tuned Vision Transformer (ViT) for image classification
- Conducted hyperparameter experiments (hidden size, dropout, learning rate)
- Compared model performance across all architectures

---

## Results and Observations
- Transformer-based models achieved higher accuracy than RNN-based models
- GRU performed slightly better than Vanilla RNN and LSTM
- Vision Transformer achieved the highest performance on image classification
- Hyperparameter tuning significantly impacted model stability and accuracy

---

## Key Learnings
- RNNs suffer from vanishing gradient problems in long sequences
- GRU and LSTM improve sequence learning with gating mechanisms
- Transformers outperform RNNs on most NLP tasks
- Vision Transformers can compete with CNN-based models
- Model performance depends heavily on architecture and tuning choices

---

## Project Status
This project was fully implemented and executed in a Jupyter Notebook environment. Some components required debugging and iterative fixes, particularly around dataset handling and model execution flow.

All models were implemented and tested within the lab environment, with results documented through training outputs, visualizations, and comparison tables.

---

## Files in This Project
- L05_RNN_Transformers.ipynb → Main lab notebook
- results/ → Accuracy plots, comparison charts
- images/ → Attention maps and visual outputs
