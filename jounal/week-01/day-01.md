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
