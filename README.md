# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm
## Step1:
Load the necessary packages.

## Step2:
Read the Image and convert to grayscale.

## Step3:
Use Global thresholding to segment the image.

## Step4:
Use Adaptive thresholding to segment the image.

## Step5:
Use Otsu's method to segment the image and display the results.

## Program

```python
# Name: Jothilakshmi P
# Reg no: 212223110017
# Load the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt




# Read the Image and convert to grayscale
image = cv2.imread("D:\DIPT\images (1).jpg")  # Replace with your image file path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)  # Convert to grayscale
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert from BGR to RGB for display
plt.title("Original Image")
plt.axis('off')





# Use Global thresholding to segment the image
_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)




# Use Adaptive thresholding to segment the image
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)



# Use Otsu's method to segment the image 
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)




# Display the results
# Global Thresholding
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')

# Adaptive Thresholding
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')

# Otsu's Method
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')

# Show the plot
plt.tight_layout()
plt.show()




```
## Output

### Original Image

<img width="893" height="312" alt="image" src="https://github.com/user-attachments/assets/33957670-0cc2-422a-aad4-322354a5b6e0" />


### Global Thresholding

<img width="811" height="297" alt="image" src="https://github.com/user-attachments/assets/9f306af3-769f-46bb-ba64-e66e6959be40" />

### Adaptive Thresholding

<img width="949" height="316" alt="image" src="https://github.com/user-attachments/assets/eec240f5-7d40-420e-960b-76d76c83323b" />

### Optimum Global Thesholding using Otsu's Method

<img width="973" height="320" alt="image" src="https://github.com/user-attachments/assets/e6394baa-4528-4dfb-a164-4adb8c18450c" />

## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
