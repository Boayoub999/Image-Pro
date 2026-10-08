# Lab 5: Spatial Filtering – Smoothing and Sharpening

**Course:** ARTI 404 – Image Processing[cite: 6]  
**University:** Imam Abdulrahman Bin Faisal University (IAU)[cite: 6]  
**Department:** Computer Engineering[cite: 6]  
**Academic Year:** 2025 - 2026[cite: 6]  

---

## 📌 Overview
This lab covers spatial domain filtering techniques, focusing on image smoothing (Box and Gaussian filters) and image sharpening (Laplacian filter and Unsharp Masking) using Python and OpenCV[cite: 6].

---

## 📂 Folder Structure
The `Lab#5` directory contains[cite: 6]:
* `Lab5_Tasks.ipynb` - Jupyter Notebook containing the full implementation and displayed plots[cite: 6].
* `images/` - Directory containing input and processed images[cite: 6].
* `README.md` - Lab description and documentation[cite: 6].

---

## 🛠️ Completed Tasks (Assessment)

### Task 1: 7x7 Box Filter Smoothing
* Applied a $7 \times 7$ box filter convolution using `cv2.blur()` to smooth the image[cite: 6].
* Displayed the original image and the smoothed image side by side[cite: 6].

### Task 2: Gaussian Blur Comparison
* Applied two Gaussian filters with kernel sizes of $5 \times 5$ and $21 \times 21$ using `cv2.GaussianBlur()`[cite: 6].
* Plotted the original image alongside both blurred images to visualize the effect of kernel size on smoothing[cite: 6].

### Task 3: Image Sharpening using 3x3 Laplacian Filter
Implemented sharpening following the step-by-step procedure[cite: 6]:
1. Loaded the image and converted it to `float32` normalized between 0 and 1[cite: 6].
2. Computed edges using `cv2.Laplacian()` with a $3 \times 3$ kernel[cite: 6].
3. Sharpened the image using `np.clip(image_float - laplacian, 0, 1)`[cite: 6].
4. Plotted the original image, the Laplacian output, and the final sharpened result side by side[cite: 6].

---

## 🚀 Tools & Libraries Used
* **Python 3**[cite: 6]
* **Jupyter Notebook**[cite: 6]
* **OpenCV (`cv2`)**[cite: 6]
* **NumPy**[cite: 6]
* **Matplotlib (`matplotlib.pyplot`)**[cite: 6]

---

## 👤 Student Info
* **Course:** ARTI 404 - Image Processing[cite: 6]
