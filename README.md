# OPENING AND CLOSING

## AIM:
To implement Opening and Closing using Python and OpenCV.

## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV
## ALGORITHM:
### Step 1:
Import the necessary packages.
### Step 2:
Create the Text using cv2.putText
### Step 3:
Create the structuring element.
### Step 4:
Use Opening operation.
### Step 5:
Use Closing Operation.

<br><br><br><br><br>

## PROGRAM:
```
/*
Developed by   : J . RITHANIEPRIYANKA
Register Number: 212220230039
*/
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'Rithu',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img)
plt.show()

# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation
image_open=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.axis('off')
plt.imshow(image_open)
plt.show()

# Use Closing Operation
image_close=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.axis('off')
plt.imshow(image_close)
plt.show()

```
## OUTPUT:

### Display the input Image

![EXP11-A](https://user-images.githubusercontent.com/75235132/171092516-d9a3a6a0-19ce-40b1-b25d-d56b3ef52093.png)

### Display the result of Opening
![EXP11=B](https://user-images.githubusercontent.com/75235132/171092525-6a5b81a2-dc00-4836-9f4d-193357324234.png)

### Display the result of Closing

![EXP11-C](https://user-images.githubusercontent.com/75235132/171092533-337371a6-2859-427c-bac1-54e96820cc12.png)

## RESULT:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
