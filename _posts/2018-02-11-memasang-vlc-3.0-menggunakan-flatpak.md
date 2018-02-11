---
layout: post
title: "Memasang VLC 3.0 Menggunakan Flatpak pada openSUSE"
description: "Memasang VLC 3.0 Menggunakan Flatpak pada openSUSE"
comments: false
keywords: "VLC, openSUSE, Flatpak"
---

[VLC 3.0](https://www.videolan.org/vlc/releases/3.0.0.html) baru saja dirilis. Lima fitur unggulannya antara lain:

* Dukungan chromecast
* VLC 3.0 merupakan rilis LTS (Long Term Support)
* Dukungan penjelajahan jaringan
* Dukungan adaptive streaming
* Sudah menggunakan openGL pada Linux untuk memutar video 4K dengan smooth

Berikut ini cara memasang VLC menggunakan [Flatpak](https://flatpak.org/)

* Pastikan Anda sudah memasang paket `flatpak`, jika belum silakan pasang, contoh pemasangan melalui terminal adalah dengan mengetikkan perintah
```
sudo zypper install flatpak
```

* Apabila paket flatpak sudah terpasang, langkah selanjutnya adalah memasang VLC dengan flatpak. Masih di terminal, ketikkan 
```
flatpak install --from https://flathub.org/repo/appstream/org.videolan.VLC.flatpakref
```

* Tunggu sampai pemasangan selesai dan VLC siap digunakan

![https://opensuse.id/wp-content/uploads/2018/02/vlc.png](https://opensuse.id/wp-content/uploads/2018/02/vlc.png)