# Implementation-of-filter :
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1 :
Import the required libraries.

### Step2 :
Convert the image from BGR to RGB.

### Step3 :
Apply the required filters for the image separately.

### Step4 :
Plot the original and filtered image by using matplotlib.pyplot.

### Step5 :
End the program.
## Program:
### Developed By   : MAMTHA I
### Register Number: 212222230076


### 1. Smoothing Filters

i) Using Averaging Filter :
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("NATURE.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()




```
ii) Using Weighted Averaging Filter :
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()





```
iii) Using Gaussian Filter :
```Python

gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()







```

iv) Using Median Filter :
```Python

median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()







```

### 2. Sharpening Filters :
i) Using Laplacian Kernal
```Python

kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()







```
ii) Using Laplacian Operator :
```Python



laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()





```

## OUTPUT:
### 1. Smoothing Filters :


i) Using Averaging Filter :

![image](https://github.com/Mamthaiyappaprabu/Implementation-of-filter/assets/119393563/5749f12d-1e4c-4146-9802-d263dd727f80)



ii) Using Weighted Averaging Filter :

![image](https://github.com/Mamthaiyappaprabu/Implementation-of-filter/assets/119393563/c1436a04-e6b9-45b5-8944-87836cb01dcc)


iii) Using Gaussian Filter :

![image](https://github.com/Mamthaiyappaprabu/Implementation-of-filter/assets/119393563/405f99f4-73d5-4522-a47a-ab829bad8cd1)


iv) Using Median Filter :

![image](https://github.com/Mamthaiyappaprabu/Implementation-of-filter/assets/119393563/536b8b15-d275-4c8a-bc0f-d0b7f92bbc30)



### 2. Sharpening Filters :


i) Using Laplacian Kernal :

![image](https://github.com/Mamthaiyappaprabu/Implementation-of-filter/assets/119393563/7ebecd3c-2e3c-4023-8ff0-1ff8cf43db4b)


ii) Using Laplacian Operator :

![image](https://github.com/Mamthaiyappaprabu/Implementation-of-filter/assets/119393563/f1fa0e9e-cc4c-42c6-922c-bc66f134cbd3)



## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
