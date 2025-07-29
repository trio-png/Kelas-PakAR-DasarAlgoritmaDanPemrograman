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
     
