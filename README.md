# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

### Step1:

Import all the necessary modules

### Step2:

Choose an image and save it as filename.jpg
### Step3:


Use imread to read the image
### Step4:
Use cv2.warpPerspective(image,M,(cols,rows)) to translation the image
### Step5:
Use cv2.warpPerspective(image,M,(cols*2,rows*2)) to scale the image
### Step6:
Use cv2.warpPerspective(image,M,(int(cols*1.5),int(rows*1.5))) for x and y axis to shear the image
### Step7:
Use cv2.warpPerspective(image,M,(int(cols),int(rows))) for x and y axis to reflect the image
### Step8:
Use cv2.warpPerspective(image,M,(int(cols),int(rows))) to rotate the image
### Step9:
Crop the image to remove unwanted areas from an image
### Step10:

Use cv2.imshow to show the image
### Step11:
<br>
End the program

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
### i)Image Translation
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
### ii) Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("chintu.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M = np.float32([[2.4,0 ,0],[0,1.9,0],[0,0,1]])
scaled_image = cv2.warpPerspective(image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_image)
plt.show()
```


### iii)Image shearing
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("chintu.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M_x= np.float32([[1,0.8 ,0],[0,1,0],[0,0,1]])
M_y = np.float32([[1,0,0],[0.6,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(image,M_x,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(image,M_y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.imshow(sheared_img_yaxis)
plt.show()
```


### iv)Image Reflection
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("chintu.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M_x= np.float32([[1,0 ,0],[0,-1,rows],[0,0,1]])
M_y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(image,M_x,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(image,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.imshow(reflected_img_yaxis)
plt.show()
```


### v)Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("chintu.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
angle = np.radians(10)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```



### vi)Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("chintu.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
cropped_img = image[100:800,20:400]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
```




## Output:
### Original image
![image](https://github.com/Madhavareddy09/IMAGE-TRANSFORMATIONS/assets/145742470/639fe554-891c-46f1-83f6-8fba22aff206)

### i)Image Translation

![image](https://github.com/Madhavareddy09/IMAGE-TRANSFORMATIONS/assets/145742470/181fc291-47eb-4365-9673-64fa97a988ee)

### ii) Image Scaling
![image](https://github.com/Madhavareddy09/IMAGE-TRANSFORMATIONS/assets/145742470/29f0576e-7036-4c53-89bd-080bcd0f017d)



### iii)Image shearing
![image](https://github.com/Madhavareddy09/IMAGE-TRANSFORMATIONS/assets/145742470/efd17af2-f796-402e-8166-1e2a30c55153)


### iv)Image Reflection
![image](https://github.com/Madhavareddy09/IMAGE-TRANSFORMATIONS/assets/145742470/66a8e1db-82fa-4602-a499-dbfe848fad09)




### v)Image Rotation
![image](https://github.com/Madhavareddy09/IMAGE-TRANSFORMATIONS/assets/145742470/49b24088-5cab-484d-8270-adcf3653a52d)



### vi)Image Cropping
![image](https://github.com/Madhavareddy09/IMAGE-TRANSFORMATIONS/assets/145742470/4f14d244-a395-4e30-82fb-9fe7be20a62e)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
