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


<img width="950" height="315" alt="download" src="https://github.com/user-attachments/assets/89c9724a-4d55-4d40-bf16-d1a58c0b9564" />



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
