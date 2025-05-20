# OPENING--AND-CLOSING

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
   
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation
 
## Program:
``` Python
# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

img1=np.zeros((300,600),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"Dakshata",(5,100),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element

kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation

img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Use Closing Operation

img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:

### Display the input Image

![Screenshot 2025-05-20 103349](https://github.com/user-attachments/assets/d7221f65-c499-4eb6-9cc8-dcc1ee7d2957)

### Display the result of Opening

![Screenshot 2025-05-20 103454](https://github.com/user-attachments/assets/70a09454-c018-4e95-add8-628e86fd9731)

### Display the result of Closing

![Screenshot 2025-05-20 103532](https://github.com/user-attachments/assets/732051ee-0fb8-4509-aae2-529a6eb3789a)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
