# Menyajikan Gambar dengan Matplotlib 📊

</br>

Untuk memudahkan perbandingan dan tampilan gambar, kita dapat menggunakan Matplotlib untuk menampilkan beberapa gambar dalam satu _window_. Library Matplotlib sangat berguna untuk membandingkan beberapa gambar sekaligus. Dalam Matplotlib, fungsi `subplot()` digunakan untuk mengatur tata letak _subplot_ dalam satu _figure_. Dengan `subplot`, kita dapat menyusun beberapa plot dalam satu _figure_ secara teratur dalam baris dan kolom.

Fungsi `subplot()` membutuhkan tiga parameter utama:

```python
subplot(jumlah_baris, jumlah_kolom, index)
```

Berikut contoh penggunaan subplot menggunakan Matplotlib:

```python
import matplotlib.pyplot as plt

plt.figure(figsize=(9, 9))  # Mengatur ukuran figure
plt.suptitle("Judul Figure")

plt.subplot(2, 2, 1)
plt.title('Judul Subplot 1')
plt.imshow(img1)

plt.subplot(2, 2, 2)
plt.title('Judul Subplot 2')
plt.imshow(img2)

plt.subplot(2, 2, 3)
plt.title('Judul Subplot 3')
plt.imshow(img3)

plt.subplot(2, 2, 4)
plt.title('Judul Subplot 4')
plt.imshow(img4)

plt.tight_layout()  # Mengatur supaya subplot tidak saling tumpang tindih
plt.show()  # Menampilkan figure
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
