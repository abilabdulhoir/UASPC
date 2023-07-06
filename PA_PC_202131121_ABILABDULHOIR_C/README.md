
# uas pengolahan citra
Penjelasan Teori Program Pengolahan Citra yaitu segmentasi warna :
Segmentasi warna dalam pengolahan citra adalah proses pemisahan atau pengelompokan piksel-piksel citra berdasarkan perbedaan warna mereka. Tujuan utama segmentasi warna adalah untuk mengidentifikasi objek atau wilayah tertentu dalam citra berdasarkan karakteristik warna mereka.

Berikut adalah langkah-langkah dalam proses segmentasi warna pengolahan citra:

1. Pra-pemrosesan: Tahap ini melibatkan pra-pemrosesan citra, seperti pengurangan noise atau peningkatan kontras, untuk mempersiapkan citra sebelum dilakukan segmentasi warna. Tujuan utamanya adalah meningkatkan kualitas citra dan memperjelas perbedaan warna antar objek.

2. Konversi ruang warna: Citra asli biasanya dikonversi dari ruang warna RGB (Red-Green-Blue) ke ruang warna yang lebih sesuai untuk segmentasi warna, seperti ruang warna HSV (Hue-Saturation-Value) atau ruang warna Lab (Lab*). Konversi ini memungkinkan pemisahan komponen warna yang independen, yang memudahkan identifikasi objek berdasarkan perbedaan nilai hue, saturasi, atau komponen warna lainnya.

3. Pemilihan kriteria segmentasi: Langkah ini melibatkan pemilihan kriteria atau aturan untuk memisahkan objek berdasarkan nilai-nilai tertentu dalam ruang warna yang dipilih. Misalnya, Anda dapat memilih range nilai hue tertentu untuk memisahkan objek dengan warna tertentu dari latar belakang.

4. Segmentasi piksel: Pada langkah ini, setiap piksel dalam citra diklasifikasikan ke dalam kelompok-kelompok berdasarkan kriteria segmentasi yang telah ditentukan. Metode yang umum digunakan dalam segmentasi warna adalah metode k-means clustering, di mana piksel-piksel dielompokkan berdasarkan kesamaan warna mereka.

5. Post-processing: Setelah segmentasi awal, tahap ini melibatkan pemrosesan lanjutan untuk memperbaiki dan membersihkan hasil segmentasi. Ini mungkin melibatkan penghapusan noise kecil, penghubungan wilayah yang terputus, atau pemisahan wilayah yang tumpang tindih.

6. Analisis dan penggunaan hasil segmentasi: Setelah segmentasi warna selesai, hasilnya dapat digunakan untuk berbagai tujuan, seperti pengenalan objek, pemisahan latar belakang dan objek, pengukuran objek, pelacakan objek, atau aplikasi lain yang memerlukan informasi warna yang tersegmentasi.

Segmentasi warna adalah teknik yang berguna dalam berbagai aplikasi pengolahan citra, seperti visi komputer, pengenalan pola, robotika, pengawasan keamanan, dan banyak lagi. Dengan memahami dan menerapkan langkah-langkah segmentasi warna yang tepat, kita dapat menghasilkan pemrosesan citra yang lebih efektif dan akurat dalam mengidentifikasi objek berdasarkan karakteristik warna mereka, oleh karena itu dalam UAS Pengolahan citra kali ini saya mendapatkan bagian segmentasi warna untuk 3 buah-buahan yang warnanya berbeda dan berdekatan.

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

