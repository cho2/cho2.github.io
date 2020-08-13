---
layout: post
title: "Menurunkan Versi Flatpak"
description: "Menurunkan Versi Flatpak"
comments: false
keywords: "Flatpak"
---

* Pertanyaan: Bisa tidak ya aplikasi flatpak mau diturunkan versinya?
* Jawaban: Bisa

Begitulah kira-kira pertanyaan yang pernah masuk, hari ini pertanyaan itu masuk lagi. Mari kita bedah. 
Studi kasusnya begini, Inkscape terkini adalah versi 1.0, lalu kita ingin mundur ke versi 0.92.x.

Jalankan perintah berikut untuk melihat komit yang diinginkan, dalam hal ini 0.92.x

```
flatpak remote-info --log flathub org.inkscape.Inkscape
```

Hasilnya akan tampil seperti berikut

```
Inkscape - Penyunting Grafik Vektor

        ID: org.inkscape.Inkscape
       Ref: app/org.inkscape.Inkscape/x86_64/stable
Arsitektur: x86_64
    Cabang: stable
     Versi: 1.0
   Lisensi: GPL-2.0-or-later
   Koleksi: org.flathub.Stable
     Unduh: 73,9 MB
 Terpasang: 231,9 MB
   Runtime: org.gnome.Platform/x86_64/3.36

       Sdk: org.gnome.Sdk/x86_64/3.36
     Komit: e60b4b9cc77bd6be468b80dfbf700dd4dcf6519389533d35dbbdbbc87c829e67
     Induk: 90ed46765f25f7ca2427dbe3f46ba34646d84520f056a9719521a593c21bfda9
    Subjek: Issue #11 - Make ICC profiles availble. (130edb6a)
   Tanggal: 2020-06-24 22:00:07 +0000
   Riwayat: 

     Komit: 90ed46765f25f7ca2427dbe3f46ba34646d84520f056a9719521a593c21bfda9
    Subjek: Rename boost to boost-headers (6a046c85)
   Tanggal: 2020-05-07 04:33:30 +0000

     Komit: b38c93598ab25cf3a0d79311e0880cc5ef6b15f1e6254fb28c979e0ee426c137
    Subjek: Update URL of tarball. sha256 unchanged (ec1522a7)
   Tanggal: 2020-05-05 07:35:51 +0000

     Komit: cab57e19c385bbea40f59ece27e0107a904421e59be0e265a25bba8aabef548e
    Subjek: Issue #50 - Update Inkscape to 0.92.5 (9a3b86dc)
   Tanggal: 2020-04-18 11:01:24 +0000

     Komit: 1e3818e3854fef97387e9791daa67285029d2dd554d5a3bfa169cea4ef96e0d1
    Subjek: GNOME runtime 3.36 (2dedac42)
   Tanggal: 2020-04-07 22:18:05 +0000

     Komit: 351ad9649e37ddb2e9fb2cd13d63038f243838c003e64bce972ca687abb5f353
    Subjek: Issue #37, Issue #38 - Update and add stable package dependencies (CDR, WPG, Visio) (#40) (09370ef9)
   Tanggal: 2019-09-24 07:55:58 +0000

     Komit: 8b2330c5e85a60006a53eb8edd7b0b7f494ab63fa49cbfd0ff0749c23c284e66
    Subjek: Fix #30: apply upstream patch (#31) (242d293c)
   Tanggal: 2019-02-13 10:30:42 +0000

     Komit: c1d9c90a180ced9dce0d99f27feb8e0d545ac3d9b96c915fe5b7234ce9cb0e37
    Subjek: Update to 0.92.4 (#28) (8fb7e5d2)
   Tanggal: 2019-01-18 09:02:09 +0000

     Komit: 9e047b89712601d3633db288c46fe067dbfc499930ef20c70d5ce7eb7c2dbf2d
    Subjek: Update platform to GNOME 3.30, dependencies (#25) (d80fce3c)
   Tanggal: 2019-01-10 12:23:42 +0000

     Komit: 309f33a9b30c457ede238564020cbb0ff4bfa94263dcf9bff72ce0560fe8b940
    Subjek: Update ghostscript to 9.26 (#20) (4d9be1cd)
   Tanggal: 2018-11-21 22:10:38 +0000

     Komit: 87403c2e431dcafe45efea469d33e38b532c2e46702cc9802749c10ec300ef9d
    Subjek: Update ghostscript to 9.25 (#18) (89cd58f2)
   Tanggal: 2018-09-18 12:53:40 +0000

```

Versi Inkscape 1.0 yang tersedia di Flatpak berarti `0.92.5` dengan komit `cab57e19c385bbea40f59ece27e0107a904421e59be0e265a25bba8aabef548e`.

Langkah selanjutnya adalah deploy komit tersebut agar kita bisa menurunkan versi Inkscape ke `0.92.5`, Jalankan perintah berikut
```
flatpak update \
    --commit=cab57e19c385bbea40f59ece27e0107a904421e59be0e265a25bba8aabef548e \
    org.inkscape.Inkscape
```

Setelah selesai, cobalah membuka Inkscape, apakah versinya sudah mundur ke `0.92.5` atau belum. Bisa juga dicek dengan perintah

```
flatpak info org.inkscape.Inkscape
```
Hasilnya akan seperti berikut
```
Inkscape - Penyunting Grafik Vektor

        ID: org.inkscape.Inkscape
       Ref: app/org.inkscape.Inkscape/x86_64/stable
Arsitektur: x86_64
    Cabang: stable
     Versi: 0.92.5
   Lisensi: GPL-2.0+
      Asal: flathub
   Koleksi: org.flathub.Stable
Pemasangan: system
 Terpasang: 246,7 MB
   Runtime: org.gnome.Platform/x86_64/3.36
       Sdk: org.gnome.Sdk/x86_64/3.36

     Komit: cab57e19c385bbea40f59ece27e0107a904421e59be0e265a25bba8aabef548e
     Induk: 1e3818e3854fef97387e9791daa67285029d2dd554d5a3bfa169cea4ef96e0d1
    Subjek: Issue #50 - Update Inkscape to 0.92.5 (9a3b86dc)
   Tanggal: 2020-04-18 11:01:24 +0000
```
Untuk mengembalikan ke versi terkini, cukup jalankan
```
flatpak update org.inkscape.Inkscape
```

Mudah bukan? Jika Anda familiar dengan `git` apakah teringat dengan sesuatu?