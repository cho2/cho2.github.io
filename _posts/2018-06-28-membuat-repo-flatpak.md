---
layout: post
title: "Membuat Repo Flatpak"
description: "Membuat Repo Flatpak"
comments: false
keywords: "Flatpak"
---

> Referensi utama ada di https://blogs.gnome.org/alexl/2017/02/10/maintaining-a-flatpak-repository/. Silakan pelajari dengan baik

## Hello World
Buat aplikasi kecil Hello World kemudian buat reponya. Saya coba dengan langkah-langkah berikut dengan mengikuti tautan diatas.

```
# helloworld dan perintilannya

$ echo $'#!/bin/sh\necho hello world' > hello.sh
$ flatpak build-init appdir com.example.App \
          org.freedesktop.Sdk \
          org.freedesktop.Platform 1.6
$ flatpak build appdir mkdir /app/bin
$ flatpak build appdir install --mode=750 hello.sh /app/bin
$ flatpak build-finish --command=hello.sh appdir

# bangun repo di lokal
$ flatpak build-export repo appdir stable
```

Kemudian salin folder `repo` ke webserver, dalam contoh ini saya menggunakan GitHub pages, yaitu di https://github.com/cho2/repo.cho2.github.io. Karena GitHub pages saya sudah tertaut dengan domain https://blog.kukuh.syafaat.id maka alamat repo saya menjadi https://blog.kukuh.syafaat.id/repo.cho2.github.io/repo/.

```
# tambahkan remote
$ flatpak remote-add --no-gpg-verify cho2 https://blog.kukuh.syafaat.id/repo.cho2.github.io/repo/

# pasang aplikasinya
$ sudo flatpak install cho2 com.example.App

# jalankan aplikasinya
$ flatpak run com.example.App
```

Apabila keluaran di terminal Anda adalah `hello world`, maka berhasil.

## Firefox
Pada postingan [ini](https://blog.kukuh.syafaat.id/2017/Firefox-Quantum-Flatpak/), saya sudah pernah membangun peramban Mozilla Firefox versi Flatpak. Bagaimana kalau kita buatkan reponya.

```
# clone kode sumber Firefox Flatpak
$ git clone https://github.com/cho2/org.mozilla.Firefox.git

# bangun dengan Flatpak builder
$ flatpak-builder --repo=repo firefox org.mozilla.Firefox.json

# bangun repo
$ flatpak build-export repo firefox
```
Hampir sama dengan hello world diatas, salin folder repo ke webserver, saya kembali menggunakan GitHub pages di https://github.com/cho2/firefox-flatpak-repo dengan alamat repo https://blog.kukuh.syafaat.id/firefox-flatpak-repo/repo.


```
# tambahkan remote
$ flatpak remote-add --no-gpg-verify firefox https://blog.kukuh.syafaat.id/firefox-flatpak-repo/repo/

# pasang aplikasinya
$ sudo flatpak install firefox org.mozilla.Firefox

# jalankan aplikasinya
$ flatpak run org.mozilla.Firefox
```

Catatan: Pada saat memasang aplikasi menggunakan `sudo` karena `--no-gpg-verify`

### TODO
* GPG signatures
* Flatpakref files
* CI