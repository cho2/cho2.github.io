---
layout: post
title: "Memasang GNOME Web Canary"
description: "Memasang GNOME Web Canary"
comments: false
keywords: "GNOME Web"
---

![https://gitlab.com/cho2/blog-images/-/raw/master/2021-08-10/gnome-web-canary.png](https://gitlab.com/cho2/blog-images/-/raw/master/2021-08-10/gnome-web-canary.png)

[GNOME Web](https://wiki.gnome.org/Apps/Web), dahulu dikenal juga dengan nama Epiphany. Sekarang GNOME Web memiliki versi Canary dimana pengguna dapat menjajal fitur yang belum tersedia pada versi stabil. GNOME Web Canary dapat dipasang menggunakan Flatpak dengan cara berikut.

```
flatpak --user remote-add --if-not-exists webkit https://software.igalia.com/flatpak-refs/webkit-sdk.flatpakrepo
flatpak --user install https://nightly.gnome.org/repo/appstream/org.gnome.Epiphany.Canary.flatpakref
```
Selamat mencoba!

Referensi:
- https://news.itsfoss.com/gnome-web-canary/
- https://base-art.net/Articles/introducing-the-gnome-web-canary-flavor/