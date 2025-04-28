# Implementation-of-Erosion-and-Dilation

## Aim:

To implement Erosion and Dilation using Python and OpenCV.

## Software Required:

1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:

Step1: Import the necessary pacakages

Step2: Create the structuring element

Step3: Create a 5x5 rectangular kernel using cv2.getStructuringElement() for morphological operations.

Step4: Perform erosion and dilation on the image using cv2.erode() and cv2.dilate() with the defined kernel.

Step5: Use matplotlib to display the original, eroded, and dilated images side-by-side for comparison.

 
## Program:
### Name : Dharshni V M
### Register Number : 212223240029
``` 

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("bean.png")
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
eroded_image = cv2.erode(image, kernel, iterations=1)
dilated_image = cv2.dilate(image, kernel, iterations=1)
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
eroded_image_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
dilated_image_rgb = cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)
plt.figure(figsize=(8, 8))
plt.subplot(1, 3, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
plt.tight_layout()
plt.show()
plt.figure(figsize=(8, 8))
plt.subplot(1, 3, 2)
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")
plt.tight_layout()
plt.show()
plt.figure(figsize=(8, 8))
plt.subplot(1, 3, 3)
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")
plt.tight_layout()
plt.show()

```
## Output:

### Display the input Image

![original](https://github.com/user-attachments/assets/c640014d-ce67-439f-bcd8-a386d6c56175)

### Display the Eroded Image

![eroded](https://github.com/user-attachments/assets/cd46913f-0d0e-4a0b-9609-7bc19b0fdee5)

### Display the Dilated Image

![dilated](https://github.com/user-attachments/assets/73076454-aec4-4f16-acea-d9379dc3ec30)

## Result
Thus the generated image is eroded and dilated using python and OpenCV.
