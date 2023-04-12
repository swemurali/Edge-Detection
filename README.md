# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

### Step1:
Import the necessary modules.

### Step2:
For performing edge detection on a image.

Sobel
Laplacian
Canny

### Step3:
Display all the images with their respective edge detected images.

 
## Program:

``` 
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread ('images.jpg') 
gray_image = cv2.cvtColor(image1,cv2.COLOR_BGR2GRAY)

plt.title('GRAY IMAGE')
plt.imshow(gray_image,cmap = 'gray')

img = cv2.GaussianBlur(gray_image,(3,3),0)
sobelx = cv2.Sobel(gray_image,cv2.CV_64F,1,0,ksize=5)
sobely = cv2.Sobel(gray_image,cv2.CV_64F,0,1,ksize=5)
sobelxy =cv2.Sobel(gray_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(1)
plt.subplot(2,2,1)
plt.imshow(gray_image,cmap = 'gray')
plt.title('Original'), plt.xticks([]), plt.yticks([])

plt.subplot(2,2,2)
plt.imshow(sobelx,cmap='gray')
plt.title('sobelx')
plt.xticks([]), plt.yticks([])

plt.subplot(2,2,3)
plt.imshow(sobely,cmap='gray')
plt.title('sobely')
plt.xticks([]), plt.yticks([])

plt.subplot(2,2,4)
plt.imshow(sobelxy,cmap='gray')
plt.title('sobelxy')
plt.xticks([]), plt.yticks([])
plt.show()
# cv2.waitKey(0)
laplacian = cv2.Laplacian(gray_image,cv2.CV_64F)
plt.imshow(laplacian,cmap='gray')
plt.title('laplacian')
plt.show()

canny_edges = cv2.Canny(gray_image, 120, 150)
plt.imshow(canny_edges,cmap='gray')
plt.title('canny_edges')
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR
![a](https://user-images.githubusercontent.com/94165336/231409892-b05f7750-81f9-415e-81f1-5ad0a42653ed.png)

![b](https://user-images.githubusercontent.com/94165336/231410160-fe21ec1b-5cf4-4bbc-82d4-db3e01417e84.png)

![c](https://user-images.githubusercontent.com/94165336/231410225-6014802a-be32-45ea-a11a-de1b2403dc07.png)

![d](https://user-images.githubusercontent.com/94165336/231410310-7948a7b5-2f66-4864-b903-273dc8ce21bf.png)

![e](https://user-images.githubusercontent.com/94165336/231410362-9b3e1b0a-d4d4-433d-8589-90dd9dc03dab.png)


### LAPLACIAN EDGE DETECTOR

![f](https://user-images.githubusercontent.com/94165336/231410428-1d22d641-77aa-4473-9698-abccef77ae94.png)


### CANNY EDGE DETECTOR

![g](https://user-images.githubusercontent.com/94165336/231410491-a7656d18-710a-4c35-bcbc-5d577364e30e.png)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
