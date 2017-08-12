---
layout: post
title: "Memasang LibreOffice 5.4 Menggunakan Flatpak Pada BlankOn X Tambora"
description: "Memasang LibreOffice 5.4 Menggunakan Flatpak Pada BlankOn X Tambora"
comments: false
keywords: "LibreOffice, Flatpak, BlankOn"
---

Pastikan Anda sudah memasang [Flatpak pada BlankOn](http://blog.kukuh.syafaat.id/2017/memasang-Flatpak-pada-BlankOn-X-Tambora/).

Berikutnya adalah menambahkan repositori Flatpak yang mengandung runtime GNOME

```
$ wget https://sdk.gnome.org/keys/gnome-sdk.gpg
$ flatpak remote-add --user --gpg-import=gnome-sdk.gpg gnome https://sdk.gnome.org/repo/
$ flatpak install --user gnome org.gnome.Platform 3.24
```

Unduh berkas LibreOffice Flatpak pada laman [ini](http://www.libreoffice.org/download/flatpak/)
```
$ wget http://download.documentfoundation.org/libreoffice/flatpak/latest/LibreOffice.flatpak
```

Pasang LibreOffice Flatpak
```
$ flatpak install --user --bundle LibreOffice.flatpak
```

Jalankan LibreOffice Flatpak
```
$ flatpak run org.libreoffice.LibreOffice
```

![http://panduan.blankonlinux.or.id/wp-content/uploads/2017/08/VirtualBox_BlankOn-Tambora_12_08_2017_13_46_35-1024x517.png](http://panduan.blankonlinux.or.id/wp-content/uploads/2017/08/VirtualBox_BlankOn-Tambora_12_08_2017_13_46_35-1024x517.png)