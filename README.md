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
# Developed By: Sathish R
# Register Number:212222230138
```
### Input Grayscale Image and Color Image
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("d9178b1598964e82acc305e41a945a90.jpg")
color_image = cv2.imread("tulip-flower-bloom-pink.webp",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Histogram of Grayscale Image and any channel of Color Image
```
import numpy as np
import cv2
Gray_image = cv2.imread("d9178b1598964e82acc305e41a945a90.jpg")
Color_image = cv2.imread("tulip-flower-bloom-pink.webp")
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
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
### Histogram Equalization of Grayscale Image.
```

import cv2
gray_image = cv2.imread("tulip-flower-bloom-pink.webp",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Input Grayscale Image and Color Image
![Screenshot 2024-03-05 191018](https://github.com/Mathiofficial/Histogram-of-an-images/assets/118787327/f6d4c2d4-b51d-4adc-9bc8-90630da5b25c)


### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2024-03-05 191518](https://github.com/Mathiofficial/Histogram-of-an-images/assets/118787327/f572eb52-da5b-4f77-809d-c140dbb0bf87)
![Screenshot 2024-03-05 191537](https://github.com/Mathiofficial/Histogram-of-an-images/assets/118787327/370daae0-b611-49d3-a081-5910e9df20be)
![Screenshot 2024-03-05 191550](https://github.com/Mathiofficial/Histogram-of-an-images/assets/118787327/c42b946b-ce79-4089-bb60-278141675527)
![Screenshot 2024-03-05 191607](https://github.com/Mathiofficial/Histogram-of-an-images/assets/118787327/e50e3169-ff5e-4521-a807-8204316814bd)


### Histogram Equalization of Grayscale Image.
![Screenshot 2024-03-05 191857](https://github.com/Mathiofficial/Histogram-of-an-images/assets/118787327/93b9edcf-d02b-4a7a-b221-594863764c71)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
