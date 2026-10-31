# Image Capture and Video Processing Using OpenCV

---

## Aim:

To write a Python program using OpenCV to capture an image from the webcam and perform the following operations:
1. Write the frame as a JPG file  
2. Display the video  
3. Display the video by resizing the window  
4. Rotate and display the video  

---

## Software Used:

- Anaconda – Python 3.7  
- Jupyter Notebook / VS Code  
- OpenCV (`cv2`)  

---

## Algorithm:

### Step 1:
Import the required libraries and initialize the webcam using `cv2.VideoCapture()`.

### Step 2:
Capture frames continuously from the webcam.

### Step 3:
Save a frame as a JPG image using `cv2.imwrite()`.

### Step 4:
Display the live video stream using `cv2.imshow()`.

### Step 5:
Resize the frame and rotate it using OpenCV functions, then display the processed frames.

---

## Program:

### Developed By:
**Name:** DAKSHA SUBBAIAN

**Register No:** 212223230036 

### i) Write the frame as JPG image
```
cap = cv2.VideoCapture(0)

ret, frame = cap.read()

if ret:
    cv2.imwrite("captured_image.jpg", frame)
    print("Image saved as captured_image.jpg")
else:
    print("Failed to capture image")

cap.release()

```

### ii) Display the video
```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()

    if not ret:
        break

    frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)

    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis("off")
    plt.show()

    time.sleep(0.05)

cap.release()
```

### iii) Display the video by resizing the window (640 x 480)
```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()

    if not ret:
        break

    resized_frame = cv2.resize(frame, (640, 480))
    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)

    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis("off")
    plt.show()

    time.sleep(0.05)

cap.release()

```
### iv) Rotate and display the video (90 degrees clockwise)
```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()

    if not ret:
        break

    rotated_frame = cv2.rotate(
        frame, cv2.ROTATE_90_CLOCKWISE
    )

    frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)

    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis("off")
    plt.show()

    time.sleep(0.05)

cap.release()
```
## Output:
### i) Write the frame as JPG image
<img width="638" height="508" alt="image" src="https://github.com/user-attachments/assets/1bcb9fd7-cf4f-4a59-aee3-a86819a1f4d2" />



### ii) Display the video
<img width="636" height="485" alt="image" src="https://github.com/user-attachments/assets/d8736108-529d-4381-be74-e96a7fbb0b22" />



### iii) Display the video by resizing the window
<img width="328" height="486" alt="image" src="https://github.com/user-attachments/assets/1714c6fa-2282-4ca6-8f09-57cd2e074d53" />



### iv) Rotate and display the video
<img width="375" height="482" alt="image" src="https://github.com/user-attachments/assets/253c1299-1c6f-414c-82ed-c0b8c9e690e1" />


---

## Result:
Thus, the image is successfully captured from the webcam and various video processing operations such as saving, displaying, resizing, and rotating are performed using OpenCV.
