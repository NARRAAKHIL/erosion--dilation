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
## Developed by: NARRA AKHIL
## Register number: 212223230136
## PROGRAM
```
#exp-9-Erosion & Dilation
import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the text using cv2.putText
cv2.putText(img1,'AKHIL' ,(5,70),font,4,(255),2,cv2.LINE_AA)


# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
img_erode=cv2.erode(img1,kernel1)

# Display the results
plt.figure(figsize=(12, 5))
plt.subplot(1,3,1)
plt.imshow(img1,cmap='gray')
plt.subplot(1,3,2)
plt.imshow(img_dilate,cmap='gray')
plt.subplot(1,3,3)
plt.imshow(img_erode,cmap='gray')
```
## Output:

### Display the input Image
![Screenshot 2025-05-04 142408](https://github.com/user-attachments/assets/a337d0e8-e258-46fc-859b-48782867f568)

### Display the Eroded Image
![Screenshot 2025-05-04 142413](https://github.com/user-attachments/assets/e0df3e07-b213-42e8-a2a9-ba9bcb1ca3f9)


### Display the Dilated Image
![Screenshot 2025-05-04 142419](https://github.com/user-attachments/assets/99e94e7b-b6c3-4193-a124-26ca23910330)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
