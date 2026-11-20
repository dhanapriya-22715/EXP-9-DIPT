# Exp-9- Record-IMPLEMENTATION OF EROSION AND DILATION
## Name : Dhanappriya S
## REG NO :212224230056

## AIM

To implement Erosion and Dilation operations on an image using OpenCV to observe the shrinking and expanding effects on text.

## PROCEDURE

1.Start the program and import the required libraries (cv2, numpy, and matplotlib.pyplot).
2.Create a blank image using np.zeros().
3.Add text to the image using cv2.putText().
4.Display the input image containing the text using matplotlib.pyplot.
5.Create a 3×3 kernel using np.ones().
6.Apply Erosion using cv2.erode() to shrink the text and Dilation using cv2.dilate() to expand the text.
7.Display the Eroded and Dilated images using matplotlib.pyplot and stop the program.

## CODE
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'RAGASUDHA R', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)
# Apply erosion (shrinking effect)
eroded_image = cv2.erode(image, kernel, iterations=1)
# Display the eroded image
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')
# Apply dilation (expanding effect)
dilated_image = cv2.dilate(image, kernel, iterations=1)
# Display the dilated image
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')

```
## OUTPUT
<img width="1017" height="843" alt="image" src="https://github.com/user-attachments/assets/40ed3e64-d722-44b5-b9fc-500230c6e448" />
<img width="567" height="443" alt="image" src="https://github.com/user-attachments/assets/24114e55-f7d8-4fdc-9edc-c42abfdcba3a" />
<img width="653" height="441" alt="image" src="https://github.com/user-attachments/assets/a5937354-e1dc-4486-8e31-60c8045f5969" />
<img width="670" height="447" alt="image" src="https://github.com/user-attachments/assets/57975bbd-102d-4c7c-97c6-b02e981c76c9" />

## RESULT
Erosion and Dilation operations are successfully implemented using OpenCV. The eroded image shows thinner text, while the dilated image shows thicker text compared to the original image.
