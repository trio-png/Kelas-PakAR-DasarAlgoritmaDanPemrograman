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
