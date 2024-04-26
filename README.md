# Implementation-of-Erosion-and-Dilation
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
Developed by : ARVIND S
Register Number : 21222240012
```
# Import the necessary packages
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```python
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'Django',(80,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
# Create the structuring element
```python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
# Erode the image
```python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```
# Dilate the image
```python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

### Display the input Image
![image](https://github.com/S-ARVIND01/erosion--dilation/assets/118707337/93c99917-db40-4e25-a398-57d276106a5a)

### Display the Eroded Image
![image](https://github.com/S-ARVIND01/erosion--dilation/assets/118707337/39bbb978-7289-4e4e-bb35-54d95606b32f)

### Display the Dilated Image
![image](https://github.com/S-ARVIND01/erosion--dilation/assets/118707337/ab5feb89-be98-492a-a279-eec982cd612b)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
