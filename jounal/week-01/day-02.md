# Day 2 - Variable, Object, dan Memory Model di Python

## Topik
- Hubungan antara variable dan object di Python
- Konsep reference (binding nama ke object)
- Perbedaan assignment dan mutation
- Dasar memory model Python

## Materi / Pembahasan

### 1. Variable di Python Bukan Kotak Nilai

Di Python, **variable bukan tempat menyimpan nilai** seperti di beberapa bahasa lain.
Variable adalah **nama (label)** yang menunjuk ke sebuah **object** di memory.

Artinya:

- Variable tidak punya nilai sendiri
- Variable hanya menunjuk ke object tertentu

Contoh:
```python
a = 10
```
Yang terjadi:

- Python membuat object integer bernilai ```10```
- Nama ```a``` diarahkan (bind) ke object tersebut

### 2. Object dan Identitas (id)

Setiap object di Python memiliki identitas unik di memory.
Identitas ini bisa dilihat menggunakan fungsi ```id()```.

Contoh:
``` python
a = 10
b = 10

print(id(a))
print(id(b))
```
Pada kasus tertentu, ```a``` dan ```b``` bisa menunjuk ke object yang sama
karena Python melakukan object reuse (interning) untuk efisiensi.

Namun yang penting dipahami:
```Variable bisa menunjuk ke object yang sama atau berbeda, tergantung konteks.```

### 3. Assignment Bukan Menyalin Nilai

Perhatikan contoh berikut:
``` python
a = 10
b = a
a = 20

print(b)
```
Output: ```10```

Penjelasan:

- ```b = a``` membuat ```b``` menunjuk ke object yang sama dengan ```a```
- Saat ```a = 20```, Python membuat object baru bernilai ```20```
- Nama ```a``` diarahkan ke object baru
- ```b``` tetap menunjuk ke object lama (```10```)

Ini menunjukkan bahwa:

- Assignment tidak menyalin nilai
- Assignment hanya mengubah arah referensi nama

### 4. Immutable vs Mutable Object

Python membagi object menjadi dua kategori penting:

Immutable (tidak bisa diubah)
Contoh:

- ```int```
- ```float```
- ```str```
- ```tuple```

Jika nilainya berubah:

- Object lama ditinggalkan
- Object baru dibuat

Mutable (bisa diubah)

Contoh:

- ```list```
- ```dict```
- ```set```

Nilai object bisa berubah tanpa membuat object baru.
Contoh:
``` python
a = [1, 2, 3]
b = a

a.append(4)
print(b)
```
Output: ```[1, 2, 3, 4]```

Karena:

- ```a``` dan ```b``` menunjuk ke object list yang sama
- Perubahan object terlihat oleh semua reference

### 5. Assignment vs Mutation (Penting untuk ML)

Perbedaan krusial:

- Assignment → mengubah referensi nama
- Mutation → mengubah isi object

Ini sering menyebabkan bug di:

- NumPy
- Pandas
- Training loop ML
- Data preprocessing

Contoh bug umum:
``` python 
x_train = data
x_train.append(0)
```
Tanpa sadar:

- data ikut berubah
- Pipeline jadi tidak konsisten

### 6. Kaitan dengan Memory Model Python

Secara sederhana:

- Python menyimpan object di memory
- Variable hanyalah nama yang menunjuk ke object
- Satu object bisa punya banyak nama
- Satu nama bisa diarahkan ulang ke object lain

Pemahaman ini penting sebelum:

- Masuk NumPy array
- Tensor
- Model training
- Debugging error ML yang “aneh”

## Note

Hari ini fokus memahami cara berpikir Python, bukan menghafal syntax.
Konsep variable–object–memory ini akan terus muncul
di hampir semua tahap Machine Learning.