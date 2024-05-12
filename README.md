# EXP-03:Histogram-of-an-images
# DATE:
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
# Developed By: SHABREENA VINCENT
# Register Number: 212222230141
```
# Grayscale image and Color image
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("dala_na.png")
color_image = cv2.imread("smillepathi.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# Histogram of Grayscale image and color image
```
import numpy as np
import cv2
Gray_image = cv2.imread("dala_na.png")
Color_image = cv2.imread("smillepathi.jpg")
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
# Histogram equalization of Grayscale image
```
import cv2
gray_image = cv2.imread("smillepathi.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image
![Screenshot 2024-03-22 091212](https://github.com/shabreenavincent/Histogram-of-an-images/assets/119475721/4bc3e79d-bdc0-439e-9107-0c0263ea80ec)
![Screenshot 2024-03-22 091226](https://github.com/shabreenavincent/Histogram-of-an-images/assets/119475721/c01a6940-c63b-420c-bd5e-1f33b6ec8569)
### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2024-03-26 102143](https://github.com/shabreenavincent/Histogram-of-an-images/assets/119475721/5ab9e8c5-e0ca-4103-9626-0e943d4349e6)
![Screenshot 2024-03-26 102153](https://github.com/shabreenavincent/Histogram-of-an-images/assets/119475721/5d952e5f-8964-47c2-a801-d210ce102413)
![Screenshot 2024-03-26 102202](https://github.com/shabreenavincent/Histogram-of-an-images/assets/119475721/d28222e3-fdc0-4c36-a160-19eb6e761664)
![Screenshot 2024-03-26 102212](https://github.com/shabreenavincent/Histogram-of-an-images/assets/119475721/9d44133a-6031-40ab-a2ee-a1811b3b162e)
### Histogram Equalization of Grayscale Image.
![Screenshot 2024-03-22 092031](https://github.com/shabreenavincent/Histogram-of-an-images/assets/119475721/a67d8613-96af-43df-95da-32b01f920e5b)
![Screenshot 2024-03-22 092042](https://github.com/shabreenavincent/Histogram-of-an-images/assets/119475721/b7849827-7b6c-4e6f-b409-46bc89f56bed)
## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
