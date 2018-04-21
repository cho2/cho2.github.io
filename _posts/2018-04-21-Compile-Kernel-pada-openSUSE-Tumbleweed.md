---
layout: post
title: "Compile Kernel Pada openSUSE Tumbleweed"
description: "Compile Kernel Pada openSUSE Tumbleweed"
comments: false
keywords: "openSUSE, Tumbleweed, Kernel"
---

Jadi ceritanya, sejak openSUSE Tumbleweed menggunakan kernel 4.16.x, Touchpad pada ThinkPad X1 Carbon 2015 saya tidak terdeteksi, sedangkan kernel sudah terlanjur naik. Konon, ada [binari yang tidak dibangun dengan benar](https://twitter.com/openSUSE/status/987254145773162497). Jadinya compile kernel 4.15.x sendiri.

* Pasang paket prasyarat
```
sudo zypper in autoconf rpm-build gcc
```

* Unduh kernel
```
wget https://cdn.kernel.org/pub/linux/kernel/v4.x/linux-4.15.18.tar.xz
```

* Ekstrak
```
tar xvf linux-4.15.18.tar.xz -C ~/src/
```

* Masuk ke direktori hasil ekstrak
```
cd ~/src/linux-4.15.18/
```

* Salin konfigurasi .config dari kernel saat ini
```
cp /boot/config-`uname -r` .config
```

* Tambahkan verbiage untuk membedakan penamaan kernel
```
nano Makefile
```
lalu modifikasi baris 
```
"EXTRAVERSION ="
``` 
ke (misal)
```
"EXTRAVERSION = -ThinkPadX1Carbon"
```

* Bangun kernel
```
`make rpm`
```

* Tunggu sampai proses bangun kernel selesai

* Pasang kernel
```
sudo zypper in ~/rpmbuild/RPMS/x86_64/kernel-4.15.18_ThinkPadX1Carbon_1_default-1.x86_64.rpm
```

* Reboot ke kernel baru

