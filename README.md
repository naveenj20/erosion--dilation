## NAME: NAVEEN JAISANKER
## REG. NO.: 212224110039

# Implementation-of-Erosion-and-Dilation

## Aim
To implement Erosion and Dilation using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
   
## Algorithm:

### Step1:
Initialize a blank image and add text to it using cv2.putText().

### Step2:
Create a kernel (structuring element) using np.ones() which defines the size and shape for erosion and dilation.

### Step3:
Use cv2.erode() to shrink or thin out the white areas (text) of the image.

### Step4:
Use cv2.dilate() to expand or thicken the white areas (text) of the image.

### Step5:
Show the original, eroded, and dilated images (using cv2.imshow() or save them with cv2.imwrite()).

## Program:

``` Python
import cv2
import numpy as np
from matplotlib import pyplot as plt

img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

cv2.putText(img1,'FRIDAY' ,(80,75),font,4,(255),2,cv2.LINE_AA)

kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

img_dilate=cv2.dilate(img1,kernel1)
img_erode=cv2.erode(img1,kernel1)

plt.figure(figsize=(12, 5))
plt.subplot(1,3,1)
plt.imshow(img1,cmap='gray')
plt.subplot(1,3,2)
plt.imshow(img_dilate,cmap='gray')
plt.subplot(1,3,3)
plt.imshow(img_erode,cmap='gray')
```
## Output:

### Display the input Image:

![Screenshot 2025-05-03 111858](https://github.com/user-attachments/assets/a7327a27-fcac-400a-af74-f75e89b4751d)

### Display the Eroded Image:

![Screenshot 2025-05-03 111902](https://github.com/user-attachments/assets/2b33bca7-3fbd-478b-b7e3-445093382a6c)

### Display the Dilated Image:

![Screenshot 2025-05-03 111910](https://github.com/user-attachments/assets/d5a29436-5edb-4a2d-b8cf-34c0b19f05de)

## Result
Thus, the generated text image is eroded and dilated using python and OpenCV.
