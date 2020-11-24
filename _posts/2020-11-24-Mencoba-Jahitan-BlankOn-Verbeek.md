---
layout: post
title: "Mencoba Jahitan BlankOn Verbeek"
description: "Mencoba Jahitan BlankOn Verbeek"
comments: false
keywords: "BlankOn"
---

Ya, sesuai judul, BlankOn sudah memulai lagi pengembangannya. Rasanya kangen juga dengan BlankOn. Meskipun sudah jadi [pensiunan](https://kabarlinux.id/2017/enam-pengembang-undur-diri-dari-tim-pengembang-blankon-terima-kasih-atas-kerja-kerasnya/), tetapi saya masih berkontribusi di beberapa proyek hulu, harapannya kontribusi tersebut bermanfaat BlankOn.

<blockquote class="twitter-tweet"><p lang="in" dir="ltr">Jahitan Verbeek pertama yang dapat dipasang ke komputer. 🥳🥳🥳<br><br>Jahitan harian 20201123-1 dari <a href="https://t.co/U19USX8BVW">https://t.co/U19USX8BVW</a> cabang master telah terbit. Berkas citra dapat diunduh di <a href="https://t.co/yc1TRUqNw8">https://t.co/yc1TRUqNw8</a></p>&mdash; BlankOn (@BlankOnLinux) <a href="https://twitter.com/BlankOnLinux/status/1330888111987978242?ref_src=twsrc%5Etfw">November 23, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

Jahitan BlankOn Verbeek yang sudah dapat dipasang sudah terbit. Mari kita coba.

* Unduh dari tautan yang sudah disediakan
    ```
    wget -c https://cdimage.blankonlinux.or.id/blankon/jahitan-harian/20201123-1/20201123-1-live-image-amd64.hybrid.iso
    ```
* Boot iso yang sudah diunduh pada mesin virtual favorit Anda (misal menggunakan Virtualbox). Kalau Anda memiliki mesin yang nganggur, tidak ada salahnya mencoba di mesin beneran. Kali ini saya menggunakan [GNOME Boxes](https://wiki.gnome.org/Apps/Boxes).

* Silakan nikmati video berikut

    <iframe width="560" height="315" src="https://www.youtube.com/embed/ZUvYLtjz1SM" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

* Kesimpulan:
    - Destop yang digunakan Xfce
    - Pemasang (*installer*) menggunakan Calamares
    - Branding masih menggunakan Debian Bullseye/Sid

* Tips
    * Unduh juga berkas `zsync`. Contoh 
        ```
        https://cdimage.blankonlinux.or.id/blankon/jahitan-harian/20201123-1/20201123-1-live-image-amd64.hybrid.iso.zsync
        ``` 
        Sedikit penjelasan tentang `zsync`, kita tidak perlu mengunduh keseluruhan berkas iso selanjutnya (dengan kata lain, kita hanya perlu mengunduh perubahannya saja/delta). Menarik bukan?

        Lebih lanjut, bisa membaca tulisan [berikut](https://ha.hn.web.id/2016/10/16/unduh-berkas-iso-dengan-zsync/). Jangan lupa juga untuk memasang paket `zsync` pada distro kesayangan Anda. (Disaya, cukup dengan menggetikkan `sudo zypper in zsync` di terminal).

        Perintah untuk menjalankan `zsync` adalah sebagai berikut
        ```
        zsync 20201123-1-live-image-amd64.hybrid.iso.zsync
        ```

O iya, BlankOn juga mengadakan urunan, silakan berdonasi pada tautan [berikut](https://kitabisa.com/campaign/urunanpengembanganblankon).

Selamat ngoprek!