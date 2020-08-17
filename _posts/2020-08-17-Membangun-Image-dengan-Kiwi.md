---
layout: post
title: "Membangun Image dengan Kiwi"
description: "Membangun Image dengan Kiwi"
comments: false
keywords: "Kiwi"
---

Masih ingat [SUSE Studio](https://en.wikipedia.org/wiki/SUSE_Studio)? SUSE Studio ini adalah salah satu perkakas daring untuk membangun image dan appliance atau dengan bahasa yang mudah adalah remaster. *User Experience* di SUSE Studio ini cukup baik sehingga kita bisa dengan mudah membangun atau meremaster distro berbasis openSUSE. Sayang sekali, di awal tahun 2018 SUSE Studio dimatikan. Peran SUSE Studio digantikan [Studio Express](https://studioexpress.opensuse.org/) yang masih dikembangkan (?). 

Teknologi dibelakang SUSE Studio adalah [Kiwi](https://en.opensuse.org/Portal:Kiwi). Kiwi juga digunakan pada [Open Build Service](https://openbuildservice.org/). Dengan menggunakan Open Build Service atau OBS, kita bisa membangun paket aplikasi, tidak hanya .rpm pada openSUSE, tetapi juga mendukung Arch, Raspi, Debian, Fedora, RedHat, Centos, Ubuntu, Univention, Mageia, dan appimage. Dengan integrasi Kiwi di OBS, kita bisa juga membangun image dan appliance dalam berbagai format seperti  ISO, Live CD/DVD, PXEBoot, Hard Disk, USB, Amazon EC2 (.ami), Docker, Google Cloud Format (.gce), KVM/Qemu (.qcow2), Open Virtualization Format (.ovf, .ova), Vagrant (.vagrant), Virtualbox (.vdi), Virtual Hard Disk (.vhd), Vmware (.vmdk), dan Xen.

Meremaster distro dengan OBS tidak se-*user friendly* SUSE Studio. Sampai saat ini saya masih gagal membangunnnya di OBS. Salah satu contoh distro berbasis openSUSE yang berhasil membangun imagenya di OBS adalah [Kamarada](https://kamarada.github.io/). Proyek di OBS-nya dapat dilihat [disini](https://build.opensuse.org/project/show/home:kamarada:15.2). Distro berbasis openSUSE lain yang cukup populer adalah [Geckolinux](https://geckolinux.github.io/), tetapi saya tidak dapat menemukannya di di OBS. Untungnya, kita bisa melihat berkas untuk membangun image-nya di [GitHub](https://github.com/geckolinux/geckolinux-project). 

Dengan gagalnya saya membangun image di OBS, maka alternatif lainnya adalah membangun di lokal menggunakan Kiwi. [Dokumentasinya](http://osinside.github.io/kiwi/) cukup lengkap, begitu juga yang ditulis [SUSE](https://documentation.suse.com/kiwi/9/pdf/kiwi_color_en.pdf) dalam bentuk pdf, Anda dapat mencetaknya bila perlu. Instalasinya pun cukup mudah, silakan [diikuti](http://osinside.github.io/kiwi/installation.html#installation-from-obs). Saya mencobanya di openSUSE Leap 15.2 dengan cukup menjalankan perintah `sudo zypper install python3-kiwi`. Keterbatasan membangun image di lokal adalah [kita hanya bisa membangun image berdasarkan versi sistem operasi yang kita pakai](http://osinside.github.io/kiwi/building_images.html#supported-distributions). Sebagai contoh, jika sistem operasi kita openSUSE Leap 15.2, maka kita hanya bisa membangun image berbasis openSUSE Leap 15.2, kita tidak bisa membangun image openSUSE Tumbleweed di atas openSUSE Leap 15.2.  

Sebagai langkah awal, kita bisa mencoba membangun image [JeOS](https://en.opensuse.org/Portal:JeOS) (Just Enough OS) dengan mengambil salah satu contoh dari [sini](https://github.com/OSInside/kiwi-descriptions).
Contoh perintah untuk membangun imagenya adalah 
```
sudo kiwi-ng --type iso system build --description kiwi-descriptions/suse/x86_64/suse-leap-15.2-JeOS --target-dir /tmp/myimage
```
Image yang sudah selesai dibangun akan ada pada direktori `/tmp/myimage` dengan ekstensi `.iso`. Lalu Anda dapat menjalankannya dengan perangkat lunak virtualisasi, misalnya [GNOME Boxes](https://wiki.gnome.org/Apps/Boxes). 
Contoh lainnya adalah Anda bisa coba membangun image berdasarkan skrip dari [Geckolinux](https://github.com/geckolinux/geckolinux-project) atau [Kamarada](https://build.opensuse.org/package/show/home:kamarada:15.2/Linux-Kamarada-GNOME). Inilah yang saya gunakan untuk proyek iseng iseng saya.

Saya mencoba meremaster openSUSE Leap 15.2 dengan menggunakan Kiwi. Proyek iseng ini saya namakan [Belajar](https://blog.kukuh.syafaat.id/belajar/), sebuah distribusi Linux tanpa terminal dan YaST, dalam format live, berisi aplikasi untuk pembelajaran seperti Gcompris, LibreOffice, Inkscape, dan GIMP. Tidak hanya itu, saya menyertakan buku [Belajar Komputer Tingkat Dasar](http://imgos-belajarlinux.blogspot.com/2020/06/buku-belajar-komputer-tingkat-dasar-5.html) dan beberapa buku lainnya yang ditulis oleh Pak Sokibi seperti LibreOffice dan Inkscape. Kodenya dapat Anda lihat [disini](https://github.com/cho2/belajar/blob/20.08/kiwi-source.tar.xz). Distro [Belajar](https://blog.kukuh.syafaat.id/belajar/) saya rilis hari ini, 17 Agustus 2020, sehingga saya beri kode rilis 20.08, Anda dapat mengunduhnya [disini](https://osdn.net/projects/belajar/downloads/73443/Belajar.x86_64-20.08.iso/) atau [disini](https://drive.google.com/file/d/1sulTJM8ybqmYpcG-A_DQAmNkRbYwfAKV/view?usp=sharing). Proyek iseng selanjutnya mungkin membangun [Belajar](https://blog.kukuh.syafaat.id/belajar/) di OBS, akan dilanjutkan jika ada waktu luang.

Merdeka!!!