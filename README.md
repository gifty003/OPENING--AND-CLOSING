# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages


### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation

 
## Program:
```
Developed By : GIFTSON RAJARATHNAM N
Reg no : 212222233002
```
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Step 1: Load the image using cv2.imread()
image = cv2.imread("Fish.jpg")  

# Step 2: Create a structuring element (5x5 rectangular)
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

# Step 3: Use Opening operation (erosion followed by dilation)
opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

# Step 4: Use Closing operation (dilation followed by erosion)
closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

# Convert images from BGR to RGB for Matplotlib
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)

# Plot the original, opening, and closing images using Matplotlib
plt.figure(figsize=(10, 5))

plt.subplot(1, 3, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 3, 2)
plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")

plt.subplot(1, 3, 3)
plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")

plt.tight_layout()
plt.show()

```
## Output:

### Display the input Image
![Screenshot 2024-10-09 160207](https://github.com/user-attachments/assets/6381bd44-a19e-4069-950a-42fd1ebd0876)



### Display the result of Opening
![Screenshot 2024-10-09 160225](https://github.com/user-attachments/assets/2b261458-0b3a-4746-a7ac-b92fef379047)




### Display the result of Closing
![Screenshot 2024-10-09 160235](https://github.com/user-attachments/assets/005e0f9d-2b5d-44fd-b5bc-e5e9b445d0f7)





## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
