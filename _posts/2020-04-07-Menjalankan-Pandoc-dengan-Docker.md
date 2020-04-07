---
layout: post
title: "Menjalankan Pandoc dengan Docker"
description: "Menjalankan Pandoc dengan Docker"
comments: false
keywords: "Pandoc, Docker"
---

[Postingan sebelumnya tentang Pandoc](https://blog.kukuh.syafaat.id/2020/Konversi-Berkas-Markdown-ke-PDF-dengan-Pandoc/) dijalankan pada [openSUSE Tumbleweed](https://software.opensuse.org/distributions/tumbleweed). Karena hari ini kebetulan sedang pegang komputer dengan [openSUSE Leap](https://software.opensuse.org/distributions/leap), maka coba mengikuti panduan pada postingan tersebut dan hasilnya galat.

Coba mampir ke halaman [cara memasang Pandoc](https://pandoc.org/installing.html), ada bagian Docker. Mari kita coba saja. Pastikan Anda sudah memasang Docker dan servicenya jalan. Pada halaman tersebut, terdapat dua macam image Docker, yaitu:

> The `pandoc/core` image contains pandoc and pandoc-citeproc.

> The `pandoc/latex` image also contains the minimal LaTeX installation needed to produce PDFs using pandoc.

Saya ambil yang kedua karena kebutuhan untuk membuat PDF. Langkahnya

* Tarik image Docker `pandoc/latex`
    ```
    docker pull pandoc/latex
    ```
* Jalankan perintah sederhana untuk konversi berkas markdown ke PDF.
    ```
    docker run --rm --volume "`pwd`:/data" --user `id -u`:`id -g` pandoc/latex berkas.md -o berkas.pdf
    ```

Voila! 

Selamat mencoba!

--

Catatan:

* Yang belum dicoba, menjalankan dengan menggunakan `podman` alih-alih `docker`
* Bonus:
    * Ekspor ke berkas PDF dengan tampilan *landscape*
        ```
        docker run --rm --volume "`pwd`:/data" --user `id -u`:`id -g` pandoc/latex berkas.md -V geometry:landscape -f markdown -o berkas.pdf
        ```
    * Ekspor ke berkas PDF dengan pengaturan margin
        ```
        docker run --rm --volume "`pwd`:/data" --user `id -u`:`id -g` pandoc/latex berkas.md -V geometry:"top=2cm, bottom=1.5cm, left=1cm, right=1cm" -o berkas.pdf
        ```