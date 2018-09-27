---
layout: post
title: "Memasang Vivaldi Pada openSUSE"
description: "Memasang Vivaldi Pada openSUSE"
comments: false
keywords: "Vivaldi, openSUSE"
---

![https://vivaldi.com/wp-content/uploads/two-point-oh-hero-d.jpg](https://vivaldi.com/wp-content/uploads/two-point-oh-hero-d.jpg)

[Vivaldi 2.0](https://vivaldi.com/blog/vivaldi-2-0-your-browser-matters/) baru saja dirilis hari ini. Mari mencoba memasangnya pada openSUSE. Versi yang digunakan disini adalah openSUSE Leap 15.0.

* Unduh kunci publik Vivaldi
    ```
    wget https://repo.vivaldi.com/stable/linux_signing_key.pub
    ```
* Impor kunci publik Vivaldi
    ```
    sudo rpm --import linux_signing_key.pub
    ```
* Tambahkan repo Vivaldi
    ```
    sudo zypper ar https://repo.vivaldi.com/stable/rpm/x86_64/ Vivaldi
    ```
* Pasang Vivaldi
    ```
    sudo zypper in vivaldi-stable
    ```

Ada masalah dengan *codecs*? Silakan pasang dengan petunjuk [disini](https://gist.github.com/cho2/998073bb6567581846a09295ba1ae814).