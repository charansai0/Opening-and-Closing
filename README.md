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
Use Opening operation.

### Step 5:
Use Closing Operation.

### Step 6:
Print the output and end the program.

PROGRAM:
~~~
/*
Developed by   : V.CHARAN SAI
Register Number: 212220240061
*/
~~~
~~~
# Import the necessary packages

# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'jithu',(5,70),font,2,(255),5,cv2.LINE_AA)
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
~~~
## Output:

### Display the input Image
![11](https://user-images.githubusercontent.com/94296221/172039811-142fffdb-f382-45e8-bb44-175b82b91329.png)


### Display the result of Opening
![22](https://user-images.githubusercontent.com/94296221/172039813-68345889-6b9e-40df-9f4f-f4e61221b740.png)


### Display the result of Closing
![3](https://user-images.githubusercontent.com/94296221/172039814-a390c7cd-0eaf-4b3d-91cf-3e6a017b2b2a.png)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
