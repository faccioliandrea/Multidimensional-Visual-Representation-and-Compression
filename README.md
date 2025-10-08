# 🖼️ Multidimensional Visual Representation and Comooression

This repository contains the laboratory exercises developed for the **Multidimensional Visual Representation and Compression (DTA096A)** course.  
Each lab explores foundational concepts in image representation, sampling, quantization, color models, and information-theoretic analysis of images.

---

## 📘 Lab Overview

| Lab | Title | Topics | Status |
|------|-------|---------|---------|
| **Lab 1** | Visual Representation & Information Theory | Sampling, aliasing, quantization, color models, entropy, predictive coding | ✅ Completed |
| **Lab 2** | *(To be released)* | TBD | 🚧 Upcoming |
| **Lab 3** | *(To be released)* | TBD | 🚧 Upcoming |

---

## 🧩 Lab 1 — Visual Representation & Information Theory

### 🔍 Overview
This session investigates core principles of image representation and information theory. Topics include sampling and aliasing, quantization and SQNR, color models and chroma subsampling, and information measures such as entropy, mutual information, and predictive coding.

### 🧪 Key Topics
- **Sampling & Aliasing**: Nyquist theorem, anti-aliasing filters, Fourier analysis  
- **Quantization & SQNR**: Bit-depth reduction, color banding, empirical vs. theoretical SQNR  
- **Color Models & Chroma Subsampling**: Human visual system, compression trade-offs  
- **Information Theory**: Entropy, joint and conditional entropy, mutual information  
- **Predictive Coding**: Redundancy reduction, spatial correlation exploitation  

### 📈 Findings
- Anti-aliasing filters reduce artifacts but sacrifice sharpness.  
- Quantization artifacts are most visible in smooth regions (color banding).  
- Chroma subsampling is effective in smooth areas but fails near edges.  
- Natural images have high spatial redundancy, enabling efficient compression.  
- Predictive coding reduces entropy significantly (e.g., from 4.89 to 1.91 bits/pixel).

---

## 🧠 Lab 2 — *(To Be Released)*

> 🔒 **Coming soon!**  

---

## 🧭 Lab 3 — *(To Be Released)*

> 🔒 **Coming soon!**  

---

## ⚙️ Environment & Dependencies

All labs are implemented in **Python** using Jupyter Notebooks.

### Main libraries
```bash
numpy
opencv-python
scikit-image
matplotlib
