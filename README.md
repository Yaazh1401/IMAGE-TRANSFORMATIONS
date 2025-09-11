# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step 1:
Import necessary libraries such as OpenCV, NumPy, and Matplotlib for image processing and visualization.

## Step 2:
Read the input image using cv2.imread() and store it in a variable for further processing

## Step 3:
Apply various transformations like translation, scaling, shearing, reflection, rotation, and cropping by defining corresponding functions:

1.Translation moves the image along the x or y-axis.

2.Scaling resizes the image by scaling factors.

3.Shearing distorts the image along one axis.

4.Reflection flips the image horizontally or vertically.

5.Rotation rotates the image by a given angle.

## Step 4:
Display the transformed images using Matplotlib for visualization. Convert the BGR image to RGB format to ensure proper color representation.

## Program:
```python
Developed By:
Register Number:
original Image
import cv2
import numpy as np
import matplotlib.pyplot as plt
image=cv2.imread("C:\\Users\\admin\\OneDrive\\Desktop\\DIPT\\bird.jpeg")
image.shape
#Display the images.
plt.imshow(image[:,:,::-1])
plt.title("Original Image")
plt.show()

i)Image Translation
tx,ty=100,200
M_translation=np.float32([[1,0,tx],[0,1,ty]])
translated_image=cv2.warpAffine(image,M_translation, (673,419))
plt.imshow(translated_image[:,:,::-1])
plt.title("Translated Image")
plt.axis("on")
plt.show()

ii) Image Scaling
fx, fy = 5.0, 2.0  
scaled_image = cv2.resize(image, None, fx=fx, fy=fy, interpolation=cv2.INTER_LINEAR)

plt.imshow(cv2.cvtColor(scaled_image, cv2.COLOR_BGR2RGB))  
plt.title("Scaled Image")  # Set title
plt.axis('off')


iii)Image shearing
shear_matrix = np.float32([[1, 0.5, 0], [0.5, 1, 0]])
sheared_image = cv2.warpAffine(image, shear_matrix, (image.shape[1], image.shape[0]))

plt.imshow(cv2.cvtColor(sheared_image, cv2.COLOR_BGR2RGB))  
plt.title("Sheared Image")  
plt.axis('off')


iv)Image Reflection

reflected_image = cv2.flip(image, 2)

plt.imshow(cv2.cvtColor(reflected_image, cv2.COLOR_BGR2RGB))  
plt.title("Reflected Image")  
plt.axis('off')


v)Image Rotation
(height, width) = image.shape[:2] 
angle = 45 
center = (width // 2, height // 2)  
M_rotation = cv2.getRotationMatrix2D(center, angle, 1)
rotated_image = cv2.warpAffine(image, M_rotation, (width, height))

plt.imshow(cv2.cvtColor(rotated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Rotated Image")  
plt.axis('off')(height, width) == image.shape[:2] 
angle = 45 
center = (width // 2, height // 2)  
M_rotation = cv2.getRotationMatrix2D(center, angle, 1)
rotated_image = cv2.warpAffine(image, M_rotation, (width, height))

plt.imshow(cv2.cvtColor(rotated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Rotated Image")  
plt.axis('off')



vi)Image Cropping
x, y, w, h = 400, 400, 600, 450 
cropped_image = image[y:y+h, x:x+w]

plt.imshow(cv2.cvtColor(cropped_image, cv2.COLOR_BGR2RGB)) 
plt.title("Cropped Image")  
plt.axis('off')





```
## Output:
### Original image 

<br><img width="799" height="566" alt="image" src="https://github.com/user-attachments/assets/5b668711-4ab3-49ac-83c6-16da6e574d80" />

<br>
### i)Image Translation

<br><img width="803" height="492" alt="image" src="https://github.com/user-attachments/assets/5baed32d-f3d5-4a1d-87eb-c8a8d822126a" />

<br>
<br>
<br>

### ii) Image Scaling
<br>

<br><img width="779" height="332" alt="image" src="https://github.com/user-attachments/assets/b8108563-aa48-42e1-bc0f-0f61c62eeb52" />

<br>
<br>


### iii)Image shearing
<br>

<br><img width="798" height="568" alt="image" src="https://github.com/user-attachments/assets/7a259ac9-1edd-42dc-81b0-65491fcc72be" />

<br>
<br>


### iv)Image Reflection
<br>

<br><img width="737" height="571" alt="image" src="https://github.com/user-attachments/assets/40856cd1-d3bd-4d3e-86ba-712f2c065986" />

<br>
<br>



### v)Image Rotation
<br>

<br><img width="838" height="533" alt="image" src="https://github.com/user-attachments/assets/a8fb97b7-2d0a-4903-8b35-6700fccde391" />

<br>
<br>



### vi)Image Cropping
<br>

<br><img width="842" height="565" alt="image" src="https://github.com/user-attachments/assets/6afbd28d-4c03-414e-b282-0657aa3d2343" />

<br>
<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
