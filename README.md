# SIG_TEORI_TGS_22
 Animating Time Series Data
Langkah Kerja Peta 8: Animating Time Series Data (QGIS3)

1. Di Panel Peramban QGIS, temukan direktori tempat Anda menyimpan data unduhan. Luaskan ne_10m_land.zip dan pilih layer ne_10m_land.shp. Seret layer ke kanvas. Selanjutnya, cari file ASAM_shp.zip. Luaskan dan pilih layer asam_data_download/ASAM_events.shp dan seret ke kanvas.

2. Setelah lapisan dimuat, Anda dapat melihat masing-masing titik yang mewakili insiden lokasi pembajakan. Ada ribuan insiden dan sulit ditentukan dengan lebih banyak pembajakan. Daripada poin individual, cara yang lebih baik untuk memvisualisasikan data ini adalah melalui peta panas. Pilih layer ASAM_events dan klik tombol Open the layer Styling Panel di panel Layers. Klik tarik-turun Simbol tunggal.

3. Di drop-down pemilihan perender, pilih Perender peta panas. Selanjutnya, pilih jalur warna Viridis dari pemilih Jalur warna.

4. Sesuaikan nilai Radius ke 5.0. Di bagian bawah, luaskan bagian Layer Rendering dan sesuaikan Opacity menjadi 75,0%. Ini memberikan efek visual yang bagus dari hotspot dengan lapisan tanah di bawahnya.

5. Sekarang mari kita animasikan data ini untuk menunjukkan peta insiden pembajakan tahunan. Klik kanan pada layer ASAM_event, dan pilih Properties.

6. Di kotak dialog Properti lapisan, pilih tab Temporal dan aktifkan dengan mengklik kotak centang..

7. Data sumber berisi atribut dateofocc - mewakili tanggal terjadinya insiden. Ini adalah bidang yang akan digunakan untuk menentukan poin yang diberikan untuk setiap periode waktu. Pilih Bidang Tunggal dengan Data/Waktu di menu Tarik-turun Konfigurasi, dateofocc sebagai Bidang.

8. Sekarang simbol jam akan muncul di sebelah nama layer. Klik pada Panel Kontrol Temporal (ikon Jam) dari Bilah Alat Navigasi Peta.

9. Klik pada Animated Temporal Navigation (ikon putar) untuk mengaktifkan kontrol animasi. Klik Atur ke Rentang Penuh (ikon segarkan) di sebelah Rentang untuk secara otomatis mengatur rentang waktu agar cocok dengan kumpulan data.

10. Sekarang Anda siap untuk melihat animasi. Tetapkan Langkah sebagai 1 Tahun lalu klik tombol Putar untuk memulai animasi.

Catatan : Jika animasi terlalu cepat, Anda dapat menyesuaikan frame rate dengan mengklik Temporal Setting (ikon gerigi kuning) di pojok kanan atas panel Temporal Controller. Menurunkan frame rate (frame per detik) akan memperlambat animasi.

11. Akan sangat membantu juga untuk menampilkan label yang menunjukkan kerangka waktu saat ini di peta. Kita dapat melakukannya dengan menggunakan dekorasi Judul bawaan. Pergi ke Lihat ‣ Dekorasi ‣ Label Judul.

12. Klik kotak centang untuk mengaktifkannya dan klik tombol Sisipkan Ekspresi dan masukkan ekspresi berikut untuk menampilkan tahun. Di sini variabel @map_start_time berisi stempel waktu potongan waktu saat ini yang ditampilkan. Jadi kita bisa menggunakan stempel waktu itu dan memformatnya untuk menampilkan tahun kejadian. Lihat Dokumentasi QGIS untuk detail tentang berbagai opsi pemformatan yang didukung untuk stempel waktu.

format_date(@map_start_time, 'yyyy')

13. Pilih ukuran font sebagai 25, atur warna bilah latar belakang sebagai Putih dan atur transparansi menjadi 50%. Di Penempatan pilih Kanan Bawah. Sekarang klik Oke.

14. Setelah parameter diatur sesuai, tahun akan ditampilkan seperti yang ditunjukkan. Untuk mengekspor ini sebagai gambar dan mengonversinya sebagai GIF pilih Ekspor Animasi (simpan ikon) di jendela kontrol Temporal.

15. Klik pada ... Direktori keluaran untuk memilih direktori tempat gambar akan disimpan.

16. Di bawah Extent pilih Hitung dari Layer ‣ ne_10_land layer. Klik Simpan.

17. Setelah ekspor selesai, Anda akan melihat gambar PNG untuk setiap tahun (total 18 gambar) di direktori keluaran.

18. Sekarang mari buat GIF animasi dari gambar-gambar ini. Ada banyak opsi untuk membuat animasi dari masing-masing bingkai gambar. Saya suka ezgif untuk alat yang mudah dan online. Kunjungi situs dan klik Pilih File dan pilih semua file .png. Setelah dipilih, klik Unggah dan buat GIF! tombol. Setelah dibuat, Anda dapat mengunduh GIF menggunakan tombol Simpan
