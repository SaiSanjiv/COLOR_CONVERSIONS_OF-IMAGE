# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
1.  Draw a line from the top-left to the bottom-right of the image.

2.	Draw a circle at the center of the image.

3.	Draw a rectangle around a specific region of interest in the image.

4.	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
1.	Convert the image from RGB to HSV and display it.
2.	Convert the image from RGB to GRAY and display it.
3.	Convert the image from RGB to YCrCb and display it.
4.	Convert the HSV image back to RGB and display it.

### Step4:
1.	Access and print the value of the pixel at coordinates (100, 100).
2.	Modify the color of the pixel at (200, 200) to white.

### Step5:
Resize the original image to half its size and display it.
### Step6:
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
1.	Flip the original image horizontally and display it.
2.	Flip the original image vertically and display it.

### Step8:
Save the final modified image to your local directory.


## Program:
### Developed By: SAI SANJIV R
### Register Number: 212223230179


## Output:

### 1. Read and display the image
i.Load an image from your local directory and display it.
```
img=cv2.imread("strawhat.jpeg")
cv2.imshow("display", img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/d37179bd-15b8-453b-be23-b6bee06c80a5)


### Draw Shapes and Add Text
(1) Draw a line from the top-left to the bottom-right of the image.
```
img=cv2.imread("strawhat.jpeg")
line=cv2.line(img,(0,0),(736,414),(0,0,255),10)
plt.imshow(line)
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/ade58724-ba27-4d7d-a08d-6cdf81f68a7d)


2. Draw a circle at the center of the image.
```
img=cv2.imread("strawhat.jpeg")
circle=cv2.circle(img,(400,200),(150),(255,0,0),10)
plt.imshow(circle)
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/ea6881ee-5b4c-4a55-9954-06c8280e7190)


3.Draw a rectangle around a specific region of interest in the image.
```
image = cv2.imread("strawhat.jpeg")
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
l = (200, 100) 
b = (550, 300)  
rectangle = cv2.rectangle(image_rgb, l, b, (255, 0, 0), 5)
plt.imshow(rectangle)
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/0ca01665-6f6f-4679-af14-6940198ffd9d)



4.Add the text "OpenCV Drawing" at the top-left corner of the image.
```
iimport cv2
import matplotlib.pyplot as plt
image = cv2.imread("strawhat.jpeg")
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image_rgb, 'OpenCV Drawing', (50, 50), font, 1, (255, 0, 0), 2, cv2.LINE_AA)
plt.imshow(image_rgb)
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/fcb8c188-5c42-4e32-9d3c-b2dcc54a5751)


### iii)Image Color Conversion
(i)Convert the image from RGB to HSV and display it
```
import cv2
image = cv2.imread('strawhat.jpeg',1)
cv2.imshow('ORIGINAL IMAGE',image)
hsv = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/3f56e2bb-8750-42a5-bb56-8c0c2ac7868a)


(2) Convert the image from RGB to GRAY and display it.

```
import cv2
image = cv2.imread('strawhat.jpeg',1)
cv2.imshow('ORIGINAL IMAGE',image)
gray = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/1cd69d0f-a53d-4dac-8e68-31e7bfff2c50)



(3) Convert the image from RGB to YCrCb and display it.
```
import cv2
image = cv2.imread('strawhat.jpeg',1)
cv2.imshow('ORIGINAL IMAGE',image)
YCrCb = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/8250fb00-53d9-46cf-a224-a7ea3ceb602d)


(4) Convert the HSV image back to RGB and display it.
```
import cv2
image = cv2.imread('strawhat.jpeg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
RGB = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',RGB)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/063a6305-abcb-4e3d-96d8-98b2442a06ad)


### iv)Access and Manipulate Image Pixels
(1) Access and print the value of the pixel at coordinates (100, 100)
```
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
```
![image](https://github.com/user-attachments/assets/0fa6b1ac-d44b-4820-817c-946639a361a8)


(2) Modify the color of the pixel at (200, 200) to white
```
import cv2
image = cv2.imread('strawhat.jpeg',1)
image = cv2.resize(image,(400,300))
cv2.imshow('ORIGINAL IMAGE',image)
image[200, 200] = [255, 255, 255] 
cv2.imshow('MODIFIED IMAGE', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/e82aaf8a-efd2-4da2-b37a-add17c3fbfaf)


### v)Image Resizing:
Resize the original image to half its size and display it.
```
cv2.imshow('ORIGINAL IMAGE',image)
resized_image = cv2.resize(image, (350,200))
cv2.imshow('RESIZED IMAGE', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/7523d7b5-8811-4485-8572-0b4f674235c3)


### vi)Image Cropping
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```
import cv2
image = cv2.imread('strawhat.jpeg',1)
image = cv2.resize(image,(400,300))
x, y = 50, 50
width, height = 100, 100
roi = image[y:y + height, x:x + width]
cv2.imshow('CROPPED IMAGE', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/47f1a7e4-9b05-45b5-b6f9-270082ee4ed1)

### vii)Image Flipping:
(1) Flip the original image horizontally and display it.
```
import cv2
image = cv2.imread("strawhat.jpeg")
image= cv2.resize(image, (400,300))
res=cv2.rotate(image,cv2.ROTATE_180)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/00453786-d5a4-45eb-89e3-65486d90621a)


(2) Flip the original image vertically and display it.
```
import cv2
image = cv2.imread("strawhat.jpeg")
image= cv2.resize(image, (400,400))
res=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/103a34b5-23c2-41b3-9959-9d163ab4759b)


### viii)Write and Save the Modified Image
Save the final modified image to your local directory.
```
import cv2
img = cv2.imread("strawhat.jpg")
cv2.imwrite('luffy.jpg',img)
```
![image](https://github.com/user-attachments/assets/30936b2a-9e5a-45e7-9388-291db6e4156e)


## Result:

Thus the images are read, displayed, and written ,and color conversion was performed successfully using the python program.







