# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Use Opening operation.

### Step5:
Use Closing Operation. 
## Program:
```
DEVELOPED BY: ROGITH GANESH.R
REGISTER NO: 212223100046
```
# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'ROGITH', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```
# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```
# Use Opening operation
```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")
```
# Use Closing Operation
```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")
```
## Output:
![Screenshot 2025-05-17 060010](https://github.com/user-attachments/assets/6ec640b4-7d8f-4d01-88eb-6ea28be66996)


### Display the input Image
![Screenshot 2025-05-17 060028](https://github.com/user-attachments/assets/694677ca-12c0-45e9-a69b-cbd34436c92d)


### Display the result of Opening

![Screenshot 2025-05-17 060039](https://github.com/user-attachments/assets/476917cc-ff5d-4cb6-8361-e6982ef59bc6)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
