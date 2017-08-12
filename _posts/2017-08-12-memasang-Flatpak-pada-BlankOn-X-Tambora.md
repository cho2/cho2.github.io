---
layout: post
title: "Memasang Flatpak Pada BlankOn X Tambora"
description: "Memasang Flatpak Pada BlankOn X Tambora"
comments: false
keywords: "Flatpak, BlankOn"
---

Apa itu [Flatpak](http://flatpak.org)? Silakan Anda baca sendiri pada tautan [ini](http://flatpak.org).

Versi Flatpak dilumbung BlankOn saat ini adalah 0.6.6-2. Untuk memasang aplikasi terbaru dari Flatpak, maka harus menggunakan versi terbaru. Untuk itu, kita coba **"meminjam"** paket Flatpak dari lumbung Debian Stretch.

Tambahkan baris berikut pada berkas `/etc/apt/sources.list` dengan penyunting teks favorit Anda
```
deb http://kartolo.sby.datautama.net.id/debian/ stretch main contrib non-free
```

Kemudian perbarui lumbung
```
sudo apt update
```

Pasang Flatpak
```
sudo apt install flatpak
```

Perlu Anda ketahui, paket-paket yang akan dipasang dan diperbarui adalah `bubblewrap dbus dbus-user-session dbus-x11 libdbus-1-3 libgail-3-0 libglib2.0-0 libglib2.0-bin libgtk-3-0 libgtk-3-common libostree-1-1 xdg-desktop-portal xdg-desktop-portal-gtk bubblewrap flatpak libostree-1-1 xdg-desktop-portal xdg-desktop-portal-gtk dbus dbus-user-session dbus-x11 libdbus-1-3 libgail-3-0 libglib2.0-0  libglib2.0-bin libgtk-3-0 libgtk-3-common`

Agar lumbung BlankOn tetap bersih, sunting kembali berkas `/etc/apt/sources.list` menjadi
```
#deb http://kartolo.sby.datautama.net.id/debian/ stretch main contrib non-free
```