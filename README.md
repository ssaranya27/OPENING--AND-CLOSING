
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
### DEVELOPED BY: SARANYA S
### REGISTER NO: 212223220101

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
cv2.putText(img, 'SARANYA S', (5,70), font, 2, (255), 5, cv2.LINE_AA)
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

### Display the input Image

<img width="697" height="189" alt="image" src="https://github.com/user-attachments/assets/2b36dbef-4c32-4799-ab32-12797f4fe307" />


### Display the result of Opening
<img width="679" height="183" alt="image" src="https://github.com/user-attachments/assets/7469917c-92e7-4b9c-b479-112896cbadde" />



### Display the result of Closing
<img width="673" height="179" alt="image" src="https://github.com/user-attachments/assets/85ceefaf-3f7b-4314-90ed-99d0959fdefc" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
