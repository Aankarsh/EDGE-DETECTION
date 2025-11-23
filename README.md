# Exp-6- EDGE DETECTION 
## NAME : AANKARSH J
## REG.NO: 212223233001
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
```
## Exp-6- Record-EDGE DETECTION ##
## NAME : AANKARSH J ##
## REG.NO: 212223233001 ##

import cv2
from matplotlib import pyplot as plt
img = cv2.imread('sunflower.png') 
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY) 
gray = cv2.GaussianBlur(gray, (3, 3), 0)
sobelx = cv2.Sobel(gray, cv2.CV_64F, 1, 0, ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny")
plt.axis("off")
plt.show()
```

## Output:
### SOBEL EDGE DETECTOR

#### SOBEL X:
<img width="639" height="230" alt="download" src="https://github.com/user-attachments/assets/b0210d50-5af8-415f-bf5a-b5a315b1b375" />

#### SOBEL Y:
<img width="639" height="230" alt="download" src="https://github.com/user-attachments/assets/02597d66-5394-47bc-b64f-c3a48c895481" />

#### SOBEL XY:
<img width="639" height="230" alt="download" src="https://github.com/user-attachments/assets/0b8764f1-967b-4cac-b759-eeb13ba88ebe" />

### LAPLACIAN EDGE DETECTOR

<img width="639" height="230" alt="download" src="https://github.com/user-attachments/assets/243181a8-56d5-47b4-9bc4-10604f563307" />

### CANNY EDGE DETECTOR
<img width="639" height="230" alt="download" src="https://github.com/user-attachments/assets/b1c3a888-67e4-4647-af68-96a982853293" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
