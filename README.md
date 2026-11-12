# Lab 10: Image Segmentation and Feature Extraction

**Course:** ARTI404, Image Processing
**College of Computer Science and Information Technology, Imam Abdulrahman Bin Faisal University**
**Author:** Mustafa Abbas Abokhadher

This repository contains my solution for Lab 10. The notebook covers two classic feature-extraction techniques (Canny edges and Harris corners) and image segmentation by thresholding, including the assessment task on Otsu's method.

## Contents

| File | Description |
|---|---|
| `Lab10_Image_Segmentation_Feature_Extraction.ipynb` | The full notebook with code and outputs |
| `Lab10_Image_Segmentation_Feature_Extraction.pdf` | A PDF export of the notebook (optional) |

## What's Inside

### 1. Canny Edge Detection
Detects edges on the `camera` sample image using `cv2.Canny(img, 100, 200)`.
Canny works in five steps: Gaussian blur, gradient computation, non-maximum suppression, double thresholding, and hysteresis.
A common rule of thumb is `T_high ≈ 2×T_low` or `3×T_low`.

### 2. Harris Corner Detection
Detects corners on a resized `checkerboard` image using `cv2.cornerHarris` with `blockSize=2`, `ksize=3`, `k=0.04`.
Strong corners (response above `0.01 × max`) are marked with red dots.

| Harris response `R` | Meaning |
|---|---|
| Large positive | Corner |
| Large negative | Edge |
| Small | Flat region |

### 3. Simple (Global) Binary Thresholding
Applies a fixed threshold `T = 127` on the `coins` image with `cv2.threshold`.
Every pixel above `T` becomes white and every pixel below becomes black.

### 4. Q1: Otsu's Thresholding (Assessment Task)
Otsu's method chooses the threshold automatically by maximizing the between-class variance. It assumes the histogram has two peaks (foreground and background).

```python
T_otsu, otsu_binary = cv2.threshold(
    img, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU
)
```

The notebook displays three panels side by side: the original image, its histogram with the Otsu threshold marked, and the resulting binary image.

**Result:** Otsu selected `T = 107`, which falls in the valley between the two histogram peaks (dark background and brighter coins).

**Observation:** Because Otsu uses a single global threshold and the lighting in the image is uneven, some bright background areas in the top-right corner appear white, and a few dark details inside the coins appear black. `cv2.adaptiveThreshold` (local thresholds) is a natural fix for this.

## Summary of Techniques

| Technique | Category | What it finds | OpenCV function |
|---|---|---|---|
| Canny | Edge detection | Thin connected edges | `cv2.Canny` |
| Sobel | Edge detection | Gradient magnitude (thick) | `cv2.Sobel` |
| Laplacian | Edge detection | Zero-crossings (2nd derivative) | `cv2.Laplacian` |
| Harris | Feature extraction | Corners | `cv2.cornerHarris` |
| Shi-Tomasi | Feature extraction | Corners (improved) | `cv2.goodFeaturesToTrack` |
| Simple threshold | Segmentation | Fixed-`T` binary mask | `cv2.threshold` |
| Otsu | Segmentation | Automatic bimodal threshold | `cv2.threshold` + `THRESH_OTSU` |
| Adaptive threshold | Segmentation | Local-`T` binary mask | `cv2.adaptiveThreshold` |

## Requirements

- Python 3.9+
- opencv-python
- numpy
- matplotlib
- scikit-image
- jupyter (or any environment that can open `.ipynb` files)

Install everything with:

```bash
pip install opencv-python numpy matplotlib scikit-image jupyter ipywidgets
```

> `ipywidgets` is optional. It only removes the harmless `TqdmWarning: IProgress not found` message that can appear when importing `skimage.data`.

## How to Run

```bash
git clone <your-repo-url>
cd <your-repo-folder>
jupyter notebook Lab10_Image_Segmentation_Feature_Extraction.ipynb
```

Then run the cells from top to bottom. All images (`camera`, `checkerboard`, `coins`) come from `skimage.data`, so no external files are needed.

## Notes

- OpenCV uses **BGR** channel order, so `(0, 0, 255)` is red.
- `cv2.threshold` with `THRESH_OTSU` requires an 8-bit single-channel (grayscale) image.
