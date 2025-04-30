# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:
### Developed By: Yathin Reddy T
### Reg.No: 212223100062
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('EAGLE.jpg') 
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
![Screenshot 2025-04-29 135121](https://github.com/user-attachments/assets/5052b2d8-b86e-461a-9f64-8730012ae96c)


### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
![Screenshot 2025-04-29 135133](https://github.com/user-attachments/assets/50b04e9b-0f8e-4abe-882d-296b97b02f28)


### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
![Screenshot 2025-04-29 135143](https://github.com/user-attachments/assets/60485f00-6170-487b-8a0a-c2f303765521)


### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
![Screenshot 2025-04-29 135150](https://github.com/user-attachments/assets/db155e94-49bc-4075-9b01-4fd6e091b96b)



## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
