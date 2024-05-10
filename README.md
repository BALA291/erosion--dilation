# EX-09 Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages


### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image

 
## Program:

``` Python
DEVELOPED BY : BALAMURUGAN B
REGISTER NUMBER: 212222230016
# Import the necessary packages

import numpy as np
import cv2
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
img = np.zeros((100,600),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'BALAMURUGAN',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')


# Create the structuring element

kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)


# Erode the image
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')




# Dilate the image

img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')






```
## Output:

### Display the input Image
![BALA](https://github.com/BALA291/erosion--dilation/assets/120717501/1fb1eb65-2250-43e9-86ae-1c151e853642)

### Display the Eroded Image
![BALA E](https://github.com/BALA291/erosion--dilation/assets/120717501/41fa0355-5ca0-4190-b735-4f00c1fcd278)

### Display the Dilated Image
![BALA D](https://github.com/BALA291/erosion--dilation/assets/120717501/e5af666d-2ea4-40e2-9ba0-a374197b7822)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
