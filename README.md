# Image_Acqusition-_using_Web_Camera.

### Developed By: NAVEEN RAJA N R
### Register No: 212222230093
### Date:

## Aim:
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used:
Anaconda - Python 3.7

## Algorithm:

### Step 1:
Use cv2.VideoCapture(0) to access web camera

### Step 2:
Use cv2.imread to read the video or image

### Step 3:
Use cv2.imwrite to save the image

### Step 4:
Use cv2.imshow to show the video

### Step 5:
End the program and close the output video window by pressing 'q'.

## Program:
```
 Developed By:Anbuselvan.S
 Register No:212223240008
```
## i) Write the frame as JPG file
```py
import cv2
viedoCaptureObject=cv2.VideoCapture(0)
while(True):
    ret,frame=viedoCaptureObject.read()
    cv2.imwrite("Anbuselvan.jpg",frame)
    result=False
viedoCaptureObject.release()
cv2.destroyAllWindows()
```


## ii) Display the video

```py
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('Anbuselvan',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## iii) Display the video by resizing the window
```py
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('Anbuselvan 212223240008',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```



## iv) Rotate and display the video
```py
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('Anbuselvan 212223240008',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```







## Output

### i) Write the frame as JPG image
![Screenshot 2024-09-26 201025](https://github.com/user-attachments/assets/dca97b54-272f-4276-af0e-2ea4c4327fad)

### ii) Display the video

![Screenshot 2024-09-26 201231](https://github.com/user-attachments/assets/3ac81614-f052-47dd-ab77-cf0b59f00681)

### iii) Display the video by resizing the window

![Screenshot 2024-09-26 201329](https://github.com/user-attachments/assets/5dd980ea-1d68-493b-8b75-452344fd854d)

### iv) Rotate and display the video

![Screenshot 2024-09-26 201450](https://github.com/user-attachments/assets/2c048466-e83b-4d16-b475-a6f3f8bdbde3)

## Result:
Thus the image is accessed from webcamera and displayed using openCV.
