---
layout: post
title: "Mencoba GNOME Boxes Beta dengan Flatpak pada openSUSE Leap 15.0"
description: "Mencoba GNOME Boxes Beta dengan Flatpak pada openSUSE Leap 15.0"
comments: false
keywords: "GNOME Boxes, Flatpak, openSUSE, Leap"
---

Sekarang Anda dapat memasang Flatpak Beta dari Flatpak, lebih lanjut silakan dibaca [disini](https://blogs.gnome.org/alexl/2019/02/19/changes-in-flathub-land/).
Sebelum mencoba panduan ini, pastikan Anda sudah memasang `flatpak`. Sebelum GNOME Boxes 3.32 rilis, kita bisa mencoba versi 3,31 (beta) dengan cara berikut.

* Menambahkan repo Flatpak Beta dari Flathub

	```
	flatpak remote-add flathub-beta https://flathub.org/beta-repo/flathub-beta.flatpakrepo
	```

* Memasang GNOME Boxes Beta

	```
	flatpak install flathub-beta org.gnome.Boxes
	```

* Menjalankan GNOME Boxes Beta

	```
	flatpak run org.gnome.Boxes//beta
	```

Selamat mencoba, have fun!