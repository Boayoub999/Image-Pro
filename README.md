# Lab 7: Laplacian Filter & Mathematical/Statistical Filters

This repository contains practical implementations for **Lab 7** of the **Image Processing** course. The lab is divided into two main parts focusing on edge enhancement using the Laplacian operator and noise reduction using various mathematical and statistical filters.

---

## 👨‍💻 Student Information
* **Name:** Mustafa Abbas Abokhadher
* **ID:** 2240002889
* **Section:** 7MA2
* **Course:** Image Processing (Fourth Year)

---

## 📂 Lab Structure & Contents

### Part A: Laplacian Filter (`Lab_7_(A)_Laplacian_Filter.ipynb`)
Focuses on image sharpening and edge detection using second-order derivative filters.
* **Loading & Grayscale Conversion:** Reads an input image (`moon.jpg`) and converts it to grayscale[cite: 2].
* **Manual Kernels:** Implements standard 4-neighbor (centre = -4) and 8-neighbor (centre = -8) Laplacian kernels[cite: 2, 4].
* **Noise Reduction Prep:** Applies optional Gaussian blur to prevent noise amplification[cite: 3].
* **Proper Sharpening:** Combines the original image with the Laplacian response using proper data type handling (`CV_64F`) and clipping (`np.clip`) to avoid overflow/underflow artifacts[cite: 4].

### Part B: Mathematical & Statistical Filters (`Lab_7_(B)_Maths_&_Statistics_Filters.ipynb`)
Focuses on artificial noise generation and restoring images using advanced spatial and statistical filters.
* **Noise Generation Functions:** Custom implementation for adding:
  * **Gaussian Noise**[cite: 6]
  * **Salt & Pepper Noise**[cite: 6]
  * **Exponential Noise**[cite: 6, 7]
  * **Uniform Noise**[cite: 7]
* **Spatial/Mean Filters:**
  * **Arithmetic Mean Filter:** Built-in (`cv2.blur`) and manual kernel implementation[cite: 8, 9].
  * **Geometric Mean Filter:** Log-transform based smoothing[cite: 10].
  * **Harmonic Mean Filter:** Reciprocal-based filtering, effective for salt noise[cite: 12].
  * **Contra-Harmonic Mean Filter:** Adjustable parameter $Q$ to selectively remove pepper ($Q > 0$) or salt ($Q < 0$) noise[cite: 13].
* **Order-Statistics Filters:**
  * **Median Filter:** Effective for impulsive (salt & pepper) noise[cite: 14].
  * **Max and Min Filters:** Using dilation and erosion morphology for extreme value selection[cite: 14, 15].
  * **Mid-Point Filter:** Averaging max and min neighborhood values[cite: 15].

---

## 🚀 Requirements & Dependencies

Make sure you have the following Python libraries installed before running the notebooks:

```bash
pip install opencv-python numpy matplotlib ipython
