---
layout: post
title: "BlankOn Uluwatu dan Flatpak"
description: "BlankOn Uluwatu dan Flatpak"
comments: false
keywords: "Flatpak, BlankOn"
---

[BlankOn](https://www.blankonlinux.or.id/), distro yang mana saya sempat menjadi pengembangnya, akan merilis edisi terbaru, "konon" akan rilis berbarengan dengan acara [LibreOffice Conference Indonesia 2018](http://libreoffice.id). Belakangan ini sering ngoprek [flatpak](https://flatpak.org/) gara-gara [Endless OS](https://endlessos.com/), pas ikutan [hackfest resep](https://blog.kukuh.syafaat.id/2018/GNOME-Recipes-Hackfest/) tiba-tiba terlintas untuk menanyakan apakah paket `flatpak` [dapat disertakan](https://groups.google.com/forum/#!topic/BlankOn-dev/4GwfxnTLtPQ) pada BlankOn Uluwatu atau tidak. Ternyata pada tanggal [jahitan tanggal 1 Maret](https://groups.google.com/forum/#!topic/BlankOn-dev/a7lLCKGsOTQ) paket `flatpak` sudah masuk. Karena penasaran, maka saya mencobanya di BlankOn.

Dengan perintah `flatpak list` dapat dipastikan paket `flatpak` sudah terpasang tetapi belum ada remote yang terpasang
![https://gitlab.com/cho2/blog-images/raw/master/2018-03-09/1.png](https://gitlab.com/cho2/blog-images/raw/master/2018-03-09/1.png) 

Saya mencoba memasang [Spotify](https://www.spotify.com/) dari [flathub](https://flathub.org/) dengan perintah `flatpak install --from https://flathub.org/repo/appstream/com.spotify.Client.flatpakref`
![https://gitlab.com/cho2/blog-images/raw/master/2018-03-09/2.png](https://gitlab.com/cho2/blog-images/raw/master/2018-03-09/2.png) 

Kemudian masukkan kata sandi root untuk mengkonfigurasikan remote baru
![https://gitlab.com/cho2/blog-images/raw/master/2018-03-09/3.png](https://gitlab.com/cho2/blog-images/raw/master/2018-03-09/3.png) 

Pilih ya untuk memasang remote flathub
![https://gitlab.com/cho2/blog-images/raw/master/2018-03-09/4.png](https://gitlab.com/cho2/blog-images/raw/master/2018-03-09/4.png) 

Tunggu hingga proses unduh selesai. Ketik `flatpak list` maka terlihat bahwa Spotify sudah terpasang dan dua runtime lainnya
![https://gitlab.com/cho2/blog-images/raw/master/2018-03-09/5.png](https://gitlab.com/cho2/blog-images/raw/master/2018-03-09/5.png) 

Coba menjalankan Spotify dari flatpak dengan perintah `flatpak run com.Spotify.Client`
![https://gitlab.com/cho2/blog-images/raw/master/2018-03-09/6.png](https://gitlab.com/cho2/blog-images/raw/master/2018-03-09/6.png) 

Voila, Spotify berjalan
![https://gitlab.com/cho2/blog-images/raw/master/2018-03-09/7.png](https://gitlab.com/cho2/blog-images/raw/master/2018-03-09/7.png) 

Coba mencari Spotify dari Manokwari, tetapi belum muncul dalam menu
![https://gitlab.com/cho2/blog-images/raw/master/2018-03-09/8.png](https://gitlab.com/cho2/blog-images/raw/master/2018-03-09/8.png) 

Jalankan `pkill manokwari` dan Spotify akan muncul di Manokwari
![https://gitlab.com/cho2/blog-images/raw/master/2018-03-09/9.png](https://gitlab.com/cho2/blog-images/raw/master/2018-03-09/9.png) 

Spotify berada dalam menu Suara & Video
![https://gitlab.com/cho2/blog-images/raw/master/2018-03-09/10`.png](https://gitlab.com/cho2/blog-images/raw/master/2018-03-09/10.png) 