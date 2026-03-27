# OPENING--AND-CLOSING

## Name: Darshan V
## Register Number: 212224230050

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
## Step1:
Import the necessary packages

## Step2:
Create the Text using cv2.putText

## Step3:
Create the structuring element

## Step4:
Use Opening operation

## Step5:
Use Closing Operation

 
## Program Developed By:

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = np.zeros((500, 500, 3), dtype=np.uint8)

font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'JEEVITH', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

kernel = np.ones((3, 3), np.uint8)

opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

original_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
opened_rgb = cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB)
closed_rgb = cv2.cvtColor(closed_image, cv2.COLOR_BGR2RGB)

plt.figure(figsize=(12,5))

plt.subplot(1,3,1)
plt.imshow(original_rgb)
plt.title("Input Image with Text")
plt.axis('off')

plt.subplot(1,3,2)
plt.imshow(opened_rgb)
plt.title("Opening Operation")
plt.axis('off')

plt.subplot(1,3,3)
plt.imshow(closed_rgb)
plt.title("Closing Operation")
plt.axis('off')

plt.show()

```


## Output:
<img width="389" height="411" alt="download" src="https://github.com/user-attachments/assets/ac9a89b6-162b-4370-8489-6a16f2dfb3e1" />
<img width="389" height="411" alt="download" src="https://github.com/user-attachments/assets/b39e78e6-c95c-48d5-a1a6-3aaeffcaeb6a" />

<img width="389" height="411" alt="download" src="https://github.com/user-attachments/assets/cbb88ea7-4dd7-4737-b071-bea9ffae84bd" />





## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
