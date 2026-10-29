## Pertemuan 13 - Debugging dan Testing

Nama: Siti Solehah
NIM: 2225250058
Kelas: 3B

## Tujuan

Memahami debugging, tracing, testing, dan test case untuk menemukan serta memperbaiki bug pada program Python.

## Struktur Folder

- "kasus/" berisi program yang memiliki bug.
- "latihan/" berisi latihan tracing dan testing.
- "praktik/" berisi program Praktik 4 yang diperbaiki.
- "README.md" berisi penjelasan dan hasil praktik.

Cara Menjalankan

Jalankan perintah berikut di terminal VS Code:

python praktik/praktik_4_debugging.py

## Kasus

Program yang diuji adalah program pengolahan nilai mahasiswa. Program awal memiliki tiga bug, yaitu kesalahan dalam menghitung rata-rata, menentukan status kelulusan, dan mencari nilai tertinggi.

## Test Case

ID| Input| Expected Result
T1| "[80, 60, 90, 70]"| Rata-rata: 75.0
T2| "[100, 80]"| Rata-rata: 90.0
T3| "60"| Lulus
T4| "59"| Tidak lulus
T5| "[80, 60, 90, 70]"| Nilai tertinggi: 90

Bug Report

Bug 1: Perhitungan rata-rata

Penyebab: Program membagi jumlah nilai dengan angka tetap, yaitu 5.

Perbaikan: Pembagi diganti dengan "len(nilai)" agar sesuai dengan jumlah data.

Bug 2: Status kelulusan

Penyebab: Program menggunakan operator ">" sehingga nilai 60 dianggap tidak lulus.

Perbaikan: Operator diganti menjadi ">=" agar nilai 60 dinyatakan lulus.

Bug 3: Nilai tertinggi

Penyebab: Program menggunakan operator "<" sehingga proses pencarian nilai tertinggi menjadi salah.

Perbaikan: Operator diganti menjadi ">" dan nilai awal diambil dari data pertama.

## Retest

Setelah program diperbaiki, pengujian dilakukan kembali menggunakan test case yang telah dibuat.

## Hasil pengujian:

- T1: PASS
- T2: PASS
- T3: PASS
- T4: PASS
- T5: PASS

## Hasil Program

Rata-rata: 75.0
Status 60: Lulus
Tertinggi: 90

## Refleksi

Dari praktik ini, saya belajar bahwa program yang bisa dijalankan belum tentu menghasilkan jawaban yang benar. Oleh karena itu, program perlu diuji menggunakan beberapa test case agar bug dapat ditemukan dan diperbaiki dengan tepat.