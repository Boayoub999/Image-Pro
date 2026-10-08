# Lab 3: Image Manipulations using OpenCV Library

**Course:** ARTI 404 – Image Processing  
**University:** Imam Abdulrahman Bin Faisal University (IAU)  
**Department:** Computer Engineering  
**Academic Year:** 2025 - 2026  

---

## 📌 Overview
In this lab, I worked with the OpenCV library in Python to perform basic image manipulation tasks, geometric transformations, and intensity transformations.

---

## 📂 Folder Structure
The `Lab#3` directory contains the following files:
* `Lab3_Tasks.ipynb` - Jupyter Notebook containing all the code and outputs for the tasks.
* `images/` - Folder containing original input images (`input.jpg`) and output results.
* `README.md` - Lab overview and description.

---

## 🛠️ Tasks & Implementation Summary

### Task 1: Geometric Transformations
Applied the following geometric transformations on an input image:
1. **Resizing:** Increased the dimensions/size of the image using `cv2.resize()`.
2. **Rotation:** Rotated the image by 120 degrees using `cv2.getRotationMatrix2D()` and `cv2.warpAffine()`.
3. **Shearing:** Performed affine shearing transformations (Horizontal & Vertical) on the image.

### Task 2: Intensity Transformations
Applied point-wise intensity transformation functions:
1. **Negative Image:** Inverted pixel intensities using `cv2.bitwise_not()`.
2. **Log Transformation:** Applied $s = c \cdot \log(1 + r)$ using an appropriately calculated scaling constant $c$.
3. **Power-Law (Gamma) Transformation:** Applied $s = c \cdot r^\gamma$ with $\gamma > 1$ to increase image contrast.

---

## 🚀 Tools & Libraries
* **Python 3**
* **Jupyter Notebook**
* **OpenCV (`cv2`)**
* **NumPy**
* **Matplotlib**

---

## 👤 Student Info
* **Course:** ARTI 404 - Image Processing
