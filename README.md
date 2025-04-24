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
```
# Developed By: YOGESH.V
# Register Number: 212223230250
```
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("gray.jpeg")
color_image = cv2.imread("color.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```
import numpy as np
import cv2
Gray_image = cv2.imread("gray.jpeg")
Color_image = cv2.imread("color.jpeg")
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
```
import cv2
gray_image = cv2.imread("gray.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![Screenshot 2025-04-25 005813](https://github.com/user-attachments/assets/205de28b-6a23-49db-a6d0-345ccd8eeeec)

### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2025-04-25 005035](https://github.com/user-attachments/assets/cd12b87e-898c-4ee9-8674-f6aa1d404475)
![Screenshot 2025-04-25 005119](https://github.com/user-attachments/assets/4291c71d-b585-47e6-a940-c8012002d6ac)

### Histogram Equalization of Grayscale Image.
![Screenshot 2025-04-25 005239](https://github.com/user-attachments/assets/b99d2cdd-0f0b-408c-8cc0-79603cb5d4e8)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
