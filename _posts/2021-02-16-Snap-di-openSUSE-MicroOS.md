---
layout: post
title: "Snap di openSUSE MicroOS"
description: "Snap di openSUSE MicroOS"
comments: false
keywords: "openSUSE, MicroOS, Snap"
---

Sekadar catatan pribadi saja, siapa tahu nanti ada yang membutuhkan juga.

Pasang [snap](https://snapcraft.io/) di [MicroOS](https://microos.opensuse.org/), jalankan
```
$ sudo transactional-update shell
  # zypper addrepo --refresh https://download.opensuse.org/repositories/system:/snappy/openSUSE_Tumbleweed snappy
  # zypper --gpg-auto-import-keys refresh
  # zypper ref
  # zypper dup --from snappy
  # zypper in snapd
  # exit
$ sudo reboot
```
Setelah reboot jalankan
```
$ sudo mksubvolume /snap
$ source /etc/profile
$ sudo systemctl enable --now snapd
$ sudo systemctl enable --now snapd.apparmor
``` 
Lalu pasang aplikasi lewat snap, contoh poedit
```
snap install poedit
```
Jalankan lewat terminal
```
snap run poedit
```
Apabila menemui galat berikut `snap-confine has elevated permissions and is not confined but should be. Refusing to continue to avoid permission escalation attacks`, jalankan
```
sudo apparmor_parser -r /etc/apparmor.d/*snap-confine*
sudo apparmor_parser -r /var/lib/snapd/apparmor/profiles/snap-confine*
```
Jalankan ulang lewat terminal
```
snap install poedit
```
Aapbila menemukan galat seperti gambar berikut ini,
![https://gitlab.com/cho2/blog-images/-/raw/master/2021-02-16/1.png](https://gitlab.com/cho2/blog-images/-/raw/master/2021-02-16/1.png)
jalankan
```
sudo rm /var/cache/fontconfig/*
rm ~/.cache/fontconfig/*
fc-cache -r
```
Jalankan ulang lagi lewat terminal
```
snap install poedit
```
Hasilnya 

![https://gitlab.com/cho2/blog-images/-/raw/master/2021-02-16/2.png](https://gitlab.com/cho2/blog-images/-/raw/master/2021-02-16/2.png)


Have Fun!