# Day 3 - Data, Tipe Data, dan Struktur Dasar untuk ML

## 🎯 Tujuan
Memahami apa itu data, bentuk-bentuk data di Python, dan kenapa ini krusial di Machine Learning.

## Materi / Pembahasan

### 1️⃣ Apa itu “Data” di Machine Learning?

Dalam ML:
```Data = representasi dunia nyata dalam bentuk angka / simbol```

Contoh dunia nyata:
- Tinggi badan
- Nilai ujian
- Harga rumah
- Warna baju
- Teks ulasan

Semua itu harus diubah menjadi data sebelum bisa dipelajari oleh mesin.

📌 ``` ML tidak belajar dari “makna”, tapi dari pola dalam data ```

### 2️⃣ Tipe Data Dasar di Python (yang Sering Dipakai di ML)

🔹 a. Integer (int)

Bilangan bulat
Contoh:
- Jumlah data
- Umur
- Banyak kelas
Contoh:
``` python
age = 20
epochs = 100
```
📌 Di ML: sering dipakai untuk parameter & indeks

🔹 b. Float (float)

Bilangan desimal
Contoh:
- Berat badan
- Loss
- Akurasi
``` python
weight = 55.5
accuracy = 0.87
```
📌 Hampir semua perhitungan ML pakai float

🔹 c. String (str)

Teks / label
``` python
label = "spam"
name = "Fathir"
```
📌 ML tidak bisa langsung memproses string
➡️ Nanti akan diubah jadi angka (encoding)

🔹 d. Boolean (bool)

Benar / Salah
``` python
is_train = True
is_empty = False
```
📌 Dipakai untuk kondisi, filter, dan logika

### 3️⃣ Struktur Data Penting untuk ML

🔸 a. List

Kumpulan data berurutan
``` python
scores = [80, 85, 90]
```
📌 Dalam ML:
- Menyimpan dataset sederhana
- Batch data

🔸 b. Tuple

Mirip list tapi immutable
``` python
shape = (100, 3)
```
📌 Sangat sering dipakai untuk: Bentuk data (rows, columns)

🔸 c. Dictionary

Pasangan key–value
``` python
student = {
    "name": "Fathir",
    "score": 90
}
```
📌 Dipakai untuk:
- Konfigurasi
- Metadata model

4️⃣ Kenapa mutable vs immutable itu penting di ML?

Contoh:
- List → mutable → bisa berubah saat training
- Tuple → immutable → aman untuk menyimpan shape
- Float → immutable → update loss = buat objek baru

👉 Ini menjelaskan:
Kenapa training ML sering “mengubah” nilai tapi sebenarnya membuat nilai baru

## Evaluasi
1. Kenapa ML lebih sering pakai float dibanding int?
2. Menurutmu, kenapa shape data lebih cocok pakai tuple?
3. Apakah string bisa langsung dipakai oleh model ML? Kenapa?