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
