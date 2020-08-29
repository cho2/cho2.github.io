---
layout: post
title: "Manjaro ARM GNOME di Raspberry Pi4"
description: "Manjaro ARM GNOME di Raspberry Pi4"
comments: false
keywords: "Manjaro, GNOME, Raspberry Pi4"
---

![https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-23/05-neofetch-gnome.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-23/05-neofetch-gnome.png)

Pada [pos sebelumnya](https://blog.kukuh.syafaat.id/2020/openSUSE-dengan-GNOME-di-Raspberry-Pi4/) sudah dibahas mengenai GNOME di Raspberry Pi4 dengan menggunakan openSUSE. Kali ini kita coba dengan Manjaro. Manjaro memiliki beberapa varian ARM selain Raspberry Pi4, salah satunya [Pinebook Pro](https://www.pine64.org/pinebook-pro/) yang sedang hangat dikalangan pengembang Linux di luar sana. Sayangnya pada versi ARM [20.06](https://forum.manjaro.org/t/manjaro-arm-20-06-released/112), Manjaro hanya menyediakan destop XFCE, KDE dan i3 (hanya untuk Pinebook dan Pinebook Pro). Baru di versi [20.08](https://forum.manjaro.org/t/manjaro-arm-20-08-released/1516) menyediakan dukungan i3 dan Sway untuk beberapa perangkat ARM. Tidak ada GNOME disitu, tapi itu bukan penghalang.

Image yang digunakan kali ini adalah [Manjaro ARM XFCE 20.06](https://osdn.net/projects/manjaro-arm/storage/rpi4/xfce/20.06/). Setelah berhasil dipasang, salah satu isu sebelumya berhasil diatasi, yaitu audio. Selanjutnya adalah memasang GNOME. Jalankan perintah berikut
```
sudo pacman -S gnome
```
setelah selesai, aktifkan GDM sebagai bawaaan
```
systemctl enable gdm.service --force
```
Mulai ulang dan GNOME berhasil dipasang. 
Sampai pada tahapan ini, kernel yang digunakan adalah `4.19.127-1` selaras dengan rilis [20.06](https://forum.manjaro.org/t/manjaro-arm-20-06-released/112). GNOME dapat berjalan dengan baik di Wayland maupun Xorg. (Sampai tahapan ini atau sebelum kernel ditingkatkan, semua cuplikan layar lupa diambil, mohon maaf). Agar selaras dengan [20.08](https://forum.manjaro.org/t/manjaro-arm-20-08-released/1516) dan mendapatkan pemutakhiran terkini, jalankan 
```
sudo pacman -Syu
```
Kernel terkini `5.4.51-2`. Waktu yang dibutuhkan dari awal boot sampai tampil GDM hanya **30 detik**. Pada Wayland, terdapat masalah ketika papan tik tidak dapat digunakan dalam aplikasi (misal mengetik di terminal atau gedit), tetapi dapat digunakan untuk mengetik pencarian di gnome-shell. Menggunakan papan tik virtual pun tidak menyelesaikan masalah ini. Beralih menggunakan xorg, semuanya lancar tanpa hambatan.


* Penggunaan memori awal (xorg)

  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-23/01-htop.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-23/01-htop.png)

* Skor `glmark2` (xorg)

  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-23/04-glmark2.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-23/04-glmark2.png)

  * Catatan: Skor kali ini lebih tinggi daripada skor yang dituliskan di [pos sebelumnya](https://blog.kukuh.syafaat.id/2020/openSUSE-dengan-GNOME-di-Raspberry-Pi4/)

* GNOME 3.36.5 Wayland

  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-23/02-gnome-wayland.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-23/02-gnome-wayland.png)

* GNOME 3.36.5 Xorg

  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-23/03-gnome-xorg.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-23/03-gnome-xorg.png)

Sekian 

Bonus: [Hardinfo](https://blog.kukuh.syafaat.id/raspi4-hardinfo-manjaro-arm-gnome/hardinfo_report.html)