---
layout: post
title: "Mencoba Endless OS 3.4 Beta"
description: "Mencoba Endless OS 3.4 Beta"
comments: false
keywords: "Endless OS"
---

Sebentar lagi Endless OS 3.4 rilis. Endless OS 3.4 beta sudah bisa dicoba. Berikut langkah-langkahnya.
* Pastikan Anda sudah memperbarui Endless OS ke versi 3.3.18. Apabila belum, buka Pengaturan > Rincian > tekan "Periksa Pembaruan Sekarang Juga" pada pojok kanan bawah.
*  Buka Terminal, ketik `sudo eos-updater-ctl update`, lalu nyalakan ulang.
*  Setelah dinyalakan ulang, buka terminal kembali, jalankan `sudo eos-stage-ostree demo`, kemudian nyalakan ulang.
* Setelah itu, Anda sudah berada dalam mode beta.
* Untuk mengembalikan dari mode beta ke model stabil, buka terminal, jalankan `sudo eos-stage-ostree prod`.

Bila cara diatas belum berhasil, cobalah cara berikut:
* Buka terminal, jalankan `sudo eos-stage-ostree demo`, kemudian nyalakan ulang.
* Buka Pengaturan > Rincian > tekan “Periksa Pembaruan Sekarang Juga” pada pojok kanan bawah. Tunggu hingga pembaruan selesai dan nyalakan ulang.
* Sekarang seharusnya versi Endless OS sudah mencapai 3.3.18. Kemudian buka lagi Pengaturan > Rincian > tekan “Periksa Pembaruan Sekarang Juga” pada pojok kanan bawah. Tunggu hingga pembaruan selesai dan nyalakan ulang.