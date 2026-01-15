# Day 05 – Aljabar Linear Praktis untuk Machine Learning

## 🎯 Tujuan

- Memahami data sebagai **objek aljabar linear**, bukan sekadar kumpulan angka
- Mengerti perbedaan makna **1D, 2D, dan nD array** dalam konteks Machine Learning
- Memahami **vektor dan matriks** sebagai representasi dataset
- Mengenal konsep **feature matrix (X)** dan **label vector (y)**
- Mengubah cara pandang: dari tabel visual menjadi **struktur matematis**

---

## 🧭 Posisi Day 5 dalam ML Journey

Jika Day 4 mengubah *alat berpikir* dari Python list ke NumPy array,  
maka Day 5 mengubah *bahasa berpikir* dari logika pemrograman ke **aljabar linear**.

Day 5 adalah tahap di mana:

> *Data tidak lagi diperlakukan sebagai elemen individual,  
> tetapi sebagai vektor dan matriks yang memiliki makna matematis.*

Tanpa pemahaman ini, Machine Learning akan terasa seperti *magic box*  
karena model bekerja pada struktur aljabar, bukan pada cerita data.

---

## 📐 Dimensi Data: 1D, 2D, dan Maknanya

### 1D Array (Vektor)

Contoh:
```python
y = [50, 60, 70, 80]
```

Makna:

* Merepresentasikan vektor
* Biasanya digunakan sebagai label / target
* Bentuk matematis: (n,)

Dalam ML, vektor sering digunakan untuk:

* Label
* Bobot (weights)
* Satu fitur tunggal

### 2D Array (Matriks)

Contoh: 

```python
X = [
  [2, 5],
  [3, 6],
  [4, 7]
]
```

Makna:

* Merepresentasikan matriks
* Setiap baris = satu data (sample)
* Setiap kolom = satu fitur (feature)
* Bentuk matematis: (n_samples, n_features)

Dalam ML:

```Dataset hampir selalu direpresentasikan sebagai matriks.```

## 🧠 Insight Penting tentang Shape

```Dalam Machine Learning, bentuk (shape) data sering lebih penting daripada nilainya.```

Kesalahan umum pemula:

* Nilai data masuk akal
* Tidak ada error sintaks
* Tetapi shape data salah

Akibatnya:

* Model error
* Atau lebih berbahaya: model jalan tapi hasil tidak bermakna

## ➡️ Vektor vs Matriks

| Konsep  | Makna dalam ML                    |
| ------- | --------------------------------- |
| Vektor  | Satu dimensi data (label / bobot) |
| Matriks | Dataset                           |
| Baris   | Satu sampel data                  |
| Kolom   | Satu fitur                        |

Machine Learning tidak memahami konteks manusia.
Ia hanya bekerja pada relasi matematis antar vektor dan matriks.

## 📊 Dataset sebagai Objek Matematis

Dalam supervised learning, dataset selalu dapat direduksi menjadi:
```
X → feature matrix
y → label vector
```
Contoh:

* X: jam belajar, jumlah latihan
* y: nilai ujian

Secara matematis:
```
X ∈ R^(n × m)
y ∈ R^n
```
Ini berarti:

* ML bekerja di ruang vektor
* Dataset adalah titik-titik dalam ruang berdimensi m

## 🔄 Operasi Aljabar Linear Dasar dalam ML

Operasi yang hampir selalu muncul:

* Transpose
* Dot product
* Penjumlahan vektor
* Rata-rata (mean) per axis

Makna filosofisnya:

```Model Machine Learning pada dasarnya adalah rangkaian transformasi linear terhadap data.```

## 🔁 Axis

Axis menentukan sudut pandang perhitungan.

* axis = 0 → operasi per kolom (fitur)
* axis = 1 → operasi per baris (data)

Kesalahan memahami axis:

* Menghasilkan interpretasi statistik yang salah
* Mengacaukan proses training model

Axis bukan detail teknis kecil,
melainkan bagian dari cara berpikir matematis.

## 🧩 Perubahan Cara Berpikir

Cara Lama (Imperative Thinking)

* Fokus pada loop
* Fokus pada elemen per elemen
* Programmer mengontrol langkah perhitungan

Cara Baru (Linear Algebra Thinking)

* Fokus pada bentuk (shape)
* Fokus pada transformasi
* Library menangani detail perhitungan

Dalam Machine Learning, saya tidak mengontrol setiap langkah,
saya mendefinisikan struktur dan relasi data.

## ✍️ Refleksi Pribadi

* Dataset ternyata lebih dekat ke matriks daripada tabel visual
* Banyak kesalahan ML berasal dari salah memahami bentuk data
* NumPy dan aljabar linear memaksa saya berpikir lebih disiplin
* ML terasa lebih matematis daripada sekadar pemrograman

## ⏭️ Arah Day 6

* Linear Regression sebagai transformasi linear
* Dot product sebagai inti prediksi
* Model sebagai fungsi matematis, bukan sekadar API library

Day 5 adalah bahasa.
Day 6 adalah mulai berbicara Machine Learning.

## 📌 Catatan Akhir:
Jika saya belum nyaman membaca shape dan operasi matriks,
maka saya belum siap memahami cara kerja model Machine Learning.