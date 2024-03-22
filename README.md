# Histogram-of-an-images
## Aim:
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
# Developed By: Hari Prasath. P
# Register Number: 212223230070

import cv2
import matplotlib.pyplot as plt

# Histogram for Gray scale and Color image
 
gray_image = cv2.imread('Thala.jpg')
color_image = cv2.imread('Thala Colour.jpg')
plt.imshow(gray_image)
plt.show()
plt.imshow(color_image)
plt.show()
hist = cv2.calcHist([gray_image],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('GrayScaleValue')
plt.ylabel('PixelCount')
plt.stem(hist)
plt.show()
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity Value')
plt.ylabel('PixelCount')
plt.stem(hist1)
plt.show()

import cv2
Gray_image=cv2.imread('Thala.jpg',0)
equ = cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image:

![Screenshot 2024-03-22 141744](https://github.com/Hari-Prasath-P-08/Histogram-of-an-images/assets/139455593/105160a6-6bda-4c13-994b-21fe6f26266a)

![Screenshot 2024-03-22 141816](https://github.com/Hari-Prasath-P-08/Histogram-of-an-images/assets/139455593/ccd4342f-c895-4aa5-9213-40502a3fd1f3)

### Histogram of Grayscale Image and any channel of Color Image:

![Screenshot 2024-03-22 141836](https://github.com/Hari-Prasath-P-08/Histogram-of-an-images/assets/139455593/aae46f49-b47d-42df-8e15-780509940e3d)

![Screenshot 2024-03-22 141858](https://github.com/Hari-Prasath-P-08/Histogram-of-an-images/assets/139455593/62a8ec5a-1558-4ba8-8f9a-f1968bae3bf8)

### Histogram Equalization of Grayscale Image:

![Screenshot 2024-03-22 142056](https://github.com/Hari-Prasath-P-08/Histogram-of-an-images/assets/139455593/06daa522-2ac1-4b50-8ca6-1bbb4b609527)

![Screenshot 2024-03-22 142114](https://github.com/Hari-Prasath-P-08/Histogram-of-an-images/assets/139455593/5ba56f29-c0a7-446f-bf63-2ecbe94a2575)

## Result:

Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
