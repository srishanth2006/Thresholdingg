## Thresholdingg
## Name : SRISHANTH J
## Reg No : 212223240160

## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Load the necessary packages.

### Step2:
Read the Image and convert to grayscale.

### Step3:
Use Global thresholding to segment the image.

### Step4:
Use Adaptive thresholding to segment the image.

### Step5:
Use Otsu's method to segment the image and display the results.

## Program
```
Name : SRISHANTH J
Reg no : 212223240160

```

### Load the necessary packages
```py
import numpy as np
import matplotlib.pyplot as plt
import cv2
```
### Read the Image and convert to grayscale
```py
image = cv2.imread("disney.jpg",1)
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
image_gray = cv2.imread("disney.jpg",0)
```
### Use Global thresholding to segment the image
```py
ret,thresh_img1=cv2.threshold(image_gray,86,255,cv2.THRESH_BINARY)
ret,thresh_img2=cv2.threshold(image_gray,86,255,cv2.THRESH_BINARY_INV)
ret,thresh_img3=cv2.threshold(image_gray,86,255,cv2.THRESH_TOZERO)
ret,thresh_img4=cv2.threshold(image_gray,86,255,cv2.THRESH_TOZERO_INV)
ret,thresh_img5=cv2.threshold(image_gray,100,255,cv2.THRESH_TRUNC)
```
### Use Adaptive thresholding to segment the image
```py
thresh_img7=cv2.adaptiveThreshold(image_gray,255,cv2.ADAPTIVE_THRESH_MEAN_C,cv2.THRESH_BINARY,11,2)
thresh_img8=cv2.adaptiveThreshold(image_gray,255,cv2.ADAPTIVE_THRESH_GAUSSIAN_C,cv2.THRESH_BINARY,11,2)
```
### Use Otsu's method to segment the image 
```py
ret,thresh_img6=cv2.threshold(image_gray,0,255,cv2.THRESH_BINARY+cv2.THRESH_OTSU)
```
### Display the results
#### ORIGIONAL IMAGE
```py


plt.axis("off")
plt.title("Original Image")
plt.imshow(image)

```
![image](https://github.com/user-attachments/assets/8dc09b3c-3cc1-4c09-a583-5d3f8aaf3d1c)

#### GREY IMAGE
```py


plt.axis("off")
plt.title("Gray Image")
plt.imshow(cv2.cvtColor(image_gray, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()
```
![image](https://github.com/user-attachments/assets/dd62748d-a746-4bf5-98d5-deefdcff2b7e)

#### Threshold Image (Binary)
```py


plt.axis("off")
plt.title("Threshold Image (Binary)")
plt.imshow(cv2.cvtColor(thresh_img1, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
![image](https://github.com/user-attachments/assets/e5c88c77-5cc1-4ee3-8328-e028270dfab0)


#### Threshold Image (Binary Inverse)
```py


plt.axis("off")
plt.title("Threshold Image (Binary Inverse)")
plt.imshow(cv2.cvtColor(thresh_img2, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
![image](https://github.com/user-attachments/assets/296e1db7-b7d9-4b65-b612-0d95abe591cb)


#### Threshold Image (To Zero)
```py


plt.axis("off")
plt.title("Threshold Image (To Zero)")
plt.imshow(cv2.cvtColor(thresh_img3, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
![image](https://github.com/user-attachments/assets/62c18fbd-4eeb-42c1-add5-6604f5fc4856)

#### Threshold Image (To Zero-Inverse)
```py


plt.axis("off")
plt.title("Threshold Image (To Zero-Inverse)")
plt.imshow(cv2.cvtColor(thresh_img4, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
![image](https://github.com/user-attachments/assets/5f83fb78-7b32-4ac3-93cd-9066eadc13ed)

#### Threshold Image (Truncate)
```py

plt.axis("off")
plt.title("Threshold Image (Truncate)")
plt.imshow(cv2.cvtColor(thresh_img5, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
![image](https://github.com/user-attachments/assets/01a17b9a-040b-4574-857c-1d1fdee5e657)

#### Otsu
```py
plt.axis("off")
plt.title("Otsu")
plt.imshow(cv2.cvtColor(thresh_img6, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
![image](https://github.com/user-attachments/assets/ce9c7e64-e282-44f7-9f87-4b0aa954be0d)

#### Adaptive Threshold (Mean)
```py

plt.axis("off")
plt.title("Adaptive Threshold (Mean)")
plt.imshow(cv2.cvtColor(thresh_img7, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
![image](https://github.com/user-attachments/assets/98ab8e7b-630c-4b34-abd9-d481eb151f64)
#### Adaptive Threshold (Gaussian)
```py
plt.axis("off")
plt.title("Adaptive Threshold (Gaussian)")
plt.imshow(cv2.cvtColor(thresh_img8, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
![image](https://github.com/user-attachments/assets/13d50828-7cc3-48b0-b793-28c4a2b51e7d)





## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
