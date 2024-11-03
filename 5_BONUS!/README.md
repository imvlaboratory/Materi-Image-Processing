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

   Untuk menampilkan stream video dari kamera atau file video:

   ```python
   while cap.isOpened():
      # Membaca frame demi frame
      ret, frame = cap.read()
      # Jika frame berhasil dibaca
      if ret:
          # Mengonversi frame menjadi grayscale
          gray = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)
          # Mendeteksi wajah pada frame grayscale
          faces = face_cascade.detectMultiScale(gray,scaleFactor=1.3,minNeighbors=5)
          # Menggambar kotak di sekitar setiap wajah yang terdeteksi
          for (x, y, w, h) in faces:
              cv2.rectangle(frame, (x, y), (x + w, y + h), (0, 255, 0), 2)
          # Menampilkan frame dengan deteksi wajah
          cv2.imshow('Video Stream', frame)
          # Tekan 'q' pada keyboard untuk keluar
          if cv2.waitKey(25) & 0xFF == ord('q'):
              break
      else:
          # Keluar dari loop jika frame tidak berhasil dibaca
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
# Membuka kamera atau file video
cap = cv2.VideoCapture(0)
# Memuat model Haar Cascade
face_cascade = cv2.CascadeClassifier("haarcascade_frontalface_default.xml")

while cap.isOpened():
    # Membaca frame demi frame
    ret, frame = cap.read()

    if ret:
        # Mengonversi frame menjadi grayscale
        gray = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)

        # Melakukan deteksi wajah
        faces = face_cascade.detectMultiScale(
            gray,
            scaleFactor=1.3,
            minNeighbors=5
        )

        # Menandai setiap wajah yang terdeteksi dengan kotak
        for (x, y, w, h) in faces:
            cv2.rectangle(frame, (x, y), (x + w, y + h), (0, 255, 0), 2)

        # Menampilkan hasil deteksi wajah
        cv2.imshow('Face Detection', frame)

        # Tekan 'Q' pada keyboard untuk keluar
        if cv2.waitKey(25) & 0xFF == ord('q'):
            break
    else:
        break

# Menutup video
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
