---
layout: post
title: "Mencoba Fedora Atomic Workstation"
description: "Mencoba Fedora Atomic Workstation"
comments: false
keywords: "Fedora, Atomic, OSTree"
---

Tentang Fedora Atomic Workstation, bisa dibaca-baca [disini](https://www.projectatomic.io/blog/2018/02/fedora-atomic-workstation/). Berbeda dengan Fedora Workstation biasa, Fedora Atomic Workstation ini menggunakan [ostree](https://ostree.readthedocs.io/en/latest/), pada Fedora dikenal dengan [`rpm-ostree`](https://rpm-ostree.readthedocs.io/en/latest/). Jika Anda sudah pernah menggunakan [Endless OS](https://endlessos.com/), konsep dasarnya sama, yaitu seperti `git`. Yang membedakan hanyalah Endless OS berbasis Debian, sehingga menggunakan [`deb-ostree`](https://github.com/dbnicholson/deb-ostree-builder). Sama seperti pada Endless OS, jangan harap untuk memasang/memperbarui paket melalui perintah `dnf`, gunakan [flatpak](https://flatpak.org/) untuk memasang aplikasi. Flatpak secara bawaan sudah terpasang pada Fedora Atomic Worksation, hanya saya belum ada runtime dan aplikasi yang terpasang secara bawaan.

Untuk melihat status Fedora Atomic Workstation, jalankan perintah
```
rpm-ostree status
``` 

Untuk memperbarui Fedora Atomic Workstation, jalankan perintah
```
rpm-ostree upgrade
``` 
Setelah menjalankan `rpm-ostree`, pembaruan tidak langsung tersedia, pengguna akan diminta untuk reboot, jalankan perintah
```
systemctl reboot
```

Bagi pengguna yang baru memasang Fedora Atomic Workstation dan menjalankan perintah `rpm-ostree upgrade` untuk pertama kali, proses pembaruan akan berlangsung lama (bergantung pada sambungan internet juga), kemungkinan karena banyaknya pembaruan sehingga banyak data yang harus ditarik. Saya sendiri membutuhkan waktu lebih dari dua jam.

![https://gitlab.com/cho2/blog-images/raw/master/2018-04-05/1.png](https://gitlab.com/cho2/blog-images/raw/master/2018-04-05/1.png)
Tangkapan layar saat melihat status dan memperbarui Fedora Atomic Workstation

![https://gitlab.com/cho2/blog-images/raw/master/2018-04-05/2.png](https://gitlab.com/cho2/blog-images/raw/master/2018-04-05/2.png)
Tangkapan layar saat melihat status setelah memperbarui Fedora Atomic Workstation

Sebentar lagi, Fedora 28 akan rilis. Fedora Atomic Workstation 28 Beta dapat diunduh [disini](https://download.fedoraproject.org/pub/fedora/linux/releases/test/28_Beta/AtomicWorkstation/x86_64/iso/Fedora-AtomicWorkstation-ostree-x86_64-28_Beta-1.3.iso). Bila sudah memasang versi sebelumnya, pengguna dapat melakukan naik versi ke Fedora 28 beta pada versi Atomic Workstation dengan cara menjalankan perintah
```
# rpm-ostree rebase atomic:fedora/28/x86_64/workstation
```
Jika keluaran dari perintah tersebut berupa `error: Remote "atomic" not found`, jalankan perintah berikut untuk menambahkan remote "atomic"
```
# ostree remote add --set=gpgkeypath=/etc/pki/rpm-gpg/RPM-GPG-KEY-fedora-28-primary atomic https://kojipkgs.fedoraproject.org/atomic/repo
```
Jangan lupa untuk menjalankan berikut setelah proses naik versi berhasil
```
systemctl reboot
```
![https://gitlab.com/cho2/blog-images/raw/master/2018-04-05/3.png](https://gitlab.com/cho2/blog-images/raw/master/2018-04-05/3.png)
Tangkapan layar saat melihat status setelah memperbarui Fedora Atomic Workstation dari 27 ke 28 beta

![https://gitlab.com/cho2/blog-images/raw/master/2018-04-05/4.png](https://gitlab.com/cho2/blog-images/raw/master/2018-04-05/4.png)
Fedora 28 dengan GNOME 3.28

Referensi dan bahan bacaan:

* [Project Atomic](https://www.projectatomic.io/)
* [OSTree](https://ostree.readthedocs.io/en/latest/)
* [Flatpak](https://flatpak.org/)
* [Fedora Atomic Workstation](https://www.projectatomic.io/blog/2018/02/fedora-atomic-workstation/)
* [Fedora Atomic Workstation: Trying things out the easy way](https://blogs.gnome.org/mclasen/2018/03/08/fedora-atomic-workstation-trying-things-out-the-easy-way/)
* [Fedora Atomic Workstation: Ruling the commandline](https://blogs.gnome.org/mclasen/2018/03/16/fedora-atomic-workstation-ruling-the-commandline/)
* [Fedora Atomic Workstation: Almost fool-proof](https://blogs.gnome.org/mclasen/2018/03/22/fedora-atomic-workstation-almost-fool-proof/)
* [Fedora Atomic Workstation: Beta](https://blogs.gnome.org/mclasen/2018/04/03/fedora-atomic-workstation-beta/)