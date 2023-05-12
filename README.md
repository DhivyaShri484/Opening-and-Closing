# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the required packages.

### Step2:
Create the input image.

### Step3:
Create the structuring element.

### Step4:
Apply opening operation.

### Step5:
Apply closing operation.

 
## Program:

``` Python
# Import necessary packages

import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
im=cv2.putText(img1,' DHIVYA ',(5,70),font,2,(255),5,cv2.LINE_AA)
cv2.imshow("Input Image",im)

# Create the structuring element

Kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation

image1=cv2.morphologyEx(im,cv2.MORPH_OPEN,Kernel)
cv2.imshow("Opening Image",image1)

# Use Closing Operation

image1=cv2.morphologyEx(im,cv2.MORPH_CLOSE,Kernel)
cv2.imshow("Closing Image",image1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:

### Display the input Image

![input](https://github.com/DhivyaShri484/Opening-and-Closing/assets/94505585/5199eed8-8406-4fcc-bc85-8b6af6d130da)

### Display the result of Opening

![opening](https://github.com/DhivyaShri484/Opening-and-Closing/assets/94505585/822dc82a-312b-4cff-b8da-9e50b4703ffe)

### Display the result of Closing

![closing](https://github.com/DhivyaShri484/Opening-and-Closing/assets/94505585/905f86ec-a0da-41a8-b539-4eeefdc1b266)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
