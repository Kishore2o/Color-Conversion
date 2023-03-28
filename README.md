# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 and save and image as filename.jpg

### Step2:
Use imread(filename, flags) to read the file

### Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

### Step4:
Split and merge the image using cv2.split and cv2.merge commands.

### Step5:
End the program and close the output image windows.

## Program:
```python
# Developed By:S.Kishore
# Register Number:212222240050
# ORIGINAL IMAGE
import cv2
rick_color_image = cv2.imread('rick.jpg')
cv2.imshow('Original image', rick_color_image)
cv2.waitKey(0)
cv2. destroyAllWindows()



# i) Convert BGR and RGB to HSV and GRAY
import cv2
rick_color_image = cv2.imread('rick.jpg')
hsv_image = cv2.cvtColor(rick_color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV' ,hsv_image )
hsv_imagel = cv2.cvtColor(rick_color_image, cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV' , hsv_imagel)
gray_image = cv2.cvtColor(rick_color_image, cv2.COLOR_BGR2GRAY)
cv2.imshow( 'BGR2GRAY', gray_image)
gray_image1 = cv2.cvtColor (rick_color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()



# ii)Convert HSV to RGB and BGR
import cv2
rick_HSV_image = cv2.imread('rick.jpg')
RGB_image = cv2.cvtColor(rick_HSV_image,cv2.COLOR_HSV2RGB)
cv2.imshow('HSV to RGB',RGB_image )
BGR_image = cv2.cvtColor(rick_HSV_image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV to BGR',BGR_image)
cv2.waitKey(0)
cv2.destroyAllWindows()






# iii)Convert RGB and BGR to YCrCb
import cv2
rick_color_image = cv2.imread('rick.jpg')
YCrCb_image = cv2.cvtColor(rick_color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb',YCrCb_image)
YCrCb_image1 = cv2.cvtColor(rick_color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb',YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()


# iv)Split and Merge RGB Image

import cv2
image = cv2.imread('rick.jpg')
blue=image[:,:,0]
green=image[:,:,1]
red=image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()


# v) Split and merge HSV Image
import cv2
image=cv2.imread('rick.jpg')
hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h,s,v=cv2.split(hsv)
cv2.imshow("Hue-image",h)
cv2.imshow("Saturation-image",s)
cv2.imshow("gray-image",v)
Merged_HSV=cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()




```
## Output:
### Original

![OUTPUT](./images/original.png)


### i) BGR and RGB to HSV and GRAY
![image](https://user-images.githubusercontent.com/118679883/228126080-af5836f3-a706-4331-9d15-7766c261555b.png)
![image](https://user-images.githubusercontent.com/118679883/228126121-9981f2e6-f624-4d52-9d4e-1ec46c7547d3.png)
![image](https://user-images.githubusercontent.com/118679883/228126099-e94b574a-a0ae-4d20-bc8f-5322ba92e31b.png)
![image](https://user-images.githubusercontent.com/118679883/228126139-3c364ae4-e471-4fd8-ba74-804b7bf5c184.png)


### ii) HSV to RGB and BGR
![image](https://user-images.githubusercontent.com/118679883/228126160-2342f0b1-c945-4be6-aa52-424472f56e04.png)
![image](https://user-images.githubusercontent.com/118679883/228126444-ab019a95-2019-4903-97dc-025c9dd6205f.png)

### iii) RGB and BGR to YCrCb
![image](https://user-images.githubusercontent.com/118679883/228126483-079a409b-f102-4d10-9c57-40c4a9145cc7.png)
![image](https://user-images.githubusercontent.com/118679883/228126499-e4f1c212-6111-4a8e-b388-3ee999888e01.png)


### iv) Split and merge RGB Image
![image](https://user-images.githubusercontent.com/118679883/228126519-b369a36b-ce3d-4e32-835e-024739b874b0.png)
![image](https://user-images.githubusercontent.com/118679883/228126539-7ac88f33-13e4-434f-8c74-e5cc090af6a1.png)
![image](https://user-images.githubusercontent.com/118679883/228126556-a6c2a832-044c-4529-bf83-cb62610dfb61.png)
![image](https://user-images.githubusercontent.com/118679883/228126601-733d984a-e856-4d34-969a-178196ad311e.png)


### v) Split and merge HSV Image
![image](https://user-images.githubusercontent.com/118679883/228126618-eefd76c0-5ca2-45dc-adc8-bd17f48d69ac.png)
![image](https://user-images.githubusercontent.com/118679883/228126638-dcd8fdef-b383-4ce0-8a4e-d77358479387.png)
![image](https://user-images.githubusercontent.com/118679883/228126662-fe7b2390-3978-451f-9135-759ea9116ab7.png)
![image](https://user-images.githubusercontent.com/118679883/228126690-8299a438-393a-4608-8509-7b72d3c76471.png)



## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
