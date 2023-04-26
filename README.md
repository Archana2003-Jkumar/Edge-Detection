# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the packages required 
### Step2:
Use the inbuilt functions .
### Step3:
Detect the edges using Sobel,Canny ,Laplacian techniques.
### Step4:
Display the output using matplotlib library.
### Step5:
End the program

 
## Program:

``` 
# Import the packages
# Load the image, Convert to grayscale and remove noise
 
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("cric.jpg")
img1=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
plt.imshow(img1)
plt.title("Original Image")
plt.show()

gray1=cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
plt.imshow(gray1)
plt.imshow(gray1,cmap="gray")
plt.title("Gray image")
plt.show()
```

# SOBEL EDGE DETECTOR
## SOBELx
```
sobelx = cv2.Sobel(gray1,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(15,15))
plt.subplot(1,2,1)
plt.imshow(gray1)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```

## SOBEly

```
sobely = cv2.Sobel(gray1,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(15,15))
plt.subplot(1,2,1)
plt.imshow(gray1)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
## SOBELxy
```
sobelxy = cv2.Sobel(gray1,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(15,15))
plt.subplot(1,2,1)
plt.imshow(gray1)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
# LAPLACIAN EDGE DETECTOR
```
lap=cv2.Laplacian(gray1,cv2.CV_64F)
plt.figure(figsize=(15,15))
plt.subplot(1,2,1)
plt.imshow(gray1)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```


# CANNY EDGE DETECTOR
```
canny=cv2.Canny(gray1,120,150)
plt.figure(figsize=(15,15))
plt.subplot(1,2,1)
plt.imshow(gray1)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()

```
## Output:
### Original image
![op1](https://user-images.githubusercontent.com/93427594/234475368-bdfe8208-4a46-4b8f-af2f-753925e4c209.png)
###Gray scale image
### SOBEL EDGE DETECTOR
 ![op3](https://user-images.githubusercontent.com/93427594/234475445-ddbffb44-116e-417f-8fae-1624a254475c.png)
![op4](https://user-images.githubusercontent.com/93427594/234475988-576e2a28-6d86-4162-a87b-aa6cb5db104b.png)
![op5](https://user-images.githubusercontent.com/93427594/234476076-562164c2-d71f-493a-b05c-68f4eb6ab5cf.png)

### LAPLACIAN EDGE DETECTOR
 ![op6](https://user-images.githubusercontent.com/93427594/234476084-8d9cd9c6-c037-4ce8-b331-c719e58ad5e9.png)

### CANNY EDGE DETECTOR
![op7](https://user-images.githubusercontent.com/93427594/234476096-afb91904-db41-459b-9d64-2b26eacce809.png)
 

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
