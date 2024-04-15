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

![image](https://github.com/Evangelin-Ruth/IMAGE-TRANSFORMATIONS/assets/94219798/db9fd5e2-8ba1-4e7b-adfe-7fc0aa0aa402)
![image](https://github.com/Evangelin-Ruth/IMAGE-TRANSFORMATIONS/assets/94219798/b95baf73-9167-4888-b78d-35d57f4d018c)


### ii) Image Scaling

![image](https://github.com/Evangelin-Ruth/IMAGE-TRANSFORMATIONS/assets/94219798/5d7f37f0-9c56-464b-a79e-2867d73b5bea)
![image](https://github.com/Evangelin-Ruth/IMAGE-TRANSFORMATIONS/assets/94219798/284a204c-3673-4b0d-a05d-12cfa69cdf89)

### iii)Image shearing

![image](https://github.com/Evangelin-Ruth/IMAGE-TRANSFORMATIONS/assets/94219798/18253b66-70b2-4dd3-bb60-9f291ffedfb6)
![image](https://github.com/Evangelin-Ruth/IMAGE-TRANSFORMATIONS/assets/94219798/44e0028f-b0ff-41fd-9c41-337cdc45d492)
![image](https://github.com/Evangelin-Ruth/IMAGE-TRANSFORMATIONS/assets/94219798/9b65ba73-185a-49ec-b65a-8732f394f67f)

### iv)Image Reflection

![image](https://github.com/Evangelin-Ruth/IMAGE-TRANSFORMATIONS/assets/94219798/7805316c-c573-47b7-a1a9-ee9f8d379516)
![image](https://github.com/Evangelin-Ruth/IMAGE-TRANSFORMATIONS/assets/94219798/7e297ab3-53f1-420c-9b6c-5ddf924db5be)
![image](https://github.com/Evangelin-Ruth/IMAGE-TRANSFORMATIONS/assets/94219798/cbad7818-406a-4fca-a56d-401391d25c1f)


### v)Image Rotation

![image](https://github.com/Evangelin-Ruth/IMAGE-TRANSFORMATIONS/assets/94219798/51634186-024d-47bf-8c6e-a80ade211b7c)
![image](https://github.com/Evangelin-Ruth/IMAGE-TRANSFORMATIONS/assets/94219798/41ca041d-553b-438b-92c2-c241ce4967a5)


### vi)Image Cropping

![image](https://github.com/Evangelin-Ruth/IMAGE-TRANSFORMATIONS/assets/94219798/66394469-d940-4618-95b7-9b3e83e27474)
![image](https://github.com/Evangelin-Ruth/IMAGE-TRANSFORMATIONS/assets/94219798/7d040b7e-296e-4e1e-88ce-d2dec78859c7)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
