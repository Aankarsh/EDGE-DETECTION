# EX 6 EDGE-DETECTION
## Name: ALDRIN.S
## Reg.no: 212223240005

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
Developed by : ALDRIN S
Reg no : 212223240005

import cv2
import matplotlib.pyplot as plt
img=cv2.imread("bui.png")
gray=cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
gray = cv2.GaussianBlur(gray,(3,3),0)
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
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
<img width="816" height="289" alt="image" src="https://github.com/user-attachments/assets/778edeb6-eaf6-46c7-bc53-d1067deda29c" />

#### SOBEL Y:
<img width="818" height="283" alt="image" src="https://github.com/user-attachments/assets/f0b7bdbe-6294-4977-8bfb-d6ad8f5a0ca3" />

#### SOBEL XY:
<img width="835" height="285" alt="image" src="https://github.com/user-attachments/assets/b16274ef-9c6c-445a-a219-ec7044102b27" />

### LAPLACIAN EDGE DETECTOR
<img width="848" height="278" alt="image" src="https://github.com/user-attachments/assets/2badba1e-a235-4837-ba60-dab68c1c223e" />

### CANNY EDGE DETECTOR
<img width="847" height="296" alt="image" src="https://github.com/user-attachments/assets/fb19a1c2-098b-4557-b47b-5378ec79ad54" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
