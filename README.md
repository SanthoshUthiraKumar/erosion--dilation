## EX 09 Implementation-of-Erosion-and-Dilation
### Aim
To implement Erosion and Dilation using Python and OpenCV.
### Software Required
1. Anaconda - Python 3.7
2. OpenCV
### Algorithm:
#### Step1:<br>
Import the necessary pacakages

#### Step2:<br>
Create the text using cv2.putText

#### Step3:<br>
Create the structuring element

#### Step4:<br>
Erode the image


#### Step5: <br>
Dilate the Image

 
### Program:
```
NAME: Santhosh U
REG.NO: 212222240092
```

##### Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
##### Create the Text using cv2.putText
``` Python
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'Santhosh',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
##### Create the structuring element
``` Python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
##### Erode the image
``` Python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

```
##### Dilate the image
``` Python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')



```
### Output:
#### Display the input Image
![Output1](https://github.com/SanthoshUthiraKumar/erosion--dilation/assets/119477975/47cbe6a7-ef74-498c-8609-258ba6a83e4c)

#### Display the Eroded Image
![Output2](https://github.com/SanthoshUthiraKumar/erosion--dilation/assets/119477975/1d087117-d38b-40db-b8ab-398c36f5e97c)

#### Display the Dilated Image
![Output3](https://github.com/SanthoshUthiraKumar/erosion--dilation/assets/119477975/0b7d9667-1f9f-43b5-9aea-e0b47c0a7429)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
