# L08 - Creating Numbers/Images with AI (Diffusion Model)

## 📌 Introduction

This project implements a diffusion model trained on the MNIST dataset to generate handwritten digits (0–9). Diffusion models work by gradually adding noise to images and then learning how to reverse that process step-by-step to reconstruct clean images from random noise.

The goal of this project is to generate recognizable handwritten digits using a U-Net-based architecture and evaluate the results using both visual inspection and CLIP scoring.

This project was developed and tested in a GPU-enabled environment (Google Colab recommended due to training and memory requirements).

---

## 🧠 What We Built

The system includes:

- A diffusion model trained on MNIST digits  
- A U-Net architecture for image generation  
- A forward diffusion process (gradual noise addition)  
- A reverse diffusion process (step-by-step denoising)  
- Time embeddings to track diffusion steps  
- Class conditioning to control digit generation (0–9)  
- CLIP-based evaluation for image quality scoring  

The model is trained using PyTorch and optimized for small-scale GPU environments.

---

## 🧠 Approach and Methodology

### 1. Forward Diffusion Process

The forward process gradually adds Gaussian noise to clean images over multiple timesteps:

:contentReference[oaicite:0]{index=0}

This allows the model to learn how images degrade into noise.

---

### 2. Reverse Diffusion Process

The model learns to reverse this process by predicting the noise at each timestep and progressively removing it to reconstruct the original image.

---

### 3. Model Architecture (U-Net)

The architecture includes:

- Downsampling blocks for feature extraction  
- Upsampling blocks for reconstruction  
- Skip connections to preserve spatial detail  
- Time embeddings to represent diffusion steps  
- Class embeddings for digit control  

This structure allows the model to both understand image structure and control output generation.

---

### 4. Training Process

The model was trained using:

- Adam optimizer  
- Mean Squared Error (MSE) loss  
- Random timestep sampling for robustness  
- Gradient clipping for training stability  
- Validation checks during training  

Training was performed on MNIST using GPU acceleration where available.

---

## 📈 Results and Evaluation

The model successfully learned the diffusion process and can generate handwritten digits from random noise. However, output quality varies significantly depending on the digit class.

### Observed Results:

- Some digits are partially recognizable  
- Many outputs remain blurry or noisy  
- Simpler digits (0, 1, 7) perform better than complex digits (8, 9)  
- Loss decreases steadily, showing learning progress  

### Key Insight:

While the model learns the general structure of digits, final outputs are still inconsistent and not always sharp enough for reliable recognition.

This indicates that the model captures the diffusion process correctly but is limited by scale, training time, and computational constraints.

---

## 🧪 CLIP Evaluation

CLIP was used to evaluate how well generated images match their intended digit labels.

### Key Findings:

- Simpler digits (0, 1, 7) achieve higher CLIP “good” scores  
- Complex digits (8, 9) often produce higher “blurry” scores  
- Some digits (especially 0) still show low confidence in CLIP scoring  
- CLIP confirms inconsistency in image quality across classes  

### Insight:

CLIP evaluation highlights that while the model generates valid outputs, the clarity and recognizability are not consistent across all digit types.

---

## ⚠️ Limitations and Challenges

Several challenges were encountered during development:

- GPU memory constraints during training and evaluation  
- Stability issues when running CLIP (mixed precision warnings)  
- Generated images often remain blurry or partially formed  
- Performance varies significantly between digit classes  

These limitations directly impacted final output quality and consistency.

---

## 📚 Learning Outcomes

From this project, I learned:

- How diffusion models progressively generate images from noise  
- How forward and reverse diffusion processes are mathematically linked  
- How U-Net architectures are used in generative AI systems  
- How time and class conditioning improve control over outputs  
- How CLIP can be used to evaluate generative model performance  
- How hardware constraints (GPU memory and compute time) affect model quality  

---

## 🚀 How the System Works (High-Level View)

1. Start with random noise  
2. Gradually remove noise step-by-step  
3. Condition generation on a digit label (0–9)  
4. Use a trained U-Net to predict noise at each step  
5. Produce a final generated handwritten digit  

This process transforms pure randomness into structured visual output.

---

## 📁 Project Summary

This project demonstrates a working diffusion model capable of generating handwritten digits from noise. While the model successfully learns the denoising process, output quality is still inconsistent due to limited training scale and computational constraints.

It highlights both the strengths of diffusion models and the challenges of training them in lightweight environments.
