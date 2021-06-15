---
layout: post
title: "Memutar Spotify di Raspberry Pi dengan Spot"
description: "Memutar Spotify di Raspberry Pi dengan Spot"
comments: false
keywords: "Spotify, Spot, Flatpak, Raspberry Pi"
---

> T: Memutar Spotify di Raspberry Pi? Bisa?

> J: Bisa, pasti bisa!

Konteksnya adalah Raspberry Pi dengan destop. Kebetulan saya menggunakan destop GNOME di Raspberry Pi 4. Sebelumnya saya pernah mencoba  [Raspotify](https://github.com/dtcooper/raspotify). Hanya saja ini merupakan klien Spotify Connect, jadi hanya numpang memutar audionya saja di Raspberry Pi 4, memilih lagu tetap harus melalui gawai lain.

Klien [Spotify](https://flathub.org/apps/details/com.spotify.Client) di Flathub hanya mendukung arsitektur [`x86_64`](https://github.com/flathub/com.spotify.Client/blob/master/flathub.json#L2). Lalu saya menemukan aplikasi bernama [Spot](https://flathub.org/apps/details/dev.alextren.Spot) di Flathub. Coba pasang Raspberry Pi 4, berhasil (berarti mendukung `arm64`). Perintahnya 
```
flatpak install flathub dev.alextren.Spot
```

Kemudian, masuk dengan akun Spotify, jreng!

![https://gitlab.com/cho2/blog-images/-/raw/master/2021-06-15/spot.png](https://gitlab.com/cho2/blog-images/-/raw/master/2021-06-15/spot.png)

Yang perlu diperhatikan, Spot ini hanya bisa berjalan dengan akun premium saja seperti yang dijelaskan di [Github](https://github.com/xou816/spot).

> Gtk/Rust native Spotify client for the GNOME desktop. Only works with premium accounts!

Tertarik berkontribusi? Spot ini bisa dibangun dengan [GNOME Builder](https://wiki.gnome.org/Apps/Builder) lho!

