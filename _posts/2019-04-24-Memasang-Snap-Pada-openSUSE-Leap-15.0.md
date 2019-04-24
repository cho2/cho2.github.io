---
layout: post
title: "Memasang Snap Pada openSUSE Leap 15.0"
description: "Memasang Snap Pada openSUSE Leap 15.0"
comments: false
keywords: "openSUSE, Snap"
---

Mari kita coba memasang snap pada openSUSE Leap. Berikut langkahnya.

* Tambahkan repo snap
    ```
    sudo zypper addrepo --refresh https://download.opensuse.org/repositories/system:/snappy/openSUSE_Leap_15.0 snappy
    ```

* Impor gpg secara otomatis
    ```
    sudo zypper --gpg-auto-import-keys refresh
    ```

* Pasang snap
    ```
    sudo zypper install snapd
    ```

* Anda perlu menyalakan ulang komputer atau keluar dan masuk ke user Anda lagi, atau jalankan `source /etc/profile` untuk menambahkan `/snap/bin` ke `PATH`

* Nyalakan servis snap

    ```
    sudo systemctl enable snapd
    sudo systemctl start snapd
    ```
* Snap siap digunakan

* Untuk pengguna Tumbleweed, perbedaannya terdapat pada langkah 1 dan 5.
    * Langkah 1, reponya adalah
        ```
        sudo zypper addrepo --refresh https://download.opensuse.org/repositories/system:/snappy/openSUSE_Tumbleweed snappy
        ```
    * Langkah 5, jalankan
        ```
        sudo systemctl enable snapd.apparmor
        sudo systemctl start snapd.apparmor
        ```

Selamat mencoba, have fun!