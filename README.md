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
<img width="632" height="505" alt="image" src="https://github.com/user-attachments/assets/0affbae9-7d2d-4a00-b4ef-7b76db3ce4eb" />


### ii) Display the video
<img width="635" height="482" alt="image" src="https://github.com/user-attachments/assets/0dfcc860-8885-40c2-a3bd-796e1d9539ba" />


### iii) Display the video by resizing the window
<img width="332" height="486" alt="image" src="https://github.com/user-attachments/assets/4f629a88-19c2-4c66-847a-209deb2960c8" />


### iv) Rotate and display the video
<img width="370" height="482" alt="image" src="https://github.com/user-attachments/assets/5086932b-a030-4cff-bd5d-6b4a6bf2647c" />


---

## Result:
Thus, the image is successfully captured from the webcam and various video processing operations such as saving, displaying, resizing, and rotating are performed using OpenCV.
