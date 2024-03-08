# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>

### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>

## Program:
```python
Developed By : K MADHAVA REDDY
Register Number : 212223240064
```
### Original image 
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("chintu.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(image)
plt.show()
```
###i)Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("chintu.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M = np.float32([[1,0,114],[0,1,-230],[0,0,1]])
translated_image = cv2.warpPerspective(image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```
###ii) Image Scaling



###iii)Image shearing



###iv)Image Reflection




###v)Image Rotation




###vi)Image Cropping





## Output:
### Original image
![image](https://github.com/Madhavareddy09/IMAGE-TRANSFORMATIONS/assets/145742470/639fe554-891c-46f1-83f6-8fba22aff206)

### i)Image Translation

![image](https://github.com/Madhavareddy09/IMAGE-TRANSFORMATIONS/assets/145742470/181fc291-47eb-4365-9673-64fa97a988ee)

### ii) Image Scaling
<br>
<br>
<br>
<br>


### iii)Image shearing
<br>
<br>
<br>
<br>


### iv)Image Reflection
<br>
<br>
<br>
<br>



### v)Image Rotation
<br>
<br>
<br>
<br>



### vi)Image Cropping
<br>
<br>
<br>
<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
