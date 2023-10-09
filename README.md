# COLOR-CONVERSION
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
Step1:
Import opencv

Step2:
Read the original Image.

Step3:
Store the required conversion of the image in a variable.

Step4:
Show the image stored in the given variable.

Step5:
Destroy all the windows and end the program.

## Program:
```
python
# Developed By: G.Lutheesh
# Register Number: 212221230029
```
## i) Convert BGR and RGB to HSV and GRAY
```
house_color_image= cv2.imread('house.jpg')
cv2.imshow ('Original image', house_color_image)
hsv_image= cv2.cvtColor (house_color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV', hsv_image)
hsv_image1 = cv2.cvtColor (house_color_image, cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV', hsv_image1)
gray_image= cv2.cvtColor (house_color_image, cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY', gray_image)
gray_image1 = cv2.cvtColor (house_color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```





## ii)Convert HSV to RGB and BGR
```
import cv2
house_HSV_image= cv2.imread('house.jpg')
cv2.imshow('Original HSV image',house_HSV_image)
RGB_image = cv2.cvtColor(house_HSV_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV to RGB',RGB_image )
BGR_image = cv2.cvtColor(house_HSV_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV to BGR',BGR_image)
cv2.waitKey(0)
cv2.destroyAllwindows()
```





## iii)Convert RGB and BGR to YCrCb
```
import cv2
houseImage = cv2.imread('house.jpg')
cv2.imshow('Original HSV Image',houseImage)
YCrCb_image = cv2.cvtColor(houseImage, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR2HSV',YCrCb_image)
YCrCb_image1 = cv2.cvtColor(houseImage, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB2HSV',YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```



## iv)Split and Merge RGB Image
```
import cv2
image = cv2.imread('house.jpg')
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
```




## v) Split and merge HSV Image
```
import cv2
image = cv2.imread('house.jpg')
hsv = cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue - Image',h)
cv2.imshow('Saturation - Image',s)
cv2.imshow('Gray - Image',v)
mergedHSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',mergedHSV)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### i) BGR and RGB to HSV and GRAY
![va1](https://github.com/Lutheeshgoparapu/COLOR-CONVERSION/assets/94154531/9ccf741b-4def-49d2-b269-8be049065c94)


### ii) HSV to RGB and BGR
![va2](https://github.com/Lutheeshgoparapu/COLOR-CONVERSION/assets/94154531/a60ce681-1aa2-4ea3-b558-77fb17d3be0d)


### iii) RGB and BGR to YCrCb
![va3](https://github.com/Lutheeshgoparapu/COLOR-CONVERSION/assets/94154531/e1a89adc-7490-4758-b3f2-ce5a2384e1ba)


### iv) Split and merge RGB Image
![va4](https://github.com/Lutheeshgoparapu/COLOR-CONVERSION/assets/94154531/cfd16749-dc00-4e02-ba15-dbfa1387443f)

### v) Split and merge HSV Image
![va5](https://github.com/Lutheeshgoparapu/COLOR-CONVERSION/assets/94154531/e5089ad4-3391-4ab6-b702-7ff462b4355e)



## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
