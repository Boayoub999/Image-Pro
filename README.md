# Lab 4: Intensity Transformations and Filtering - Spatial Domain

**Course:** ARTI 404 – Image Processing[cite: 5]  
**University:** Imam Abdulrahman Bin Faisal University (IAU)[cite: 5]  
**Department:** Computer Engineering[cite: 5]  
**Academic Year:** 2025 - 2026[cite: 5]  

---

## 📌 Overview
This lab covers intensity transformations, thresholding techniques, and histogram processing using Python (`OpenCV` and `scikit-image`)[cite: 5].

---

## 📂 Folder Structure
The `Lab#4` directory includes[cite: 5]:
* `Lab4_Tasks.ipynb` - Jupyter Notebook with the implemented code and plotted figures.
* `images/` - Directory for images used in tasks.
* `README.md` - Documentation file.

---

## 🛠️ Completed Tasks (Assessment)

### Task 1: Rescaling Intensity (Percentiles)
* Loaded the `moon` image from `skimage.data`[cite: 5].
* Rescaled intensity values between the **3rd and 80th percentiles** using `exposure.rescale_intensity()`[cite: 5].
* Plotted the contrast-stretched image alongside its corresponding histogram[cite: 5].

### Task 2: Histogram Equalization
* Applied `exposure.equalize_hist()` on the `moon` image to flatten/equalize its histogram[cite: 5].
* Visualized the equalized output image and its resulting flattened histogram[cite: 5].

### Task 3: Histogram Matching
* Used `chelsea` as the source image and `rocket` as the reference image from `skimage.data`[cite: 5].
* Applied `exposure.match_histograms()` to align the color profile of the source image to match the reference[cite: 5].
* Displayed the source, reference, and matched images together[cite: 5].

---

## 🚀 Tools & Libraries Used
* **Python 3**[cite: 5]
* **Jupyter Notebook**[cite: 5]
* **OpenCV (`cv2`)**[cite: 5]
* **scikit-image (`skimage.exposure`, `skimage.data`)**[cite: 5]
* **Matplotlib (`matplotlib.pyplot`)**[cite: 5]
* **NumPy**[cite: 5]

---

## 👤 Student Info
* **Course:** ARTI 404 - Image Processing[cite: 5]
