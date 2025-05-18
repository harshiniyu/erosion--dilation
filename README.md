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
## Harshini Y
## reg no:212223240050
``` 
# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline

# Create the Text using cv2.putText
def load_img():
    blank_img =np.zeros((600,600))
    font = cv2.FONT_HERSHEY_SIMPLEX
    cv2.putText(blank_img,text='HARSH',org=(50,300), fontFace=font,fontScale= 5,color=(255,255,255),thickness=25,lineType=cv2.LINE_AA)
    return blank_img


# Create the structuring element

def display_img(img):
    fig = plt.figure(figsize=(12,10))
    ax = fig.add_subplot(111)
    ax.imshow(img,cmap='gray')
    plt.show()
img = load_img()
display_img(img)
kernel = np.ones((5, 5), dtype=np.uint8)
kernel

# Erode the image

erosion1 = cv2.erode(img,kernel)
display_img(erosion1)



# Dilate the image


dilation = cv2.dilate(img,kernel)
display_img(dilation)


```
## Output:

### Display the input Image
![image](https://github.com/user-attachments/assets/aaf45a45-b7e1-4e0f-8d48-d3460b64e6cd)


### Display the Eroded Image
![image](https://github.com/user-attachments/assets/db33f43e-215d-4ccf-a3f3-92ddd6b127f7)


### Display the Dilated Image
![image](https://github.com/user-attachments/assets/c8d56207-969e-4195-8b62-3f410a4117fd)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
