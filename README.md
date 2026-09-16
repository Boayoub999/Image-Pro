# Lab 2 – Digital Image Fundamentals
**Course:** ARTI 403 – Image Processing

## Objective
Understand how digital images are represented and manipulated in a computer through sampling, quantization, arithmetic operations, and set/logical operations.

## Topics Covered

### 1. Image Sampling and Quantization
- **Sampling**: Downsampling an image using `cv2.resize()` with a given factor to reduce spatial resolution.
- **Quantization**: Reducing the number of grayscale levels in an image using `numpy` floor operations.
- Visualized the original, sampled, and quantized images side by side using `matplotlib`.

### 2. Arithmetic Operations
- Loaded two grayscale images (`lena_gray_256.tif`, `cameraman.tif`) using `PIL`.
- Resized both images to a common size (400×400) and converted them to `numpy` arrays.
- Performed pixel-wise **addition** of the two images.

### 3. Set and Logical Operations
- Loaded two binary/grayscale images (`A.png`, `B.png`).
- Converted them to arrays and applied the **union (OR)** operation.

## Tasks
1. **Task#1** – Modify sampling factor and quantization level parameters and observe their effect on image quality (pixelation vs. false contouring).
2. **Task#2** – Perform additional operations on two images:
   - Subtraction
   - Addition with a constant value (175)
   - Set difference
   - Symmetric difference
   - Intersection

## Tools & Libraries
- Python 3, Anaconda
- Jupyter / Spyder
- OpenCV (`cv2`), NumPy, Matplotlib, Pillow (`PIL`)

## Outcome
By the end of this lab, students can explain and implement basic digital image representation concepts, including resolution/intensity trade-offs and set-based image operations.
