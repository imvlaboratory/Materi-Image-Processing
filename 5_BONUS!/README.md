# BONUS MATERIALS 🎁

## Working with Video

1. Open Video

   Berikut adalah beberapa cara untuk membuka video menggunakan OpenCV:

   ```python
   # Membuka kamera pertama (webcam default)
   cap = cv2.VideoCapture(0)

   # Membuka kamera kedua
   cap = cv2.VideoCapture(1)

   # Membuka file video
   cap = cv2.VideoCapture('path_to_file')
   ```

2. Stream Video

   Untuk menampilkan video stream dari kamera atau video file:

   ```python
   while cap.isOpened():
       ret, frame = cap.read()
       if ret:
           cv2.imshow('Video Stream', frame)
           if cv2.waitKey(25) & 0xFF == ord('q'):
               break
       else:
           break
   ```

3. Close Video

   Setelah selesai, pastikan untuk menutup video dan melepaskan resource yang digunakan:

   ```python
   cap.release()
   cv2.destroyAllWindows()
   ```

</br>

## Haar Cascade Classifier on Video

```python
cap = cv2.VideoCapture(0)
face_cascade = cv2.CascadeClassifier("haarcascade_frontalface_default.xml")

while cap.isOpened():
    ret, frame = cap.read()

    if ret:
        gray = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)

        faces = face_cascade.detectMultiScale(
            gray,
            scaleFactor=1.3,
            minNeighbors=5
        )

        for (x, y, w, h) in faces:
            cv2.rectangle(
                frame,
                (x, y),
                (x + w, y + h),
                (0, 255, 0),
                2
            )

        cv2.imshow('Realtime Face Detection', frame)

        if cv2.waitKey(25) & 0xFF == ord('q'):
            break
    else:
        break

cap.release()
cv2.destroyAllWindows()
```

</br>

<div style="text-align: center; margin-top: 24px;">
  <a href="../README.md" style="
    display: inline-block;
    background-color: #e3383a;
    color: #fff;
    padding: 12px 24px;
    font-size: 16px;
    font-weight: bold;
    text-decoration: none;
    border-radius: 8px;
    transition: background-color 0.15s;
  " onmouseover="this.style.backgroundColor='#4caf50';" onmouseout="this.style.backgroundColor='#e3383a';">
    Kembali
  </a>
</div>
