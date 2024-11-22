# Image_Acqusition-_using_Web_Camera
## Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
<br>
Use cv2.VideoCapture(0) to access web camera

### Step 2:
<br>
Use cv2.imread to read the video or image

### Step 3:
<br>
Use cv2.imwrite to save the image

### Step 4:
<br>
Use cv2.imshow to show the video

### Step 5:
<br>
End the program and close the output video window by pressing 'q'.

## Program:
``` Python
### Developed By: B VIJAY KUMAR
### Register No: 212222230173
```

## i) Write the frame as JPG file
```
import cv2
videoCaptureObject = cv2.VideoCapture(0)
ret, frame = videoCaptureObject.read()
if ret:
    cv2.imwrite("Vijay.jpg", frame)
videoCaptureObject.release()
cv2.destroyAllWindows()
```



## ii) Display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('VIJAY',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```



## iii) Display the video by resizing the window
```
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
    cv2.imshow('212222230173-VIJAY',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```


## iv) Rotate and display the video

```
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
    cv2.imshow('212222230173-VIJAY',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```








## Output

### i) Write the frame as JPG image
</br>
</br>

![WhatsApp Image 2024-11-22 at 12 40 58](https://github.com/user-attachments/assets/a8bf8805-6e12-4f41-97d6-0fc09b9cefee)



### ii) Display the video
</br>
</br>

![WhatsApp Image 2024-11-22 at 12 40 27](https://github.com/user-attachments/assets/21d67c8c-5f49-4d7c-89c8-e90809c53ae5)

### iii) Display the video by resizing the window
</br>
</br>

![WhatsApp Image 2024-11-22 at 12 40 31](https://github.com/user-attachments/assets/b9dd12b5-ef88-45d5-ac13-427f089950de)



### iv) Rotate and display the video
</br>
</br>

![WhatsApp Image 2024-11-22 at 12 40 33](https://github.com/user-attachments/assets/3327f502-966f-44a3-97a0-c3d5d682511f)





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
