
# Edge Detection Using OpenCV

## Aim

To write a Python program using OpenCV to perform edge detection on an image using Sobel Edge Detection, Laplacian Edge Detection, and Canny Edge Detection techniques.

## Software Used

- Python
- Jupyter Notebook
- OpenCV (`cv2`)
- NumPy
- Matplotlib

## Algorithm

### Step 1: Import Libraries
Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2: Load the Image
- Read the input image using `cv2.imread()`.
- Convert the image into grayscale using `cv2.cvtColor()`.
- Display the original image.

### Step 3: Sobel Edge Detection
- Apply the Sobel operator in the X direction using `cv2.Sobel()`.
- Apply the Sobel operator in the Y direction using `cv2.Sobel()`.
- Combine both directional gradients using `cv2.magnitude()`.
- Display the Sobel edge detection result.

### Step 4: Laplacian Edge Detection
- Apply the Laplacian operator using `cv2.Laplacian()`.
- Use `cv2.CV_64F` as the output data type.
- Display the Laplacian edge detection result.

### Step 5: Canny Edge Detection
- Apply Canny edge detection using `cv2.Canny()`.
- Set the threshold values to 50 and 150.
- Display the detected edges.

## Program

## **Developed By:** PANDEESWARAN N

## **Register Number:** 212222430191

## **Program File:** `EXP6.ipynb`

### Step 1: Import Libraries and Load the Image

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('my.jpeg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

### Step 2: Sobel Edge Detection

```python
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```

### Step 3: Laplacian Edge Detection

```python
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```

### Step 4: Canny Edge Detection

```python
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```

## Output

### 1. Original Image
- The original input image is displayed.

<img width="341" height="397" alt="image" src="https://github.com/user-attachments/assets/d029ea31-f680-4070-963d-1b477fa159e3" />


### 2. Sobel Edge Detection
- The Sobel operator detects horizontal and vertical edges.
- The combined edge detection result is displayed.

<img width="185" height="225" alt="image" src="https://github.com/user-attachments/assets/139b3a73-af35-4cc4-9fb3-9876c6015ffc" />


### 3. Laplacian Edge Detection
- The Laplacian operator detects edges using second-order derivatives.
- The Laplacian edge detection result is displayed.

<img width="181" height="223" alt="image" src="https://github.com/user-attachments/assets/b4cb7362-8739-43dc-86b4-a9c59569a86e" />


### 4. Canny Edge Detection
- Canny edge detection identifies the edges using threshold values of 50 and 150.
- The detected edge image is displayed.

<img width="178" height="215" alt="image" src="https://github.com/user-attachments/assets/3013a468-18c5-47e6-bc45-ef0d44de726e" />

### 5. Prewitt

<img width="193" height="216" alt="image" src="https://github.com/user-attachments/assets/24854a09-f99d-49c0-bf3e-6dede2b0fded" />

### 6.Roberts

<img width="180" height="210" alt="image" src="https://github.com/user-attachments/assets/0ba06a50-c31f-4278-9d43-3239a8eea512" />


## Result

Thus, various edge detection techniques such as Sobel Edge Detection, Laplacian Edge Detection, and Canny Edge Detection were successfully implemented using OpenCV.
