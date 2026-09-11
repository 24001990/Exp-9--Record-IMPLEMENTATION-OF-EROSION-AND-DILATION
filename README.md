# EXP-9-Implementation-of-Erosion-and-Dilation
# Developed by: DODLA SUSMITHA
# Reg NO: 212224110016
# Aim
To implement Erosion and Dilation using Python and OpenCV.

# Software Required
Anaconda - Python 3.7
OpenCV
# Algorithm:
# Step1:
Import required libraries (OpenCV, NumPy) and load the image in grayscale

# Step2:
Define a structuring element (kernel) for morphological operations.

# Step3:
Apply erosion using cv2.erode() on the image with the defined kernel.

# Step4:
Apply dilation using cv2.dilate() on the image with the same kernel.

# Step5:
Display and compare the original, eroded, and dilated images.

# Program:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
```
image = np.zeros((500, 500, 3), dtype=np.uint8)
```
```
font = cv2.FONT_HERSHEY_SIMPLEX
text = "DODLA SUSMITHA"
cv2.putText(image, text, (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
```
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Input Image with Text")
plt.axis("off")
plt.show()
```
```
kernel = np.ones((3, 3), np.uint8)
eroded_image = cv2.erode(image, kernel, iterations=1)
```
```
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))
plt.title("Eroded Image")
plt.axis('off')
```
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
```
```
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Dilated Image")
plt.axis('off')
```
# Output:
# Display the input Image
<img width="437" height="466" alt="Screenshot 2026-09-11 230109" src="https://github.com/user-attachments/assets/1584bb29-1cb4-4701-8bd7-3f958fdaf7f5" />

# Display the Eroded Image
<img width="597" height="497" alt="Screenshot 2026-09-11 230123" src="https://github.com/user-attachments/assets/6d4fa3c8-62b2-48d8-ae64-d7020a69a867" />

# Display the Dilated Image
<img width="610" height="490" alt="Screenshot 2026-09-11 230134" src="https://github.com/user-attachments/assets/9638e7d5-6758-4224-86eb-bcf5518f751d" />

# Result
Thus the generated text image is eroded and dilated using python and OpenCV.
