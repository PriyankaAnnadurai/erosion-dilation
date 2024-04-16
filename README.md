# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
- Step1: Import the necessary packages
- Step2: Insert the text using cv2.putText()
- Step3: The perform the erosion for given text and display the text using imshow()
- Step4: Next,perform dilation for inout text and display the result
## Program:
```
DEVELOPED BY: PRIYANKA.A
REGISTER NUMBER: 212222230113
```
### Import the necessary packages
```python
import cv2
import numpy as np 
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```python
img1=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Priyanka',(5,70),font,2,(255),5,cv2.LINE_AA)
```
### Create the structuring element
```python
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
### Erode the image
```python
image_erode1=cv2.erode(img1,kernel1)
plt.imshow(image_erode1)
plt.axis("off")
```
### Dilate the image
```python
image_dilate1=cv2.dilate(img1,kernel1)
plt.imshow(image_dilate1)
plt.axis("off")
```
## Output:
### Display the input Image
![image](https://github.com/PriyankaAnnadurai/erosion-dilation/assets/118351569/61c22796-9d84-40f5-a8b6-45090bdbf159)

### Display the Eroded Image
![image](https://github.com/PriyankaAnnadurai/erosion-dilation/assets/118351569/a1f1014f-942e-4c78-a098-307c2f5c3d03)

### Display the Dilated Image
![image](https://github.com/PriyankaAnnadurai/erosion-dilation/assets/118351569/f95f7741-81a5-428e-9804-f31a8058f473)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
