---
layout: post
title: "Menuju Nautilus 3.30"
description: "Menuju Nautilus 3.30"
comments: false
keywords: "Nautilus, GNOME, Flatpak, GTK"
---

![https://www.omgubuntu.co.uk/wp-content/uploads/2018/07/nautilus-3-30.jpg](https://www.omgubuntu.co.uk/wp-content/uploads/2018/07/nautilus-3-30.jpg)
Gambar oleh [OMG Ubuntu](https://www.omgubuntu.co.uk/2018/07/nautilus-3-30-improvements-new-path-bar) 

Apa saja yang baru di Nautilus 3.30?

* Desain bilah alat yang baru
   
* Ukuran ruang dinamis

* dll :)


Mau mencobanya? Pastikan `flatpak` sudah terpasang pada sistem Anda

* Tambahkan repo flatpak `gnome-nightly`
    ```
    flatpak remote-add --if-not-exists gnome-nightly https://sdk.gnome.org/gnome-nightly.flatpakrepo
    ```
* Tambahkan repo flatpak `gnome-apps-nightly`
    ```
    flatpak remote-add --if-not-exists gnome-apps-nightly --from https://sdk.gnome.org/gnome-apps-nightly.flatpakrepo
    ```
* Pasang `nautilus` versi pengembangan
    ```
    flatpak install gnome-apps-nightly org.gnome.NautilusDevel 
    ```
* BONUS: Mau mencoba `nautilus` dengan GTK 4?
    ```
    flatpak install gnome-apps-nightly org.gnome.NautilusGtk4
    ```

Bahan bacaan lainnya:

* [https://csorianognome.wordpress.com/2018/07/27/nautilus-3-30/](https://csorianognome.wordpress.com/2018/07/27/nautilus-3-30/)

* [https://www.omgubuntu.co.uk/2018/07/nautilus-3-30-improvements-new-path-bar](https://www.omgubuntu.co.uk/2018/07/nautilus-3-30-improvements-new-path-bar)

* [https://medium.com/@alex285/gnome-3-30-preview-the-ux-changes-on-files-app-so-far-60dd97dd465e](https://medium.com/@alex285/gnome-3-30-preview-the-ux-changes-on-files-app-so-far-60dd97dd465e)