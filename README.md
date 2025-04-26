# Edge-Linking-using-Hough-Transformm
## Aim:
To write a Python program to detect the lines using Hough Transform.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import all the necessary modules for the program.
### Step2:

Load a image using imread() from cv2 module.
### Step3:

Convert the image to grayscale.
### Step4:

Using Canny operator from cv2,detect the edges of the image.
### Step5:

Using the HoughLinesP(),detect line co-ordinates for every points in the images.Using For loop,draw the lines on the found co-ordinates.Display the image.

## PROGRAM:

## DEVELOPED BY: SANTHIYA R
## REG NO : 212223230192

```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('Qn_7_.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
edges = cv2.Canny(gray_image, 50, 150, apertureSize=3)
output_image = image.copy()
if lines is not None:
    for line in lines:
        x1, y1, x2, y2 = line[0]
        cv2.line(output_image, (x1, y1), (x2, y2), (0, 255, 0), 2)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Input Image')
plt.axis('off')
plt.show()
plt.imshow(gray_image, cmap='gray')
plt.title('Grayscale Image')
plt.axis('off')
plt.show()
plt.imshow(edges, cmap='gray')
plt.title('Canny Edge Detector Output')
plt.axis('off')
plt.show()
plt.imshow(cv2.cvtColor(output_image, cv2.COLOR_BGR2RGB))
plt.title('Hough Transform - Line Detection')
plt.axis('off')
plt.show()
```
## Output

### Input image and grayscale image
![image](https://github.com/user-attachments/assets/ca587491-edcb-4b95-9bc7-49aec18bdabf)
![image](https://github.com/user-attachments/assets/50fa30e1-a281-4fca-bc4c-7eed65a236c1)


### Canny Edge detector output
![image](https://github.com/user-attachments/assets/5b018b89-24d8-4b0a-923e-b5821d7ad8bd)


### Display the result of Hough transform
![image](https://github.com/user-attachments/assets/df4c4c4b-3b3a-45fd-a8f9-6495b889e0e4)

## Result:
Hence, a python program to detect the lines using Hough Transform is implemented and executed.

