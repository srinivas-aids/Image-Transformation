# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

### Step1:

Import the necessary libraries and read the original image and save it as a image variable.
<br>

### Step2:

Translate the image.
<br>

### Step3:

Scale the image.
<br>

### Step4:

Shear the image.
<br>

### Step5:

Reflect of image.
<br>

### Step6:

Rotate the image.
<br>

## Program:
```python
Developed By: SRINIVAS.U
Register Number: 212221230108

i) Image Translation

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("OIP.png") 
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M= np.float32([[1, 0, 80],
                [0, 1, 80],
                 [0, 0, 1]])
translated_image =cv2.warpPerspective (input_image, M, (cols, rows))
plt.imshow(translated_image)
plt.show()


ii) Image Scaling

rows, cols, dim = input_image.shape
M = np. float32 ([[1.5, 0 ,0],
                 [0, 1.8, 0],
                  [0, 0, 1]])
scaled_img=cv2.warpPerspective(input_image, M, (cols*2, rows*2))
plt.imshow(scaled_img)
plt.show()


iii) Image shearing

rows, cols, dim = input_image.shape
M_x = np.float32([[1, 0.5, 0],
                  [0, 1 ,0],
                  [0, 0, 1]])

M_y = np.float32([[1, 0, 0],
                  [0.5, 1, 0],
                  [0, 0, 1]])
sheared_img_xaxis = cv2.warpPerspective (input_image, M_x, (int(cols *1.5), int (rows *1.5))) 
sheared_img_yaxis = cv2.warpPerspective (input_image, M_y, (int (cols *1.5), int (rows *1.5)))
plt.imshow(sheared_img_xaxis)
plt.show()
plt.imshow(sheared_img_yaxis)
plt.show()
iv) Image Reflection

M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_image,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_image,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()


v) Image Rotation

angle=np.radians(80)
M=np.float32([[np.sin(angle),-(np.cos(angle)),0],
               [np.cos(angle),np.sin(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()


vi) Image Cropping

cropped_img=input_image[200:250,400:650]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()


```
## Output:
### Image:

<img width="317" alt="image" src="https://user-images.githubusercontent.com/93427183/231696443-a91c0b23-b456-44c6-8fd6-f49a1ea2a273.png">

### i)Image Translation

<img width="437" alt="image" src="https://user-images.githubusercontent.com/93427183/231696784-9f05fd32-83eb-490d-b350-6c78b9f85f37.png">


### ii) Image Scaling

<img width="418" alt="image" src="https://user-images.githubusercontent.com/93427183/231696997-d54dcf7d-2f99-4f87-b11a-93a358fbeae3.png">


### iii)Image shearing

<img width="409" alt="image" src="https://user-images.githubusercontent.com/93427183/231697098-c2274781-4a0b-4006-b478-eb7dc2d22cbb.png">



### iv)Image Reflection

<img width="421" alt="image" src="https://user-images.githubusercontent.com/93427183/231697191-e99b6c98-8514-4aa5-8c15-da086c7ebc78.png">


### v)Image Rotation

<img width="402" alt="image" src="https://user-images.githubusercontent.com/93427183/231697539-681412fa-0e7c-45a8-9598-f7e68af7d86e.png">


### vi)Image Cropping

<img width="395" alt="image" src="https://user-images.githubusercontent.com/93427183/231697692-cf6eec9a-ca86-41f0-a49e-27c21cd7ca59.png">


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
