---
layout: post
title: "Menambahkan Palet Warna Pada Inkscape Flatpak"
description: "Menambahkan Palet Warna Pada Inkscape Flatpak"
comments: false
keywords: "inkscape, flatpak"
---

Sampai pos ini ditulis, versi Inkscape pada flatpak sudah mencapai [0.92.3](https://github.com/flathub/org.inkscape.Inkscape/blob/master/org.inkscape.Inkscape.json). Bagaimana menambahkan palet warna pada Inkscape versi flatpak? Normalnya palet warna ada pada direktori `/usr/share/inkscape/palettes/`. Sedangkan pada Inkscape versi flatpak, palet warna ada pada direktori `/home/namaPengguna/.var/app/org.inkscape.Inkscape/config/inkscape/palettes`.
Cara menambahkannya tinggal salin saja `paletWarna.gpl` ke direktori diatas. :D