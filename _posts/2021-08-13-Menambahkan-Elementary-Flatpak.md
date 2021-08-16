---
layout: post
title: "Menambahkan Elementary Flatpak Remote"
description: "Menambahkan Elementary Flatpak Remote"
comments: false
keywords: "Flatpak, Elementary OS"
---

Elementary OS 6 Odin baru dirilis. Tahukah Anda bahwa AppCenter (Pusat Aplikasi) sekarang berisi aplikasi yang sudah dikurasi dan dikemas dalam 
format Flatpak? Daftar antriannya dapat Anda simak [disini](https://github.com/elementary/appcenter-reviews/pulls). Daftar aplikasi yang sudah masuk, dapat Anda lihat [disini](https://github.com/elementary/appcenter-reviews/tree/main/applications). AppCenter (Pusat Aplikasi) juga daapt diakses melalui antarmuka web pada [https://appcenter.elementary.io/](https://appcenter.elementary.io/).

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Just approved the 20th Flatpak app in the new AppCenter. 195 to go!</p>&mdash; Daniel Foré (@DanielFore) <a href="https://twitter.com/DanielFore/status/1425573230689931267?ref_src=twsrc%5Etfw">August 11, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

Anda dapat memeriksa pada sistem Elementary OS Anda dengan perintah berikut pada terminal.
1. `flatpak remotes` untuk mengetahui remote apa saja yang digunakan di Elementary OS.

    ![https://gitlab.com/cho2/blog-images/-/raw/master/2021-08-13/1.png](https://gitlab.com/cho2/blog-images/-/raw/master/2021-08-13/1.png)

1.  `flatpak remote-ls appcenter` untuk mengetahui aplikasi mana saja yang dapat dipasang melalui remote milik elementary ini.

    ![https://gitlab.com/cho2/blog-images/-/raw/master/2021-08-13/2.png](https://gitlab.com/cho2/blog-images/-/raw/master/2021-08-13/2.png)

1. Anda dapat juga mengetahui informasi lebih lanjut remote `appcenter` ini seperti pada gambar berikut.

    ![https://gitlab.com/cho2/blog-images/-/raw/master/2021-08-13/3.png](https://gitlab.com/cho2/blog-images/-/raw/master/2021-08-13/3.png)

Flatpak Elementary OS ini memiliki alamat repo di [https://flatpak.elementary.io/](https://flatpak.elementary.io/). Kita dapat menambahkan remote ini pada sistem operasi lain selain Elementary OS. Jadi kita masih dapat memasang atau menggunakan aplikasi khas Elementary di sistem operasi lain. Caranya:

1. Tambahkan remote `elementary` seperti berikut (pada contoh ini, saya memasangnya di `--user` dan menggunakan nama `elementary` alih-alih `appcenter` agar mudah dikenali)
    ```
    flatpak remote-add elementary https://flatpak.elementary.io/repo.flatpakrepo --user
    ```
1. Jalankan perintah berikut untuk untuk mengetahui aplikasi mana saja yang dapat dipasang melalui remote `elementary` ini.     
    ```
    flatpak remote-ls elementary
    ```

    ![https://gitlab.com/cho2/blog-images/-/raw/master/2021-08-13/4.png](https://gitlab.com/cho2/blog-images/-/raw/master/2021-08-13/4.png)

1. Pasang salah satu aplikasi, contoh Palet
    ```
    flatpak install --user elementary com.github.cassidyjames.palette
    ```

    ![https://gitlab.com/cho2/blog-images/-/raw/master/2021-08-13/5.png](https://gitlab.com/cho2/blog-images/-/raw/master/2021-08-13/5.png)

1. Jalankan aplikasi tersebut

    ![https://gitlab.com/cho2/blog-images/-/raw/master/2021-08-13/6.png](https://gitlab.com/cho2/blog-images/-/raw/master/2021-08-13/6.png)


Selamat mencoba!            
