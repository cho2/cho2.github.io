---
layout: post
title: "Konversi Berkas Markdown ke PDF dengan Pandoc"
description: "Konversi Berkas Markdown ke PDF dengan Pandoc"
comments: false
keywords: "Pandoc, Markdown. PDF"
---

Jadi tadi pagi ceritanya perlu untuk mengkonversikan berkas markdown ke PDF. Setelah menghindari [konversi daring dengan unggah berkas](https://www.markdowntopdf.com/), coba dengan [menempel langsung](https://md2pdf.netlify.com/) namun hasilnya kurang sesuai. Coba dengan salah satu [paket dari npm](https://www.npmjs.com/package/markdown-pdf) ternyata galat. Akhirnya menemukan catatan [ini](https://gist.github.com/justincbagley/ec0a6334cc86e854715e459349ab1446).

Pada openSUSE Tumbleweed, pasang dengan perintah
```
sudo zypper in pandoc texlive-latex-bin-bin
```

Lalu jalankan pandoc untuk konversi berkas seperti berikut
```
pandoc berkas.md -s -o berkas.pdf
```

Selamat mencoba!