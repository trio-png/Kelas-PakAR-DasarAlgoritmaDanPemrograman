Pengujian dan Evaluasi Aplikasi Inventori
1. Test Suite yang Komprehensif
Untuk memastikan aplikasi inventori berfungsi dengan baik, kami akan melakukan pengujian pada setiap fitur utama. Pengujian ini mencakup:

1.1. Pengujian Fitur Tambah Produk
Tujuan: Memastikan produk baru dapat ditambahkan ke inventori.
Langkah:
Jalankan aplikasi.
Pilih opsi 2 untuk menambah produk.
Masukkan nama, kategori, jumlah, dan harga produk.
Verifikasi bahwa produk ditambahkan dengan benar dengan memilih opsi 1 untuk melihat daftar produk.
1.2. Pengujian Fitur Lihat Produk
Tujuan: Memastikan semua produk ditampilkan dengan benar.
Langkah:
Jalankan aplikasi.
Pilih opsi 1 untuk melihat daftar produk.
Verifikasi bahwa semua produk yang ditambahkan sebelumnya muncul dalam tabel.
1.3. Pengujian Fitur Edit Produk
Tujuan: Memastikan produk yang ada dapat diedit.
Langkah:
Jalankan aplikasi.
Pilih opsi 3 untuk mengedit produk.
Masukkan ID produk yang ingin diedit.
Ubah beberapa field (misalnya, nama dan harga).
Verifikasi bahwa perubahan disimpan dengan memilih opsi 1 untuk melihat daftar produk.
1.4. Pengujian Fitur Hapus Produk
Tujuan: Memastikan produk dapat dihapus dari inventori.
Langkah:
Jalankan aplikasi.
Pilih opsi 4 untuk menghapus produk.
Masukkan ID produk yang ingin dihapus.
Konfirmasi penghapusan.
Verifikasi bahwa produk tidak lagi muncul dalam daftar dengan memilih opsi 1.
1.5. Pengujian Input Tidak Valid
Tujuan: Memastikan aplikasi menangani input tidak valid dengan baik.
Langkah:
Jalankan aplikasi.
Pilih opsi 3 untuk mengedit produk.
Masukkan ID produk yang tidak ada.
Verifikasi bahwa aplikasi memberikan pesan kesalahan yang sesuai

3. Analisis Kinerja dan Optimisasi
3.1. Analisis Kinerja
Waktu Respons: Aplikasi merespons dengan cepat untuk semua operasi CRUD, dengan waktu respons kurang dari 1 detik untuk setiap permintaan.
Penggunaan Memori: Aplikasi menggunakan memori yang efisien, dengan penggunaan memori yang minimal saat menjalankan operasi.
3.2. Optimisasi
Penggunaan Parameterized Queries: Menggunakan parameterized queries untuk mencegah SQL injection dan meningkatkan keamanan.
Batch Processing: Untuk aplikasi yang lebih besar, pertimbangkan untuk menggunakan batch processing saat menambah atau mengedit banyak produk sekaligus.
Indeksasi: Jika jumlah produk meningkat, pertimbangkan untuk menambahkan indeks pada kolom yang sering dicari (misalnya, nama produk) untuk meningkatkan kecepatan pencarian.
