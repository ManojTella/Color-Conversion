# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import opencv.
<br>

### Step2:
Read the original Image.
<br>

### Step3:
Store the required conversion of the image in a variable.
<br>

### Step4:
Show the image stored in the given variable.
<br>

### Step5:
Destroy all the windows and end the program.
<br>

## Program:
```python
# Developed By:Manoj Guna Sundar Tella.
# Register Number:212221240026.
# i) Convert BGR and RGB to HSV and GRAY.
import cv2
houseImage = cv2.imread('butterfly.jpg')
cv2.imshow('Original Image',buterflyImage)
hsvImage = cv2.cvtColor(butterflyImage,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsvImage)
hsvImage1=cv2.cvtColor(butterflyImage,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsvImage1)
grayImage = cv2.cvtColor(butterflyImage,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',grayImage)
grayImage1 = cv2.cvtColor(butterflyImage,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',grayImage1)
cv2.waitKey(0)
cv2.destroyAllWindows()





# ii)Convert HSV to RGB and BGR.
import cv2
houseHSVImage = cv2.imread('butterfly.jpg')
cv2.imshow('Original HSV Image',butterflyHSVImage)
RGBImage = cv2.cvtColor(butterflyHSVImage,cv2.COLOR_HSV2RGB)
cv2.imshow('BGR2HSV',RGBImage)
BGRImage=cv2.cvtColor(butterflyHSVImage,cv2.COLOR_HSV2BGR)
cv2.imshow('RGB2HSV',BGRImage)
cv2.waitKey(0)
cv2.destroyAllWindows()






# iii)Convert RGB and BGR to YCrCb.
import cv2
houseImage = cv2.imread('butterfly.jpg')
cv2.imshow('Original HSV Image',butterImage)
YCrCb_image = cv2.cvtColor(butterflyImage, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR2HSV',YCrCb_image)
YCrCb_image1 = cv2.cvtColor(butterflyImage, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB2HSV',YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()




# iv)Split and Merge RGB Image.
import cv2
image = cv2.imread('butterfly.jpg')
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
mergeBgr = cv2.merge((blue,green,red))
cv2.imshow('Merged BGR image',mergeBgr)
cv2.waitKey(0)
cv2.destroyAllWindows()




# v) Split and merge HSV Image
import cv2
image = cv2.imread('butterfly.jpg')
hsv = cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue - Image',h)
cv2.imshow('Saturation - Image',s)
cv2.imshow('Gray - Image',v)
mergedHSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',mergedHSV)
cv2.waitKey(0)
cv2.destroyAllWindow




```
## Output:
### i) BGR and RGB to HSV and GRAY
![par1](https://user-images.githubusercontent.com/94883876/162446310-0290f855-2c10-4c70-9fee-4047a956d073.png)

<br>
<br>

### ii) HSV to RGB and BGR
![par2](https://user-images.githubusercontent.com/94883876/162446357-587c9a8c-fdf6-48b8-81d3-317c2ffea2b0.png)

<br>
<br>

### iii) RGB and BGR to YCrCb
![par3](https://user-images.githubusercontent.com/94883876/162446410-d134f5ba-b9e2-4e84-8f52-f58b39944e3b.png)

<br>
<br>

### iv) Split and merge RGB Image
![par4](https://user-images.githubusercontent.com/94883876/162446444-b4a3de41-05f9-4564-adbc-4d80cc11ed55.png)

<br>
<br>

### v) Split and merge HSV Image
![par5](https://user-images.githubusercontent.com/94883876/162446477-93456ecd-1666-4c3d-aa41-9a0c6425ef49.png)

<br>
<br>


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
