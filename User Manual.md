# User Manual Aplikasi Inventori

## Deskripsi
Aplikasi Inventori adalah program berbasis teks yang memungkinkan pengguna untuk mengelola produk dalam inventori. Pengguna dapat menambah, melihat, mengedit, dan menghapus item dari inventori.

## Prasyarat
- Python 3.x terinstal di sistem Anda.
- Modul `tabulate` harus diinstal. Anda dapat menginstalnya dengan perintah berikut:
  ```bash
  pip install tabulate

  Menjalankan Aplikasi
Simpan Kode: Salin kode aplikasi ke dalam file bernama inventory_app.py.
Jalankan Aplikasi: Buka terminal atau command prompt, navigasikan ke direktori tempat file disimpan, dan jalankan perintah berikut:

Antarmuka Pengguna
Setelah aplikasi dijalankan, Anda akan melihat menu utama dengan pilihan berikut:

=== APLIKASI INVENTORI ===
1. Lihat Daftar Produk
2. Tambah Produk
3. Edit Produk
4. Hapus Produk
0. Keluar

1. Fungsi Menu
1. Lihat Daftar Produk
Pilih opsi 1 untuk melihat semua produk yang ada dalam inventori.
Aplikasi akan menampilkan daftar produk dalam format tabel, termasuk ID, nama, kategori, jumlah, harga, dan waktu terakhir diperbarui.
2. Tambah Produk
Pilih opsi 2 untuk menambahkan produk baru.
Anda akan diminta untuk memasukkan informasi berikut:
Nama Produk: Nama dari produk yang ingin ditambahkan.
Kategori: Kategori produk.
Jumlah: Jumlah stok produk.
Harga: Harga per item produk.
Setelah semua informasi dimasukkan, produk akan ditambahkan ke inventori.
3. Edit Produk
Pilih opsi 3 untuk mengedit produk yang sudah ada.
Aplikasi akan menampilkan daftar produk. Masukkan ID produk yang ingin diedit.
Anda akan diminta untuk memasukkan informasi baru. Kosongkan field jika tidak ingin mengubahnya.
Setelah selesai, perubahan akan disimpan.
4. Hapus Produk
Pilih opsi 4 untuk menghapus produk dari inventori.
Aplikasi akan menampilkan daftar produk. Masukkan ID produk yang ingin dihapus.
Anda akan diminta untuk mengonfirmasi penghapusan. Ketik y untuk menghapus atau n untuk membatalkan.
0. Keluar
Pilih opsi 0 untuk keluar dari aplikasi. Aplikasi akan menutup dan koneksi ke database akan ditutup.

