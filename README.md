## Canny-Edge-Detection-
# Aim
To perform edge detection using Canny edge detectors.

# Software Required
Anaconda – Python 3.7
Jupyter Notebook / VS Code
OpenCV (cv2)
NumPy
Matplotlib
# ⚙️ Algorithm
Step 1:
Import all the necessary modules for the program.

Step 2:
Load an image using cv2.imread().

Step 3:
Convert the image to grayscale.

Step 4:
Apply Canny edge detector using OpenCV.

Step 5:
Display all edge-detected images for comparison.

# Developed By
Name: VISHAL M
Register No: 212225240186
# PROGRAM :
# Step 1: Import all the necessary modules
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Step 2: Load an image using cv2.imread()
```
image = cv2.imread('jack and rose.jpg')

if image is None:
    raise FileNotFoundError("red.jpg was not found. Place red.jpg in the same folder as this notebook.")
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
```
# Step 3: Convert the image to grayscale
```
gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.figure(figsize=(6, 5))
plt.imshow(gray, cmap='gray')
plt.title('Grayscale Image')
plt.axis('off')
plt.show()
```
# Step 4: Apply Canny edge detector
```
canny = cv2.Canny(gray, 100, 200)
```
# Step 5: Display all edge-detected images for comparison
```
plt.figure(figsize=(15, 10))

plt.subplot(2, 3, 1)
plt.imshow(image_rgb)
plt.title('Original Image')
plt.axis('off')


plt.subplot(2, 3, 6)
plt.imshow(canny, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')

plt.tight_layout()
plt.show()
```
# Output
# Edge Detector
Multi-stage edge detection
Produces clean and thin edges

<img width="278" height="478" alt="image" src="https://github.com/user-attachments/assets/34bfe828-e881-4efd-90cc-667ffbb8f50a" />

<img width="285" height="442" alt="image" src="https://github.com/user-attachments/assets/0a7462a7-9fea-418d-a9ca-3efb304a10a8" />

<img width="263" height="438" alt="image" src="https://github.com/user-attachments/assets/71a9279e-eee2-451c-b81d-4bb0a159f2f3" />

# Result
Thus, edges are successfully detected using Canny edge detection techniques. Each method highlights edges differently based on gradient and intensity variations, improving feature extraction and analysis.
