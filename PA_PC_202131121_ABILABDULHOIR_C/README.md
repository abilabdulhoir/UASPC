
# uas pengolahan citra
merupakan penjelasan dari kodingan untuk UAS pengolahan citra

penjelasan :
1. Import library yang diperlukan:
cv2 adalah library OpenCV yang digunakan untuk memanipulasi gambar.
numpy (diimport sebagai np) adalah library untuk melakukan operasi pada array dan matriks.
matplotlib (diimport sebagai plt) adalah library untuk visualisasi data.

2. Membaca gambar
Menggunakan fungsi cv2.imread() untuk membaca gambar dengan nama file 'tes6.jpg'.

3. Mengonversi gambar ke dalam ruang warna HSV:
Menggunakan fungsi cv2.cvtColor() untuk mengubah gambar dari ruang warna BGR (Blue-Green-Red) ke HSV (Hue-Saturation-Value).

4. Menentukan rentang warna merah, hijau, dan oranye dalam HSV:
red_low dan red_high adalah batas bawah dan atas untuk rentang warna merah dalam HSV.
green_low dan green_high adalah batas bawah dan atas untuk rentang warna hijau dalam HSV.
orange_low dan orange_high adalah batas bawah dan atas untuk rentang warna oranye dalam HSV.

5. Membuat mask untuk masing-masing rentang warna:
Menggunakan fungsi cv2.inRange() untuk membuat mask dari gambar dengan membatasi rentang warna yang diinginkan.

6. Melakukan dilasi pada mask merah, hijau, dan oranye:
Membuat kernel dengan ukuran tertentu menggunakan np.ones().
Menggunakan fungsi cv2.dilate() untuk melakukan operasi dilasi pada mask dengan kernel yang sudah dibuat.

7. Menggabungkan gambar asli dengan mask menggunakan operasi bitwise and:
Menggunakan fungsi cv2.bitwise_and() untuk menggabungkan gambar asli dengan mask, dengan memperhitungkan hanya piksel yang ada di mask.

8. Mengubah format warna gambar untuk ditampilkan dengan Matplotlib:
Menggunakan fungsi cv2.cvtColor() untuk mengubah format warna gambar dari BGR ke RGB atau sebaliknya. Hal ini dilakukan agar gambar dapat ditampilkan dengan benar oleh Matplotlib.

9. Menampilkan gambar-gambar tersebut dalam satu figure dengan menggunakan Matplotlib:
Membuat figure dengan ukuran 1x4 dan mengambil objek axes untuk setiap subplot.
Menggunakan imshow() untuk menampilkan gambar di setiap subplot.
Menggunakan set_title() untuk memberikan judul pada setiap subplot.

Objek yang terdeteksi adalah apel (dalam warna merah), alpukat (dalam warna hijau), dan jeruk (dalam warna oranye).

