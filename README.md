<div style="display: flex; align-items: center; justify-content: center;" align="center">
    <img src="displays/Banner_Github_Image_Processing.png" alt="Banner">
</div>

</br>

## **Sebelum Dimulai** ⚠️

</br>

<div style="display: flex; align-items: center; justify-content: center;" align="center">
    <img src="https://opencv.org/wp-content/uploads/2022/05/logo.png" alt="OpenCV" style="height: 50px; margin-right: 10px;">
    <img src="https://matplotlib.org/stable/_static/logo_dark.svg" alt="Numpy" style="height: 50px; margin-right: 10px;">
    <img src="https://upload.wikimedia.org/wikipedia/commons/3/31/NumPy_logo_2020.svg" alt="Matplotlib" style="height: 50px;">
</div>

</br>
</br>

### 1. Setup Enviroment

Dalam _course_ ini, kita akan menggunakan _library_ [**`OpenCV Python`**](https://pypi.org/project/opencv-python/) untuk memanipulasi gambar. Sebelum memulai, install terlebih dahulu _library_ yang diperlukan dengan menjalankan perintah di bawah ini pada terminal:

```bash
pip install opencv-python
```

Kita juga membutuhkan _library_ [**`NumPy`**](https://numpy.org/) dan [**`Matplotlib`**](https://matplotlib.org/) untuk mengolah dan plot gambar. Install keduanya dengan perintah berikut:

```bash
pip install numpy
```

```bash
pip install matplotlib
```

Atau bisa langsung menggunakan perintah berikut untuk menginstall semua _library_ secara bersamaan:

```bash
pip install opencv-python numpy matplotlib
```

</br>

### 2. Setup Menggunakan Virtual Environtment

Untuk menghindari konflik dengan _library_ yang sudah terinstal pada sistem, kita dapat menggunakan _virtual environment_ untuk membuat _environtment_ yang `terisolasi`. Ikuti langkah-langkah berikut untuk membuat dan mengaktifkan _virtual environment_:

- Install terlebih dahulu _library_ `virtualenv`

  ```bash
  pip install virtualenv
  ```

- Buat _virtual environment_ baru dengan nama `env`

  ```bash
  python -m venv env
  ```

- Aktifkan _virtual environment_ yang baru saja dibuat

  - untuk pengguna **Windows**

    ```bash
    # Jika menggunakan Terminal CMD
    env/Scripts/activate.bat
    # Jika menggunakan Terminal PowerShell
    env/Scripts/Activate.ps1
    ```

  - untuk pengguna **MacOS**

    ```bash
    source env/bin/activate
    ```

  _environtment_ aktif ditandai dengan nama _environtment_ pada terminal

  ![Environtment Active](/displays/Environtment_Active.png)

- Setelah _virtual environment_ aktif, install _library_ yang dibutuhkan

  ```bash
  pip install -r requirements.txt
  ```

</br>

## **Topik Bahasan** 📖

0. **[Pendahuluan 📘](/0_Pendahuluan/README.md)**

   - 🤔 Apa Itu Image Processing?
   - 🌐 Aplikasi dari Image Processing

1. **[Working with Images 🖼️](/1_Working_With_Images/README.md)**

   - 📸 Gambar Itu Apa Sih?
   - 📂 Format Gambar
   - 🌈 Color Space pada Gambar
   - 📥 Membaca, Menampilkan, & Menyimpan Gambar
   - ➕ Operasi Aritmatika Sederhana pada Gambar

2. **[Image Pre-processing 🔧](/2_Image_Preprocessing/README.md)**

   - ❓ Mengapa Perlu Image Preprocessing?
   - 🔄 Rotate & Flip Image
   - 📏 Resize & Interpolation Method
   - 🌈 Lebih Lanjut Mengenai Color Space
   - 📊 Histogram

3. **[Menyajikan Gambar dengan Matplotlib 📊](/3_Presenting_Images/README.md)**

4. **[Simple Image Processing ✨](/4_Simple_Image_Processing/README.md)**

   - 😎 Face Detection

5. **[BONUS! 🎁](/5_BONUS!/README.md)**
