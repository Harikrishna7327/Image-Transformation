# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image using
M=np.float32([[1,0,20],[0,1,50],[0,0,1]])
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step3:
Scale the image using
M=np.float32([[1.5,0,0],[0,2,0],[0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step4:
Shear the image using
M_x=np.float32([[1,0.2,0],[0,1,0],[0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))

### Step5:
Reflection of image can be achieved through the code
M_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
### Step 6:
Rotate the image using
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step 7:
Crop the image using
cropped_img=input_img[20:150,60:230]

### Step 8:
Display all the Transformed images.

## Program:
```python
Developed By: M Harikrishna
Register Number:212221230059
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("img.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape

i)Image Translation
M=np.float32([[1,0,20],
             [0,1,50],
             [0,0,1]])
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_img)
plt.show()

ii) Image Scaling
M=np.float32([[1.5,0,0],
             [0,2,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()

iii)Image shearing
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
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()




vi)Image Cropping
cropped_img=input_img[20:150,60:230]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()




```
## Output:
### i)Image Translation
![download](https://user-images.githubusercontent.com/94882905/231412787-e6f59478-a995-4ae1-9793-6f2581a66002.png)

![download](https://user-images.githubusercontent.com/94882905/231412807-5a8ff8a8-77e4-4e7a-b295-157333547c9b.png)


### ii) Image Scaling
![download](https://user-images.githubusercontent.com/94882905/231412726-6eeab2c7-46df-4263-a80c-ee470b76915e.png)



### iii)Image shearing
![download](https://user-images.githubusercontent.com/94882905/231412665-d815c0a3-3a58-46b3-b440-33065b8fa42d.png)

![download](https://user-images.githubusercontent.com/94882905/231412693-1dd16b92-debe-4c06-b01e-3bbac5027e1d.png)




### iv)Image Reflection
![download](https://user-images.githubusercontent.com/94882905/231411642-12c0fb7a-c16d-4baa-af05-6395a2792c16.png)

![download](https://user-images.githubusercontent.com/94882905/231411692-2c9f915e-ff14-47cb-a246-e3f42536499b.png)


### v)Image Rotation

![download](https://user-images.githubusercontent.com/94882905/231412254-dd9b497d-f670-421c-8cf9-9c60d5d102b0.png)


### vi)Image Cropping

![download](https://user-images.githubusercontent.com/94882905/231412304-5a2e0744-52a3-4615-9a4a-4acabebf2631.png)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
