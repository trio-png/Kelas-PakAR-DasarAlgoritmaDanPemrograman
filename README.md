# Aplikasi Inventori Sederhana

Aplikasi berbasis CLI (Command Line Interface) untuk mengelola inventori produk menggunakan Python dan SQLite.

## Fitur Utama
✅ Tambah produk baru  
✅ Lihat daftar produk  
✅ Edit produk yang ada  
✅ Hapus produk  
✅ Penyimpanan data persisten dengan SQLite  


## Struktur Kode

### 1. Import Library
```python
import sqlite3
from tabulate import tabulate
untuk menyimpan database 

### 2. Kelas InventoryApp
Kelas utama yang mengelola seluruh operasi aplikasi.

Method __init__
def __init__(self):
    self.conn = sqlite3.connect('inventory.db')
    self.c = self.conn.cursor()
    self.create_table()
metode ini digunakan di aplikasi kasir untuk menginisialisasi objek atau kelas kasir saat pertama kali dibuat. 
Fungsi ini mengambil semua item dari tabel inventory dan menampilkannya dalam format tabel menggunakan tabulate. Jika tidak ada item, akan ditampilkan pesan bahwa inventori kosong.
     self.c.execute("SELECT * FROM inventory")
     print(tabulate(items, headers=headers, tablefmt="grid"))
     edit_item:

print(f"\nMengedit produk: {item[1]}")
        print("Kosongkan field jika tidak ingin mengubahnya")

        name = input(f"Nama Produk [{item[1]}]: ")
        category = input(f"Kategori [{item[2]}]: ")
        quantity = input(f"Jumlah [{item[3]}]: ")
        price = input(f"Harga [{item[4]}]: ")
Fungsi ini memungkinkan pengguna untuk mengedit detail produk yang sudah ada. Pengguna diminta untuk memasukkan ID produk yang ingin diedit, dan kemudian dapat mengubah detailnya. Hanya field yang diisi yang akan diperbarui.
item_id = input("\nMasukkan ID produk yang ingin diedit: ")

Fungsi run
Fungsi ini menjalankan aplikasi utama. Ini menampilkan menu kepada pengguna dan meminta mereka untuk memilih tindakan (lihat, tambah, edit, hapus, atau keluar). Berdasarkan pilihan pengguna, fungsi yang sesuai akan dipanggil.
     while True:
         choice = input("Pilih menu: ")
     Menjalankan Aplikasi

Bagian terakhir dari kode memeriksa apakah skrip dijalankan sebagai program utama. Jika ya, objek InventoryApp dibuat dan fungsi run dipanggil untuk memulai aplikasi.
     if __name__ == "__main__":
         app = InventoryApp()
         app.run()
     



# User Manual Aplikasi Inventory untuk Beans Coffee 
Persiapan Awal
Buka Google Colab
Klik "New Notebook" untuk membuat notebook baru
Ganti nama notebook menjadi "Inventory Management System"

Langkah 1: Instalasi Package
Di cell pertama, jalankan kode ini untuk menginstal tabulate:

python
Run
Copy code
!pip install tabulate

Langkah 2: Upload File database ke Colab
Buat cell baru dan jalankan:

python
2 lines
from google.colab import files
uploaded = files.upload()
Klik tombol "Choose Files" dan pilih file database Anda (atau biarkan kosong untuk membuat baru).

Langkah 3: Salin Kode Aplikasi
Buat cell baru dan salin seluruh kode aplikasi:

python
20 lines
import sqlite3
from tabulate import tabulate


Langkah 4: Menjalankan Aplikasi
Buat cell baru dan jalankan:

python
Copy code
app.run()  # Untuk memulai aplikasi

Fitur Khusus Google Colab
Menyimpan Database
Untuk mendownload database dari Colab:

python
from google.colab import files
files.download('/content/inventory.db')
Reset Database
Jika ingin menghapus dan mulai dari awal:

python
!rm /content/inventory.db
3. Backup Otomatis
Tambahkan di akhir kode:

python
import time
def backup_db():
Troubleshooting
Masalah: Tidak bisa input data Solusi:

Pastikan menjalankan cell input secara berurutan
Di Colab, Anda mungkin perlu mengklik kotak input yang muncul di bawah cell
Masalah: Database hilang setelah menutup Colab Solusi:

Selalu download database setelah melakukan perubahan
Atau simpan di Google Drive dengan kode:
python
from google.colab import drive
drive.mount('/content/drive')

Catatan Penting
Google Colab akan menghapus file lokal saat runtime di-reset
Untuk penggunaan jangka panjang, simpan database di Google Drive
Output tabel akan ditampilkan lebih rapi di Colab dibanding terminal biasa
