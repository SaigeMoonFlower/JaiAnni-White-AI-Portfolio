## README (Project Overview)

### Problem Statement

The goal of this project is to build a generative AI model that can create realistic images from random noise using a diffusion process. The model is trained to generate handwritten digits (0–9) by learning how to reverse noise added to images.

---

### Approach and Methodology

This project uses a Denoising Diffusion Probabilistic Model (DDPM). The system includes:

- Forward diffusion process that gradually adds noise to images
- Reverse diffusion process that learns to remove noise step-by-step
- U-Net architecture for predicting noise at each timestep
- Time embeddings to represent diffusion steps
- Class conditioning to control digit generation (0–9)
- CLIP evaluation to measure image quality and recognizability

The model is trained using Mean Squared Error (MSE) between predicted noise and actual noise.

---

### Results and Evaluation

The model successfully generates digit-like images from noise.

- Simple digits (0, 1, 7) perform better and are more recognizable
- Complex digits (8, 9) are less stable and often distorted
- CLIP evaluation shows mixed results:
  - Clear scores are higher than Good scores in many cases
  - Blurry scores remain significant for several outputs
- Overall performance shows learning but limited sharpness due to model and compute constraints

---

### Learning Outcomes

This project demonstrates understanding of:

- Diffusion models and step-by-step image generation
- U-Net architecture for generative AI
- Noise scheduling and reverse diffusion process
- Time embeddings for sequence awareness
- Class conditioning for controlled generation
- CLIP-based evaluation of generated images
- GPU memory and training limitations in deep learning systems
