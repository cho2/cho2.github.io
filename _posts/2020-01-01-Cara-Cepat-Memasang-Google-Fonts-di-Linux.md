---
layout: post
title: "Cara Cepat Memasang Google Fonts di Linux"
description: "Cara Cepat Memasang Google Fonts di Linux"
comments: false
keywords: "Google Fonts"
---

* Pastikan Anda sudah memasang `git` pada sistem Anda
* Masuk ke direktori `~/.local/share/fonts/`
  ```
  cd ~/.local/share/fonts/
  ```
    * Jika direktori `~/.local/share/fonts/` belum ada, maka buat dahulu
        ```
        mkdir ~/.local/share/fonts/
        ```
* Klon Google Fonts
  ```
  git clone git@github.com:cho2/google-fonts.git
  ```
* Voila, Google Fonts sudah terpasang
* Jika nanti ada pemutakhiran dari Google Fonts, cukup masuk ke direktori `~/.local/share/fonts/google-fonts` dan tarik pemutakhiran tersebut dari git

Selamat mencoba!

NB: Percobaan ini dilakukan di openSUSE Tumbleweed