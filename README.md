# Lab 6: Frequency Domain Filtering

This repository contains practical implementations for **Lab 6** of the **Image Processing** course, focusing on performing image filtering and edge detection operations in the frequency domain using Fast Fourier Transform (FFT).

---

## 👨‍💻 Student Information
* **Name:** Mustafa Abbas Abokhadher
* **ID:** 2240002889
* **Section:** 7MA2
* **Course:** Image Processing - ART1403 (Fourth Year)[cite: 17]

---

## 📂 Lab Structure & Contents

### Task 1: Laplacian Filter in the Frequency Domain (`Lab6_Frequency_Domain_Solution.ipynb`)
Focuses on applying a second-order derivative filter to detect edges by operating on the frequency components of an image[cite: 17].
* **Image Loading & Resizing:** Loads the standard `cameraman` grayscale image from `skimage.data` and resizes it to $256 \times 256$ pixels for efficient FFT computation[cite: 17].
* **Frequency Grid Generation:** Constructs centered frequency coordinates ($u, v$) using image dimensions[cite: 17].
* **Laplacian Filter Formulation:** Computes the frequency-domain filter expression: 
  $$\text{Laplacian Filter} = -4\pi^2(u^2 + v^2)$$[cite: 17]
* **FFT & Inverse FFT:** Transforms the image using 2D FFT (`fft2`), multiplies it with the frequency filter, and reverts back via Inverse FFT (`ifft2`) to obtain the spatial edge map[cite: 17].

### Assessment Task: Sobel Filters in the Frequency Domain
Demonstrates the Convolution Theorem (spatial convolution equals frequency multiplication) using Sobel operators[cite: 18].
* **Spatial Padding & Centering:** Implements a custom function (`center_embed_kernel`) to pad small $3 \times 3$ Sobel kernels to image dimensions and shift their centers to avoid phase shifts[cite: 18].
* **Gradient Computation:** 
  * Computes horizontal edges using **Sobel-X**[cite: 18, 20].
  * Computes vertical edges using **Sobel-Y**[cite: 18, 20].
  * Combines both gradients to calculate the final **Gradient Magnitude Map** ($\sqrt{G_x^2 + G_y^2}$)[cite: 19, 20].
* **Spatial Domain Verification:** Verifies frequency-domain results against true circular convolution using `scipy.ndimage.convolve`, achieving a negligible error margin of $\approx 10^{-15}$[cite: 20].

---

## 🚀 Requirements & Dependencies

Make sure you have the following Python libraries installed before running the notebook:

```bash
pip install numpy matplotlib scikit-image scipy
