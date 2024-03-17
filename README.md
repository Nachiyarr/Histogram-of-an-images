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
#### Developed by:Alagu Nachiyar k
#### Register no:212222240006
### Grayscale image and Color image:
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("cat.jpg")
color_image = cv2.imread("bird.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Histogram of Grayscale image
```
import numpy as np
import cv2
Gray_image = cv2.imread("cat.jpg")
Color_image = cv2.imread("bird.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
```
### Histogram of Color image 
```
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
###Histogram equalization of Grayscale image 
```

import cv2
gray_image = cv2.imread("bird.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/Nachiyarr/Histogram-of-an-images/assets/113497340/43aefec8-f993-4712-bf63-a5b4d3198960)
### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/Nachiyarr/Histogram-of-an-images/assets/113497340/00ec0016-d134-40ea-9cf3-aa0a8f7296af)
![image](https://github.com/Nachiyarr/Histogram-of-an-images/assets/113497340/f449959a-0a9b-443f-8682-670714c132d0)
![image](https://github.com/Nachiyarr/Histogram-of-an-images/assets/113497340/995b9920-c886-4feb-8ccf-458bd222be71)
![image](https://github.com/Nachiyarr/Histogram-of-an-images/assets/113497340/5d582a3f-5395-4bdc-9412-f711803367ea)
### Histogram Equalization of Grayscale Image.
![image](https://github.com/Nachiyarr/Histogram-of-an-images/assets/113497340/cc0a4603-d5b3-4bc5-b1db-89b1a5b6ce80)
## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
