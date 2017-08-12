---
layout: post
title: "Memasang LibreOffice 5.4 Menggunakan Flatpak Pada openSUSE Leap 42.3"
description: "Memasang LibreOffice 5.4 Menggunakan Flatpak Pada openSUSE Leap 42.3"
comments: false
keywords: "LibreOffice, Flatpak, openSUSE"
---

Langkah pertama adalah memasang [Flatpak](http://flatpak.org) pada openSUSE
```
$ sudo zypper install flatpak
```

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

![https://opensuse.id/wp-content/uploads/2017/08/VirtualBox_Leap-42.3_12_08_2017_19_32_53.png](https://opensuse.id/wp-content/uploads/2017/08/VirtualBox_Leap-42.3_12_08_2017_19_32_53.png)