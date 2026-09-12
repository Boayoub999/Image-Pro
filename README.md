Here is a summary of Lab 1 suitable for a GitHub `README.md` file, covering the main objective and Tasks 2 through 4:

---

# Lab 1: Basics of Image Processing with Python

## Main Idea

The core purpose of this lab is to introduce the fundamentals of digital image representation, manipulation, and storage using Python. It demonstrates how images are loaded, saved, and processed under the hood as multi-dimensional numerical arrays (NumPy arrays) using two primary computer vision libraries: **OpenCV** and **PIL (Pillow)**.

---

## Tasks Summary (Tasks 2 – 4)

### Task 2: Loading and Visualizing Images

* **Objective:** Learn how to read image files from disk and display them visually.


* **Summary:**
* **OpenCV (`cv2`):** Reads an image file (e.g., `cameraman.tif`) directly into a NumPy array.


* **PIL (`Pillow`):** Loads an image (e.g., `lena_gray_256.tif`) as a PIL Image object.


* Both approaches utilize **Matplotlib** (`plt.imshow`) to render and display the images on screen.





### Task 3: Image Storing

* **Objective:** Save processed or modified images back to local disk storage.


* **Summary:**
* Demonstrates image export functionality using OpenCV (`cv2.imwrite`) and PIL (`img2.save`) to save image arrays/objects into different formats (e.g., `.jpg`).





### Task 4: Displaying Images as Arrays

* **Objective:** Understand the underlying numerical structure of digital images.


* **Summary:**
* Shows how OpenCV automatically stores images as `numpy.ndarray` objects, allowing inspection of their pixel values and dimensions via `.shape`.


* Demonstrates how to explicitly convert a PIL Image object into a NumPy array using `np.array()` to inspect its pixel grid structure and tensor shape.
