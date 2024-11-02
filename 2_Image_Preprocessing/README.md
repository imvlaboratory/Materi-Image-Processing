# Image Pre-processing

</br>

## **❓ Mengapa perlu Image Preprocessing?**

1. **Kompleksitas Data Gambar**

   - **Resolusi Berbeda**: Gambar dapat memiliki resolusi yang bervariasi. Perbedaan resolusi dalam sebuah dataset dapat mengganggu proses analisis atau mempengaruhi performa model.
   - **Kualitas Beragam**: Kualitas gambar dapat bervariasi, seperti adanya noise, perbedaan kecerahan, atau kontras yang tidak konsisten, yang dapat memengaruhi interpretasi dan analisis data.

2. **Kebutuhan Preprocessing**

   - **Standardisasi Data**: Proses preprocessing memungkinkan standarisasi format data gambar, seperti memastikan ukuran yang seragam atau skala warna yang konsisten, sehingga mempermudah analisis dan pemrosesan data lebih lanjut.
   - **Pembersihan Data**: Penghapusan noise, penghalusan, atau peningkatan kualitas gambar berfungsi untuk meningkatkan mutu data sebelum diproses oleh model atau algoritma.

3. **Persiapan Data untuk Model**

   - **Kesiapan untuk Machine Learning**: Preprocessing membantu dalam mempersiapkan data gambar agar sesuai untuk digunakan dalam model machine learning, termasuk langkah-langkah seperti normalisasi, ekstraksi fitur, atau augmentasi data.
   - **Efisiensi Model**: Data yang telah diproses dengan baik dapat meningkatkan efisiensi dan akurasi model, serta mengurangi waktu pelatihan.

4. **Reduksi Overhead Komputasi**
   - **Pengurangan Kompleksitas**: Beberapa teknik preprocessing, seperti pengurangan dimensi atau penyesuaian warna, dapat mengurangi kompleksitas data, sehingga mempercepat proses analisis dan komputasi.
     </br>

## **🔄 Rotate & Flip Image**

- Rotate image:

  ```python
  # Rotate 90 Degrees Clockwise
  cv2.rotate(img, cv2.ROTATE_90_CLOCKWISE)

  # Rotate 90 Degrees Counter Clockwise
  cv2.rotate(img, cv2.ROTATE_90_COUNTERCLOCKWISE)

  # Rotate 180 Degrees Clockwise
  cv2.rotate(img, cv2.ROTATE_180)
  ```

- Flip image:

  ```python
  # Flip Horizontally
  cv2.flip(img, 1)

  # Flip Vertically
  cv2.flip(img, 0)

  # Flip Horizontally & Vertically
  cv2.flip(img, -1)
  ```

</br>

## **📏 Resize & Interpolation Method**

- Resize image:

  ```python
  # Make it smaller
  cv2.resize(image, (0, 0), fx=0.5, fy=0.5)
  cv2.resize(image, (500, 500))

  # Make it bigger
  cv2.resize(image, (0, 0), fx=2, fy=2)
  cv2.resize(image, (2000, 2000))
  ```

- Interpolation method:

  - **cv2.INTER_AREA**: Digunakan saat mengecilkan gambar.

    ```python
    cv2.resize(img, (0, 0), fx=0.5, fy=0.5, interpolation=cv2.INTER_AREA)
    ```

  - **cv2.INTER_CUBIC**: Lebih lambat tapi lebih akurat.

    ```python
    cv2.resize(img, (0, 0), fx=0.5, fy=0.5, interpolation=cv2.INTER_CUBIC)
    ```

  - **cv2.INTER_LINEAR**: Digunakan saat memperbesar gambar dan merupakan metode interpolasi default pada OpenCV.

    ```python
    cv2.resize(img, (0, 0), fx=0.5, fy=0.5, interpolation=cv2.INTER_LINEAR)
    ```

</br>

## **🌈 Lebih Lanjut Mengenai Color Space**

OpenCV mendukung banyak color space, yang dapat dilihat pada dokumentasi resmi OpenCV [di sini](https://docs.opencv.org/3.4/d8/d01/group__imgproc__color__conversions.html). Berikut adalah beberapa yang sering digunakan:

```python
# RGB ke GRAY dan sebaliknya
cv2.cvtColor(cv2.COLOR_RGB2GRAY)
cv2.cvtColor(cv2.COLOR_GRAY2RGB)

# RGB ke BGR dan sebaliknya
cv2.cvtColor(cv2.COLOR_BGR2RGB)
cv2.cvtColor(cv2.COLOR_RGB2BGR)

# RGB ke HSV dan sebaliknya
cv2.cvtColor(cv2.COLOR_RGB2HSV)
cv2.cvtColor(cv2.COLOR_HSV2RGB)

# RGB ke LAB dan sebaliknya
cv2.cvtColor(cv2.COLOR_RGB2LAB)
cv2.cvtColor(cv2.COLOR_LAB2RGB)
```

</br>

## 📊 Histogram

Dengan histogram, kita bisa melihat distribusi warna pada suatu gambar.

```python
img = cv2.imread("../assets/Enid.jpeg")

# Calculate RGB Channel Histogram
histrBlue = cv2.calcHist([img], [0], None, [256], [0, 256])
histrGreen = cv2.calcHist([img], [1], None, [256], [0, 256])
histrRed = cv2.calcHist([img], [2], None, [256], [0, 256])

# Convert RGB to GRAY
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

# Calculate GRAY Channel Histogram
equHistr = cv2.calcHist([gray], [0], None, [256], [0, 256])
```

</br>

<div style="text-align: center; margin: 24px;">
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
