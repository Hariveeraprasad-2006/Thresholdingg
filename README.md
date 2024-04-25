# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Install the opencv in the jupiter notebook
### Step2:
Import cv2 and numpy
### Step3:
Read the image by cv2.read(
### Step4:
Doing the global Global Thresholding,Adaptive Thresholding,Otsu's Thresholding 
### Step5:
By using opencv module show the image by running the programm.
## Program
# Load the necessary packages:
```
import cv2
import numpy as np
```



# Read the Image and convert to grayscale
```
image = cv2.imread('username.jpg', 0)
```


# Use Global thresholding to segment the image

```
_, global_thresh = cv2.threshold(image, 127, 255, cv2.THRESH_BINARY)
```


# Use Adaptive thresholding to segment the image


```
adaptive_thresh = cv2.adaptiveThreshold(image, 255, cv2.ADAPTIVE_THRESH_MEAN_C, cv2.THRESH_BINARY, 11, 2)
```

# Use Otsu's method to segment the image 

```
_, otsu_thresh = cv2.threshold(image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
```


# Display the results
```
cv2.imshow('Original Image', image)
cv2.imshow('Global Thresholding', global_thresh)
cv2.imshow('Adaptive Thresholding', adaptive_thresh)
cv2.imshow("Otsu's Thresholding", otsu_thresh)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


## Output

### Original Image
![image](https://github.com/Hariveeraprasad-2006/Thresholdingg/assets/145049988/e7566d9d-4531-45fe-b1c1-7117e09be02f)

### Global Thresholding
![image](https://github.com/Hariveeraprasad-2006/Thresholdingg/assets/145049988/8e56b2f6-4254-4abc-b51a-ca1cc6f19fe4)

### Adaptive Thresholding
![image](https://github.com/Hariveeraprasad-2006/Thresholdingg/assets/145049988/46f315e7-703a-40fc-ad86-06854e95f664)

### Optimum Global Thesholding using Otsu's Method
![image](https://github.com/Hariveeraprasad-2006/Thresholdingg/assets/145049988/aaac2807-f081-4b97-a54a-a6288b422591)


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
