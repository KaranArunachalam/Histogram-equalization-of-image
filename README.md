# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().

### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.

## Program:
```python
# Developed By: Karan A
# Register Number: 212223230099
```
```py
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Read the image in grayscale format
img = cv2.imread('parrot.jpg', cv2.IMREAD_GRAYSCALE)

# Display the original image
plt.imshow(img, cmap='gray')
plt.title('Original Image')
plt.show()

# Compare arrays properly
assert np.array_equal(img, cv2.imread('parrot.jpg', cv2.IMREAD_GRAYSCALE))

# Apply histogram equalization
img_eq = cv2.equalizeHist(img)

# Display histograms
plt.figure(figsize=[15,4])
plt.subplot(121); plt.hist(img.ravel(), 256, range=[0,256]); plt.title('Original Histogram')
plt.subplot(122); plt.hist(img_eq.ravel(), 256, range=[0,256]); plt.title('Equalized Histogram')
plt.show()

# Display the equalized image
plt.imshow(img_eq, cmap='gray')
plt.title('Histogram Equalized Image')
plt.show()
```
## Output:
<img width="754" height="535" alt="image" src="https://github.com/user-attachments/assets/cee00c60-f1d2-48bf-a8f6-c01dff8ab956" />

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
