---
layout: post
title: "Memasang Inkscape 1.0 Beta Dengan Flatpak"
description: "Memasang Inkscape 1.0 Beta Dengan Flatpak"
comments: false
keywords: "Inkscape, Flatpak"
---

[Inkscape versi 1.0](https://inkscape.org/release/inkscape-1.0/) akan dirilis dalam waktu dekat. Sampai tulisan ini ditulis, versi beta sudah mencapai [Beta 2](https://inkscape.org/release/inkscape-1.0beta2/). Pengguna setia Inkscape tentu dapat mencoba dan mengujinya. Selain mengunduh dari [sini](https://inkscape.org/release/1.0beta2/platforms/), pengguna dapat juga mencoba versi beta dengan Flatpak.

* Pastikan Anda sudah memasang `flatpak`
* Tambahkan repo `flathub-beta`
  ```
  flatpak remote-add flathub-beta https://flathub.org/beta-repo/flathub-beta.flatpakrepo
  ```
* Pasang Inkscape dari `flathub-beta`
  ```
  flatpak install flathub-beta org.inkscape.Inkscape
  ```

Versi terkini pada `flathub-beta` adalah `1.0-beta2`. 
Selamat mencoba!