---
layout: post
title: "Memasang Akira"
description: "Memasang Akira"
comments: false
keywords: "Flatpak, Akira"
---

Ada dua cara untuk memasang [Akira](https://github.com/akiraux/Akira) melalui Flatpak

# Flathub Beta

Seperti dijelaskan pada [github-nya Akira](https://github.com/akiraux/Akira#flathub-beta), pengguna dapat memasang menggunakan remote `flathub-beta`

```
flatpak remote-add flathub-beta https://flathub.org/beta-repo/flathub-beta.flatpakrepo
flatpak install akira
```

# Elementary

Masih merupakan kelanjutan dari pos [Menambahkan Elementary Flatpak Remote](https://blog.kukuh.syafaat.id/2021/Menambahkan-Elementary-Flatpak/), Akira ternyata sudah tersedia juga pada [AppCenter-nya Elementary](https://appcenter.elementary.io/com.github.akiraux.akira/). Dengan menggunakan cara pada pos sebelumnya, cukup jalankan

```
flatpak remote-add elementary https://flatpak.elementary.io/repo.flatpakrepo --user
flatpak install akira
```

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">You don&#39;t need to be on elementary to try shiny brand new elementary 6 and akira:<br><br>$ flatpak remote-add --if-not-exists --system elementary-appcenter <a href="https://t.co/Hsxut7vWks">https://t.co/Hsxut7vWks</a><br>$ flatpak install akira<a href="https://twitter.com/akiraux?ref_src=twsrc%5Etfw">@akiraux</a> <a href="https://twitter.com/FlatpakApps?ref_src=twsrc%5Etfw">@FlatpakApps</a> <a href="https://twitter.com/elementary?ref_src=twsrc%5Etfw">@elementary</a></p>&mdash; Alberto Fanjul (@albfanjul) <a href="https://twitter.com/albfanjul/status/1428676754663788547?ref_src=twsrc%5Etfw">August 20, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

Sampai saat pos ini ditulis, AKira masih dalam versi alpha 0.0.16.

![https://gitlab.com/cho2/blog-images/-/raw/master/2021-08-21/akira.png](https://gitlab.com/cho2/blog-images/-/raw/master/2021-08-21/akira.png)

Selamat mencoba!