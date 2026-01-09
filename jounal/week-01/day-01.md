# Day 01 - How Python Executes Code

## Topik
- Cara Python mengeksekusi sebuah program
- Penggunaan `import` pada bahasa Python

## Materi / Pembahasan

### 1. Eksekusi Program di Python

Python mengeksekusi kode **secara berurutan dari atas ke bawah**.
Artinya, setiap baris kode akan dijalankan satu per satu sesuai urutan penulisannya.

Python **tidak membaca keseluruhan file terlebih dahulu untuk memahami variabel**,
melainkan hanya mengetahui apa yang sudah dieksekusi sampai baris tertentu.
Inilah yang disebut sebagai **state program**.

Contoh:
```python
print(a)
a = 10
```
Kode di atas akan menghasilkan error karena pada saat print(a) dieksekusi,
Python belum pernah mengenal variabel a.

Hal ini menjelaskan mengapa:

- Variabel harus didefinisikan sebelum digunakan
- Urutan penulisan kode sangat berpengaruh terhadap jalannya program

### 2. State Program dan Variabel

State program adalah kondisi program pada suatu titik eksekusi tertentu.
State ini mencakup:

- Variabel yang sudah didefinisikan
- Nilai variabel tersebut
- Module yang sudah di-import

Ketika Python menemukan baris:
```python
a = 10
```
Python akan:

- Membuat objek bernilai 10
- Mengaitkan nama a ke objek tersebut

Jika kemudian baris berikutnya:
```python
a = 20
```
Maka Python tidak mengubah objek lama, melainkan:

- Membuat objek baru bernilai 20
- Mengaitkan kembali nama a ke objek baru tersebut

### 3. Contoh Assignment dan Dampaknya
Perhatikan contoh berikut:
``` python
a = 10
b = a
a = 20
print(b)
```
Output:
``` 10 ```
Hal ini terjadi karena:

- ```b``` mengambil referensi ke objek yang sama dengan ```a``` pada saat bernilai ```10```
- Ketika ```a``` diubah menjadi ```20```, ```a``` diarahkan ke objek baru
- ```b``` tetap mengarah ke objek lama

Contoh ini menunjukkan bahwa assignment di Python bukan menyalin nilai,
melainkan mengaitkan nama ke object.

### 4. Perbandingan Singkat dengan C++

Walaupun hasil program Python dan C++ bisa sama,
cara kerjanya berbeda.

Di C++:

- Assignment berarti menyalin nilai ke lokasi memori baru
- Perubahan pada satu variabel tidak memengaruhi variabel lain

Sedangkan di Python:

- Variabel bersifat reference ke object
- Perubahan binding nama bisa menghasilkan perilaku berbeda

Pemahaman ini penting untuk materi lanjutan seperti:

- NumPy
- Tensor
- Machine Learning pipeline

### 5. Cara Kerja ```import``` di Python

Ketika Python menemukan perintah:
``` python
import module
```
Python akan:

1. Mencari module tersebut
2. Mengeksekusi seluruh isi module satu kali
3. Menyimpan hasil eksekusinya ke dalam memory

Jika module yang sama di-import kembali:

- Python tidak mengeksekusi ulang
- Python hanya menggunakan module yang sudah ada di state program

Inilah sebabnya:

- import bersifat efisien
- Module dapat menyimpan state
- Perubahan global di module bisa memengaruhi bagian lain dari program

### 6. Kesimpulan 

Python mengeksekusi program secara berurutan dan sangat bergantung pada state program.
Pemahaman tentang urutan eksekusi, variabel, dan import membantu
menghindari error serta membangun program yang lebih terstruktur.

Materi ini menjadi fondasi penting sebelum mempelajari
struktur data, NumPy, dan Machine Learning.

## Note
- Python menjalankan kode baris demi baris
- Variabel adalah **nama**, bukan kotak penyimpan nilai
- Assignment mengubah **binding nama ke object**
- `import` hanya dieksekusi satu kali per program
