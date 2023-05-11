# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1:
Import the necessary packages.
### Step 2:
Create the Text using cv2.putText.
### Step 3:
Create the structuring element.
### Step 4:
Implement Opening Operation.
### Step 5:
Implement Closing Operation.

 
## Program:

``` Python
# Name:sangeetha.K
# reg.no:212221230085
# Import the necessary packages
import numpy as np
import matplotlib.pyplot as plt
import cv2

# Create the Text using cv2.putText
text_image = np.zeros((100,500),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image," Sangeetha",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image)
plt.axis('off')

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
opening_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(opening_image)
plt.axis('off')

# Use Closing Operation
closing_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(closing_image)
plt.axis('off')

```
## Output:

### Display the input Image
![image](https://github.com/sangeethak15-AI/Opening-and-Closing/assets/93992063/7229cbe0-c94d-4ce8-a5f6-c927d751bca2)


### Display the result of Opening
![image](https://github.com/sangeethak15-AI/Opening-and-Closing/assets/93992063/438b7f05-66ab-4a69-a0b4-943cf51e99cb)


### Display the result of Closing
![image](https://github.com/sangeethak15-AI/Opening-and-Closing/assets/93992063/11b3ccaa-2ce8-4c8c-a997-0365e791324b)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
