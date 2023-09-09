# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import cv2 and matplotlib.pyplot
<br>

### Step2:
Read and display the input images
<br>

### Step3:
Calculate the Histogram Values using calcHist()
<br>

### Step4:
Display the histograms
<br>

### Step5:
Calculate and display the equalized image using equalizeHist()
<br>

## Program:
```python
# Developed By:Kavinesh M
# Register Number:212222230064
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.
Gray_image = cv2.imread('gray.png')
Color_image = cv2.imread('d.jpg')
plt.imshow(Gray_image)
plt.show()
plt.imshow(Color_image)
plt.show()

# Display the histogram of gray scale image and any one channel histogram from color image
hist = cv2.calcHist([Gray_image], [0], None, [256], [0, 256])
hist1 = cv2.calcHist([Color_image], [1], None, [256], [0, 256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()
plt.figure()
plt.title("Histogram")
plt.xlabel('color value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()

# Write the code to perform histogram equalization of the image. 
Gray_image=cv2.imread('gray.png',0)
equ = cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image', Gray_image)
cv2.imshow('Equalized Image', equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/kavinesh8476/HISTOGRAM/assets/118466561/591c9c85-f25e-4e45-97cd-8b971b9ae37f)
<br>

### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/kavinesh8476/HISTOGRAM/assets/118466561/6537032b-e835-45e6-b6d1-669baceea677)
<br>
![image](https://github.com/kavinesh8476/HISTOGRAM/assets/118466561/733a45de-4ac4-4e68-b9db-2562f6969ef7)
<br>

### Histogram Equalization of Grayscale Image
![4gray](https://github.com/kavinesh8476/HISTOGRAM/assets/118466561/c7c467b0-0f24-4688-926e-3758c8aec404)
<br>
![4equa](https://github.com/kavinesh8476/HISTOGRAM/assets/118466561/14457042-0a2b-4762-8435-67146b2f0e3f)
<br>

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
