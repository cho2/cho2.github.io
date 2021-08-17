---
layout: post
title: "Snap di openSUSE MicroOS - Bagian 2"
description: "Snap di openSUSE MicroOS - Bagian 2"
comments: false
keywords: "openSUSE, MicroOS, Snap"
---

[Lanjutan dan pemutakhiran dari pos sebelumnya](https://blog.kukuh.syafaat.id/2021/Snap-di-openSUSE-MicroOS/), topik ini juga saya bawakan pada [openSUSE.Asia Virtual Summit 2021](https://events.opensuse.org/conferences/oSAS21/program/proposals/3635).

Sebelumnya MicroOS Desktop menggunakan `transactional-update`, sekarang menggunakan `tukit`. Langkah pertama berubah menjadi seperti berikut
```
$ sudo tukit --continue execute bash
    # zypper addrepo --refresh https://download.opensuse.org/repositories/system:/snappy/openSUSE_Tumbleweed snappy
    # zypper --gpg-auto-import-keys refresh
    # zypper ref
    # zypper in snapd
    # exit
$ sudo reboot
```

Langkah berikutnya masih sama dengan pos sebelumnya, yaitu
```
$ sudo mksubvolume /snap
$ source /etc/profile
$ sudo systemctl enable --now snapd
$ sudo systemctl enable --now snapd.apparmor
``` 

Pada pos sebelumnya, snap bisa langsung dijalankan. Saat ini, SELinux sudah masuk di MicroOS Desktop, sehingga terdapat dua opsi

1. Jika Anda baru memasang MicroOS Desktop dan berencana menggunakan snap, saat pemasangan awal, pastikan Anda memilih mode `disabled` pada SELinux
    - [Lihat juga berkas ini halaman 46-47](https://blog.kukuh.syafaat.id/slides/oSAVS-2021/snap-microos-desktop.pdf) 
1. Jika Anda sudah terlanjur memasang MicroOS Desktop dengan mode SELinux `enforcing` atau `enabled` dan masih ingin menggunakan snap, maka caranya agak sedikit merepotkan.
    - Saat booting, pastikan pada parameter kernel terdapat `selinux=1`, ganti menjadi `selinux=0`.
    - Setelah berhasil booting dengan parameter kernel `selinux=0`, buka terminal, periksa dengan perintah `sestatus` untuk mengetahui status SELinux. Jika keluarannya `disabled`, maka bisa lanjut.
    - [Lebih lanjut, lihat juga berkas ini halaman 48-51](https://blog.kukuh.syafaat.id/slides/oSAVS-2021/snap-microos-desktop.pdf) 

Proses dapat dilanjutkan dengan memasang aplikasi snap. Anda bisa memasang hello-world sebagai percobaan dengan perintah `snap install hello-world` dan jalankan dengan perintah `snap run hello-world`.

Topik ini akan dibawakan kembali pada [Ubucon Asia 2021](https://2021.ubucon.asia/id/). Sebagai tambahan informasi, snap tidak didukung resmi pada openSUSE MicroOS Desktop. Risiko pemasangan ditanggung pengguna!