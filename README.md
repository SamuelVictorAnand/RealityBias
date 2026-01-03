# Physics-Based AI Image Detector (No Deep Learning)

## Overview

AI-generated images are becoming increasingly realistic, yet they still violate subtle physical image statistics.  
This project presents a **physics-based, explainable AI image detector** that distinguishes **real photographs** from **AI-generated images** without using deep learning.

The system compares **two input images** and automatically identifies:

- Which image is **REAL**
- Which image is **AI-GENERATED**

The approach is intentionally simple, transparent, and interpretable.

---

## Key Principles

- No neural networks  
- No training data  
- No metadata or watermark reliance  
- No black-box decision making  

Detection is based purely on **image physics and mathematical analysis**.

---

## Core Idea

Real-world cameras capture light governed by physical optics and sensor constraints.  
As a result, **luminance gradients** in real images show structured, directional consistency.

Diffusion-based image generators, while visually convincing, introduce:

- Isotropic gradient noise  
- Unnatural high-frequency artifacts  
- Loss of physically coherent luminance transitions  

By analyzing **luminance gradient magnitude and orientation statistics**, these differences become measurable and explainable.

---

## Methodology

1. Convert RGB images to luminance space  
2. Compute spatial gradients using numerical differentiation  
3. Analyze:
   - Gradient magnitude distribution  
   - Directional consistency  
   - Local anisotropy patterns  
4. Compare statistical coherence between the two images  
5. Classify:
   - Higher physical consistency → **REAL IMAGE**
   - Higher stochastic irregularity → **AI-GENERATED IMAGE**

---

## Why No Deep Learning?

Deep learning models:

- Require large labeled datasets  
- Are vulnerable to overfitting  
- Are difficult to interpret  

This project demonstrates that **classical image physics** can still outperform intuition when applied correctly.

---

## Results

- Deterministic and repeatable outcomes  
- Explainable decision metrics  
- No dependency on model updates or retraining  

This makes the approach suitable for:

- Academic demonstrations  
- Forensic analysis  
- Educational purposes  
- Baseline verification systems  

---

## How to Run

### 1. Open the Notebook

Run the project directly in **Google Colab** or locally via **Jupyter Notebook**.

### 2. Upload Two Images

The notebook prompts the user to upload two images for comparison.

### 3. View Output

The system reports:

- Which image is real  
- Which image is AI-generated  
- Supporting gradient statistics and visualizations  

---

## Dependencies

All required dependencies are listed in `requirements.txt`.

---

## Limitations

- Designed for **comparative detection** (two images at a time)  
- Not intended as a universal detector  
- Performance depends on image resolution and preprocessing quality  

---

## Future Work

- Extension to single-image classification  
- Frequency-domain fusion (FFT-based analysis)  
- Robustness testing across multiple generative models  

---
