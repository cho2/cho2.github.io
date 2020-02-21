---
layout: post
title: "Menuju GNOME 3.36"
description: "Menuju GNOME 3.36"
comments: false
keywords: "GNOME"
---

GNOME 3.36 akan rilis [11 Maret 2020](https://wiki.gnome.org/ThreePointThirtyfive). Berikut ini beberapa catatan saya mengenai pengembangan GNOME 3.35.

# GNOME l10n

* [GNOME l10n](https://l10n.gnome.org/languages/id/gnome-3-36/ui/) masih bergulir, target untuk UI 100%. Ada beberapa penerjemah baru. Dokumentasi sudah mencapai 30%. Hasil ngobrol dengan [Pak Andika](https://l10n.gnome.org/users/andika/), beliau ingin naik ke 40%. Tetapi saya nawar ke 35%, itu juga nanti di GNOME 3.38 :)).


# [GNOME 3.35.90](https://mail.gnome.org/archives/desktop-devel-list/2020-February/msg00000.html)

* Coba dengan unduh berkas [qcow2](https://gitlab.gnome.org/GNOME/gnome-build-meta/-/jobs/583996/artifacts/browse/image/) dari lumbung [`gnome-build-meta`](https://gitlab.gnome.org/GNOME/gnome-build-meta/). Gagal dijalankan.

   Kalau berhasil, tampilannya mestinya seperti berikut

   ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-02-21/Screenshot%20from%202020-02-10%2021-29-53.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-02-21/Screenshot%20from%202020-02-10%2021-29-53.png)
   (Tangkapan layar dari [Rocket Chat GNOME](https://chat.gnome.org/))

* Coba dengan unduh berkas iso [GNOME Next - openSUSE Tumbleweed](https://download.opensuse.org/repositories/GNOME:/Medias/images/iso/?P=GNOME_Next*). Berhasil boot dan masuk destop.

   ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-02-21/tw-33590.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-02-21/tw-33590.png)

* Coba dengan memutakhirkan vm openSUSE Tumbleweed dengan lumbung [GNOME Next](http://download.opensuse.org/repositories/GNOME:/Next/openSUSE_Factory/). Gagal.

   ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-02-21/oh-tak.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-02-21/oh-tak.png)

* Coba dengan memutakhirkan vm [Fedora Rawhide](https://fedoraproject.org/wiki/Releases/Rawhide). Gagal.

* Coba dengan unduh iso [Fedora Rawhide](https://dl.fedoraproject.org/pub/fedora/linux/development/rawhide/Workstation/x86_64/iso/). Gagal.

# [GNOME 3.35.91](https://mail.gnome.org/archives/desktop-devel-list/2020-February/msg00054.html)

* Coba dengan unduh berkas [qcow2](https://gitlab.gnome.org/GNOME/gnome-build-meta/-/jobs/598561/artifacts/file/image/disk.qcow2) dari lumbung [`gnome-build-meta`](https://gitlab.gnome.org/GNOME/gnome-build-meta/). Gagal dijalankan. Coba dengan [GNOME Boxes Nightly](https://feborg.es/gnome-nightly-vm-images-with-gnome-boxes/), gagal.


* Coba [tiket #2226 `gnome-shell`](https://gitlab.gnome.org/GNOME/gnome-shell/issues/2226).

   * Bangun [`gnome-shell` master di Fedora 31](https://gitlab.gnome.org/snippets/1017). Tidak dilanjutkan, diska penuh.
   * Coba bangun [`gnome-shell` master di openSUSE Tumbleweed](https://gist.github.com/cho2/5c42dd7c4015ae6618d351418485c9a9). Gagal saat bangun mutter, `libpipewire` masih jadi misteri .

* Coba dengan unduh berkas iso [GNOME Next - openSUSE Tumbleweed](https://download.opensuse.org/repositories/GNOME:/Medias/images/iso/?P=GNOME_Next*). Berhasil.

* Coba dengan memutakhirkan vm openSUSE Tumbleweed dengan lumbung [GNOME Next](http://download.opensuse.org/repositories/GNOME:/Next/openSUSE_Factory/). Gagal.

* Coba dengan memutakhirkan vm [Fedora Rawhide](https://fedoraproject.org/wiki/Releases/Rawhide). Gagal.

* Coba dengan unduh iso [Fedora Rawhide](https://dl.fedoraproject.org/pub/fedora/linux/development/rawhide/Workstation/x86_64/iso/). Gagal.

* Coba dengan unduh iso [Fedora 32](https://dl.fedoraproject.org/pub/fedora/linux/development/32/Workstation/x86_64/iso/). Berhasil.

   ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-02-21/F32-1.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-02-21/F32-1.png)

   ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-02-21/F32-2.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-02-21/F32-2.png)

Sampai jumpa di GNOME 3.35.92.