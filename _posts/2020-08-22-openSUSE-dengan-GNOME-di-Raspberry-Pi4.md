---
layout: post
title: "openSUSE dengan GNOME di Raspberry Pi4"
description: "openSUSE dengan GNOME di Raspberry Pi4"
comments: false
keywords: "openSUSE, GNOME, Raspberry Pi4"
---

Raspberry Pi memiliki sistem operasi bawaan, yaitu Raspberry Pi OS (sebelumnya Raspbian) berbasis Debian Buster. Karena mau antimainstream, mari kita pasang openSUSE di Raspberry Pi4. Kebetulan Raspberry Pi4 yang diuji coba memiliki RAM 8 GB, mari mencoba dengan destop GNOME yang konon katanya berat. 

Pada wiki [Raspberry Pi4 openSUSE](https://en.opensuse.org/HCL:Raspberry_Pi4), tersedia pilihan openSUSE Leap dan Tumbleweed dengan berbagai macam pilihan destop (E20, XFCE, KDE, LXQT, dan X11). Tapi sampai blog ini ditulis, tidak tercantum destop GNOME disitu. Jangan khawatir, pergi ke halaman [http://download.opensuse.org/ports/aarch64/distribution/leap/15.2/appliances/](http://download.opensuse.org/ports/aarch64/distribution/leap/15.2/appliances/) dan temukan [openSUSE-Leap-15.2-ARM-GNOME-raspberrypi4.aarch64.raw.xz](http://download.opensuse.org/ports/aarch64/distribution/leap/15.2/appliances/openSUSE-Leap-15.2-ARM-GNOME-raspberrypi4.aarch64.raw.xz) untuk openSUSE Leap, tersedia juga image yang sama untuk Raspberry Pi3. Siapkan SD Card (direkomendasikan 8 GB dan kelas 10) dan tulis image tersebut kesitu.

# openSUSE Leap 15.2

Awal boot sampai tampil GDM membutuhkan waktu sangat lama (**kurang lebih 3 menit**), tetapi setelah masuk ke destop sudah cukup responsif. Menurut [wiki](https://en.opensuse.org/HCL:Raspberry_Pi4), ada beberapa isu yang sudah diketahui, sepertinya beberapa hal tersebut berhubungan dengan kernel. Tidak seperti di Raspbian yang memodifikasi kernelnya (dan beberapa OS lain di Raspberry Pi4 seperti Manjar0), Kernel di Raspberry Pi4 openSUSE masih menggunakan official mainline kernel dari upstream. Untuk isu tidak adanya audio, [penggerak audio tidak masuk di kernel upstream dan pengembang yang terkait isu ini sedang liburan.](https://lists.opensuse.org/opensuse-arm/2020-08/msg00003.html). Perbedaan lain dengan Raspbian adalah proses boot. Pada Raspbian kernel dimuat secara langsung, sementara pada openSUSE U-Boot boot loader digunakan untuk menyediakan lingkungan boot EFI dan binari GRUB2 EFI merupakain *chain-loaded* untuk menyediakan layar boot grafis. ~~Selain itu, pada openSUSE menggunakan sistem berkas Btrfs pada partisi root, kompresi diaktifkan secara bawaan untuk kinerja kartu SD yang lebih baik.~~ Kernel pada openSUSE Leap 15.2 adalah `5.3.18`.

* GNOME 3.34

    ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-22/02-leap-gnome.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-22/02-leap-gnome.png)

* Penggunaan memori awal

    ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-22/01-leap-htop.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-22/01-leap-htop.png)
    
* Skor `glmark2`

    * Percobaan pertama

    ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-22/03-leap-glmark2.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-22/03-leap-glmark2.png)

    * Percobaan kedua

    ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-22/03-leap-glmark2-2.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-22/03-leap-glmark2-2.png)

  * Catatan: Sebagai bahan perbandingan, pada mesin yang sama  didapatkan skor 96 dengan menggunakan [Manjaro ARM XFCE](https://manjaro.org/downloads/arm/raspberry-pi-4/arm8-raspberry-pi-4-xfce/). Kemungkinan karena penggerak grafis masih menggunakan llvmpipe sehingga skor di openSUSE Leap 15.2 masih rendah.

* Menjalankan LibreOffice (Flatpak)

    ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-22/04-leap-libreoffice.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-22/04-leap-libreoffice.png)

* Menjalankan Inkscape (Flatpak)

    ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-22/05-leap-inkscape.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-22/05-leap-inkscape.png)

* Menjalankan Gimp (rpm)

    ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-22/06-leap-gimp.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-22/06-leap-gimp.png)

* Menjalankan Chromium (rpm) 10 tab

    ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-22/07-leap-chromium.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-22/07-leap-chromium.png)

* Menjalankan LibreOffice (Flatpak), Inkscape (Flatpak), Gimp (rpm), dan Chromium (rpm) 10 tab.

    ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-22/08-leap-all.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-22/08-leap-all.png)

* Meningkatkan openSUSE Leap ke Tumbleweed

    Ganti repo berikut
    ```
    https://download.opensuse.org/ports/aarch64/distribution/leap/$releasever/repo/oss/
    https://download.opensuse.org/ports/update/leap/$releasever/oss/
    ```
    menjadi
    ```
    https://download.opensuse.org/ports/aarch64/tumbleweed/repo/oss/
    https://download.opensuse.org/ports/aarch64/update/tumbleweed/
    ```
    Lalu jalankan perintah `zypper ref` dan `zypper dup`.

    ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-22/09-leap-upgrade-tumbleweed.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-08-22/09-leap-upgrade-tumbleweed.png)

    Hasilnya ada pada bagian selanjutnya.

# openSUSE Tumbleweed

## Percobaan 1

Setelah berhasil meningkatkan dari openSUSE Leap ke openSUSE Tumbleweed, mari mencobanya. Waktu yang dibutuhkan dari awal boot hingga tampil GDM adalah **2,23 menit**. Setelah muncul GDM, macet, tetikus dan papan tik tak dapat bergerak. Dibiarkan lama, layar menghitam. Kernel terkini pada openSUSE Tumblweed adalah `5.7.11`.

## Percobaan 2

Dicoba dengan mengunduh image [openSUSE Tumbleweed GNOME Raspberry Pi4, snapshot 7 Agustus 2020](http://download.opensuse.org/ports/aarch64/tumbleweed/images/openSUSE-Tumbleweed-ARM-GNOME-raspberrypi4.aarch64-2020.07.28-Snapshot20200807.raw.xz). Waktu yang dibutuhkan dari awal boot hingga tampil GDM adalah **4,05 menit**. Setelah muncul GDM, macet, tetikus dan papan tik tak dapat bergerak. Dibiarkan lama, layar menghitam. Kernel terkini pada openSUSE Tumblweed adalah `5.7.11`.

Sementara ini, openSUSE Tumbleweed masih belum bisa masuk destop. Dicoba dengan destop XFCE pun masih sama.