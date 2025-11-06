# 🖼️ Multidimensional Visual Representation and Compression

This repository contains the laboratory exercises developed for the **Multidimensional Visual Representation and Compression (DTA096A)** course.  
Each lab explores foundational and advanced concepts in image representation, sampling, quantization, color models, transform coding, and entropy-based compression.

---

## 📘 Lab Overview

| Lab | Title | Topics | Status |
|------|-------|---------|---------|
| **Lab 1** | Visual Representation & Information Theory | Sampling, aliasing, quantization, color models, entropy, predictive coding | ✅ Completed |
| **Lab 2** | Transform & Entropy Coding | Entropy analysis, predictive coding, DCT vs. KLT, Huffman vs. Arithmetic coding | ✅ Completed |
| **Lab 3** | Lossy Compression & JPEG | Scalar quantization, transform coding, rate-distortion optimization, JPEG-like codec | ✅ Completed |

---

## 🧩 Lab 1 — Visual Representation & Information Theory

### 🔍 Overview
This lab introduces key principles of image representation and information theory, including sampling, aliasing, quantization, color models, and entropy-based information measures.

### 🧪 Key Topics
- **Sampling & Aliasing**: Nyquist theorem, anti-aliasing filters, Fourier analysis  
- **Quantization & SQNR**: Bit-depth reduction, color banding, empirical vs. theoretical SQNR  
- **Color Models & Chroma Subsampling**: Human visual system, compression trade-offs  
- **Information Theory**: Entropy, joint and conditional entropy, mutual information  
- **Predictive Coding**: Redundancy reduction, spatial correlation exploitation  

### 📈 Findings
- Anti-aliasing filters reduce artifacts but at the cost of sharpness.  
- Quantization errors are most visible in smooth regions.  
- Chroma subsampling effectively compresses smooth areas but degrades edges.  
- Predictive coding reduces entropy from **4.89 → 1.91 bits/pixel**, proving strong redundancy removal.

---

## 🧩 Lab 2 — Transform & Entropy Coding

### 🔍 Overview
This lab extends the study of image information content, prediction mechanisms, transform coding (DCT and KLT), and entropy coding (Huffman and Arithmetic).

### 🧪 Key Topics
- **Spatial & Inter-Image Entropy**: Entropy as a measure of variability and compressibility  
- **Predictive Coding**: Left, average, and JPEG-LS median predictors  
- **Transform Coding**: DCT vs. KLT for energy compaction and reconstruction  
- **Entropy Coding**: Huffman and Arithmetic coding efficiency  

### 📈 Findings
- Smooth images (e.g., *Moon*) show low entropy (~4.9 bits/pixel), while textured ones (*Grass*) reach ~7.3 bits/pixel.  
- Residual entropies confirm predictive models capture spatial redundancy effectively (**H(R) ≈ H(Y|X)**).  
- **KLT outperforms DCT**, achieving higher PSNR (e.g., 35.85 dB vs. 31.53 dB at 30 % coefficient retention).  
- **Arithmetic coding** matches the entropy limit perfectly (4.697 bits/symbol), while Huffman adds 0.018 bits redundancy.  

### 🧠 Conclusions
Transform and entropy coding together yield compact, decorrelated image representations.  
KLT is optimal but computationally heavier; DCT remains an efficient approximation for practical use.

---

## 🧩 Lab 3 — Lossy Compression & JPEG

### 🔍 Overview
This lab focuses on **scalar quantization, transform coding, rate–distortion optimization**, and the **implementation of a simplified JPEG-like codec**.

### 🧪 Key Topics
- **Scalar Quantization**: Trade-off between compression and image quality  
- **Transform Coding & Quantization**: DCT with uniform and JPEG-style quantizers  
- **Rate–Distortion Optimization**: Comparing uniform vs. perceptually weighted quantization  
- **Image Quality Assessment**: PSNR vs. SSIM  
- **Simplified JPEG Codec**: Implementation of full compression–decompression pipeline  

### 📈 Findings
- Lower bit depths cause banding and high MSE (e.g., **1 bit → PSNR 17.23 dB**, **6 bits → 46.33 dB**).  
- JPEG-style quantization outperforms uniform quantization, achieving better **rate–distortion efficiency**.  
  - Example: JPEG-Q (Quality 90) → **PSNR 46.9 dB at 1.32 bpp**, vs. uniform quantizer ≈ 2.6 bpp for same quality.  
- SSIM provides more perceptually aligned evaluations than PSNR.  
- The **custom JPEG-like codec** achieved:  
  - **Compression ratio:** 44.6 : 1  
  - **Storage saving:** 97.8 %  
  - **Reconstruction PSNR:** 39.5 dB  
  - **124 unique Huffman codes**

### ⚙️ Codec Pipeline
1. 8×8 DCT on image blocks  
2. Frequency-dependent quantization  
3. Zigzag scanning  
4. Run-Length Encoding (RLE)  
5. Huffman entropy coding  
6. Inverse DCT for reconstruction  

---

## ⚙️ Environment & Dependencies

All labs are implemented in **Python** using **Jupyter Notebooks**.

### Main Libraries
```bash
numpy
opencv-python
scikit-image
matplotlib
