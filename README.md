# EXP-NO-6 EDGE-DETECTION
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
```
DEVELOPED BY : AANKARSH J
REG NO : 2122232333001
```
## Program :
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('sunflower.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
![Sunflowers_sunflower](https://github.com/user-attachments/assets/6f444961-561f-4007-a94d-e85c99e8c5cc)



### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
![sobel_edge_sunflower](https://github.com/user-attachments/assets/fbb4904f-ff98-4a40-9570-a94705dbc82f)


### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
<img width="1405" height="964" alt="image" src="https://github.com/user-attachments/assets/dfe87678-e7aa-46c8-afa3-fafc43ad3459" />

### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
<img width="1405" height="964" alt="image" src="https://github.com/user-attachments/assets/70638937-46d0-4f07-9f28-50119cc8294d" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
