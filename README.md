# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
import the neccesary packages

### Step2:
create the text using cv2.put Text

### Step3:
create the structuting element

### Step4:
Erodde the image

### Step5:
Dilate the image

 
## Program:

``` Python
# NAME: JAYADEV PALLINTI
# REG NO: 212223240058
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
image = np.zeros((500, 500, 3), dtype=np.uint8)

font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'JAYADEV PALLINTI', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)


# Create the structuring element

plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')

# Erode the image

kernel = np.ones((3, 3), np.uint8)
eroded_image = cv2.erode(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')


# Dilate the image
dilated_image = cv2.dilate(image, kernel, iterations=1)

plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')


```
## Output:

### Display the input Image
<img width="389" height="411" alt="image" src="https://github.com/user-attachments/assets/bd54bc5b-8938-4c35-adad-3707378d6b26" />



### Display the Eroded Image
<img width="389" height="411" alt="image" src="https://github.com/user-attachments/assets/90e6d1c9-712f-4495-8f33-3d6d54ddacc2" />


### Display the Dilated Image
<img width="389" height="411" alt="image" src="https://github.com/user-attachments/assets/209aebc7-5e6b-4900-8ede-707214370fdb" />


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
