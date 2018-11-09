---
layout: post
title: "Mengunci Versi Kernel Pada openSUSE"
description: "Mengunci Versi Kernel Pada openSUSE"
comments: false
keywords: "Kernel, openSUSE, Tumbleweed"
---

Jadi ceritanya saya meningkatkan versi openSUSE pada komputer saya yang sebelumnya menggunakan Leap 15.0 menjadi Tumbleweed dengan mengganti repositorinya. Ini sebenarnya karena ada kecelakaan kecil ketika saya coba-coba menaikkan versi `Flatpak` (bisa lihat tulisan saya sebelumnya mengenai Backup Flatpak [disini](https://blog.kukuh.syafaat.id/2018/backup-flatpak/) dan [sini](https://blog.kukuh.syafaat.id/2018/backup-flatpak-2/)). Belajar dari pengalaman menggunakan Tumbleweed yang versi kernelnya sering naik dan tidak jarang ada galat (bisa lihat mengenai masalah yang pernah saya hadapi [disini](https://blog.kukuh.syafaat.id/2018/Compile-Kernel-pada-openSUSE-Tumbleweed/)), maka saya ingin menggunakan Tumbleweed dengan tetap menggunakan kernel dari Leap 15.0. Akan tetapi, setiap menjalankan `zypper dup` seringkali versi kernel ikut naik. Maka dari itu, kita perlu mengunci versi kernel pada versi tertentu. 

Sampai tulisan ini ditulis, versi kernel pada openSUSE Leap 15.0 adalah 
```
4.12.14-lp150.12.22-default 
```

Mengapa versi kernel openSUSE Leap sangat tua? Jawabannya dapat Anda temukan [disini](https://en.opensuse.org/Portal:Leap/Leap_kernel_version).

Cara mengunci versi kernel adalah sebagai berikut.
```
sudo zypper addlock kernel-*
```
atau
```
sudo zypper al kernel-*
```

Perintah diatas akan mengunci semua paket yang berawalan `kernel` dan diikuti oleh `-*` apapun, misalnya paket `kernel-default`, `kernel-devel`, `kernel-default-devel`, dsb.

Untuk membukanya, cukup jalankan perintah berikut.
```
sudo zypper removelock kernel-*
```
atau
```
sudo zypper rl kernel-*
```

Untuk melihat daftar paket apa saja yang terkunci versinya, jalankan perintah berikut.
```
zypper locks
```
atau
```
zypper ll
```

Contoh keluarannya sebagai berikut
```
# | Nama     | Tipe    | Repositori
--+----------+---------+-----------
1 | kernel-* | package | (apapun)  
```

Have Fun!
