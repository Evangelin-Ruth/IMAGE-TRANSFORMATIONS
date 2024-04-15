# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import the required libraries and image for transformation.

### Step2:

Perform operations on the image like translaton, rotation and other.

### Step3:

Use the warpPerspective(image , matrix, (rows, columns)) function.

### Step4:

Plot the Image and Transformed Image on the graph using matplotlib for identifying changes.

### Step5:

Diifferent operations has been performed on the image.

## Program:
```python
Developed By: EVANGELIN S
Register Number: 212221230025

i)Image Translation

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread ("bookcover.jpg")
input_image = cv2. cvtColor (input_image, cv2. COLOR_BGR2RGB)
plt. axis('off')
plt.imshow(input_image)
plt. show()
rows, cols, dim = input_image.shape
M = np. float32([[1, 0, 300],[0, 1, 300],[0, 0, 1]])
translated_image = cv2.warpPerspective (input_image, M, (cols, rows))
plt.axis("off")
plt.imshow(translated_image)
plt.show()


ii) Image Scaling

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("bookcover.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
M=np.float32([[1.5,0,0],
             [0,2,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()

iii)Image shearing

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("bookcover.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1,0,0],
               [0.4,1,0],
               [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()


iv)Image Reflection

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("bookcover.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()


v)Image Rotation

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("bookcover.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()

vi)Image Cropping

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("bookcover.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
cropped_img=input_img[20:150,60:230]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()

```
## Output:
### i)Image Translation:
![image](https://github.com/Evangelin-Ruth/IMAGE-TRANSFORMATIONS/assets/94219798/c596d462-1b46-49a8-99dc-a0d610289f3e)





### ii) Image Scaling

![image](https://github.com/Evangelin-Ruth/IMAGE-TRANSFORMATIONS/assets/94219798/1a4da4fd-d7b1-492f-9656-cb12d281e924)


### iii)Image shearing

![image](https://github.com/Evangelin-Ruth/IMAGE-TRANSFORMATIONS/assets/94219798/a78c2a14-7b60-4e8b-9fb3-c28e5d214954)


### iv)Image Reflection
![image](https://github.com/Evangelin-Ruth/IMAGE-TRANSFORMATIONS/assets/94219798/6d3ce170-8e30-4ef2-92da-7f8429eb734c)



### v)Image Rotation

![image](https://github.com/Evangelin-Ruth/IMAGE-TRANSFORMATIONS/assets/94219798/e2c0c425-32e4-4010-9348-e40f067ee906)


### vi)Image Cropping
![image](https://github.com/Evangelin-Ruth/IMAGE-TRANSFORMATIONS/assets/94219798/3713d1e3-da4b-47a6-8ac9-f48922681caf)





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
