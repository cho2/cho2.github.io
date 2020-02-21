---
layout: post
title: "Mencoba Image GNOME Nightly VM dengan GNOME Boxes"
description: "Mencoba Image GNOME Nightly VM dengan GNOME Boxes"
comments: false
keywords: "GNOME, GNOME Boxes"
---

GNOME 3.36 akan rilis sebentar lagi. Bagi yang tidak sabar, Anda bisa mencoba image GNOME nightly dengan GNOME Boxes nightly tentunya. Pastikan Anda sudah memasang Flatpak.

## Memasang GNOME Boxes Nightly

1. Pasang repo Flatpak GNOME Nightly
   ```
   flatpak remote-add --if-not-exists gnome-nightly https://nightly.gnome.org/gnome-nightly.flatpakrepo
   ```

2. Pasang GNOME Boxes Nightly
   ```
   flatpak install gnome-nightly org.gnome.BoxesDevel
   ```


## Mencoba Image GNOME Nightly

1. Unduh image GNOME Nightly dalam bentuk berkas [qcow2](https://gitlab.gnome.org/GNOME/gnome-build-meta/-/jobs/598561/artifacts/file/image/disk.qcow2), misalnya [GNOME 3.35.91](https://mail.gnome.org/archives/desktop-devel-list/2020-February/msg00054.html)

2. Buka dialog VM di GNOME Boxes dan klik entri **“GNOME Nightly”** pada bagian **Unduhan Menarik**. Kemudian akan muncul jendela untuk memilih berkas.

   ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-02-22/gnome-nightly.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-02-22/gnome-nightly.png)

3. Setelah memilih berkas qcow2 yang sudah diunduh pada langkah 1, lanutkan dengan **Buat** VM. Setelah selesai membuat VM, Anda dapat memulai VM dengan mengkliknya.

Selamat mencoba!

Referensi: [Try the GNOME Nightly VM images with GNOME Boxes](https://feborg.es/gnome-nightly-vm-images-with-gnome-boxes/)
