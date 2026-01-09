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

