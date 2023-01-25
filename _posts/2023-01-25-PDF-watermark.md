---
layout: post
title: "Memberi Tanda Air Pada Berkas PDF"
description: "Memberi Tanda Air Pada Berkas PDF"
comments: false
keywords: "pdftk, LibreOffice"
---

Karena ada kebutuhan untuk memberi tanda air (*watermark*) di berkas pdf tanpa dari Libreoffice, jadi cari-cari sana-sini. Ketemu caranya di tautan [ini](https://www.togaware.com/linux/survivor/pdf-watermarks.html). Perkakas yang dibutuhkan adalah `pdftk` dan `LibreOffice`. `pdftk` digunakan untuk memberi tanda air (*watermark*) pada berkas pdf yang sudah ada, sementara `LibreOffice` digunakan untuk membuat berkas pdf berisi tanda air (*watermark*). Pastikan keduanya sudah terpasang ya. Selain itu, siapkan juga berkas pdf yang akan diberi tanda air (*watermark*). Kenapa tidak membubuhkan tanda air (*watermark*) di LibreOffice lalu menyimpannya dalam format pdf? Jawabannya karena bukan saya yang membuat berkas pdf tersebut, jadi saya hanya menerima berkas pdf tersebut dan ada kebutuhan untuk memberi tanda air (*watermark*).

Pertama-tama, kita akan membuat berkas berisi tanda air (*watermark*). Buka LibreOffice Writer, lalu klik menu Format > Watermark.
Anda dapat mengatur teks yang akan muncul, jenis fonta, sudut kemiringan, tingkat transparansi, dan warna tanda air (*watermark*).

![https://gitlab.com/cho2/blog-images/-/raw/master/2023-01-25/LO-watermark-1.png](https://gitlab.com/cho2/blog-images/-/raw/master/2023-01-25/LO-watermark-1.png)

![https://gitlab.com/cho2/blog-images/-/raw/master/2023-01-25/LO-watermark-2.png](https://gitlab.com/cho2/blog-images/-/raw/master/2023-01-25/LO-watermark-2.png)

Setelah selesai, ekspor berkas tersebut ke pdf. Beri nama misalnya `berkas-tanda-air.pdf`.

![https://gitlab.com/cho2/blog-images/-/raw/master/2023-01-25/evince-watermark.png](https://gitlab.com/cho2/blog-images/-/raw/master/2023-01-25/evince-watermark.png)

Kemudian, siapkan berkas pdf yang akan diberi tanda air (*watermark*). Beri nama misalnya `berkas-asal.pdf`. Jalankan perintah berikut untuk membubuhkan tanda air (*watermark*) pada berkas pdf yang sudah disiapkan.

```
pdftk berkas-asal.pdf background berkas-tanda-air.pdf output berkas-jadi.pdf
```
Keterangan:
* `berkas-asal.pdf` : Berkas pdf yang akan dibubuhkan tanda air (*watermark*)
* `background` : Membuat tanda air (*watermark*) menjadi latar belakang
* `berkas-tanda-air.pdf` : Berkas yang berisi gambar tanda air (*watermark*)
* `berkas-jadi.pdf` : Berkas pdf yang sudah dibubuhkan tanda air (*watermark*)

Hasilnya kira-kira seperti berikut.

![https://gitlab.com/cho2/blog-images/-/raw/master/2023-01-25/evince-output.png](https://gitlab.com/cho2/blog-images/-/raw/master/2023-01-25/evince-output.png)

Selamat mencoba!