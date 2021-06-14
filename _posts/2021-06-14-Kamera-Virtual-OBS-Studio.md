---
layout: post
title: "Kamera Virtual OBS Studio"
description: "Kamera Virtual OBS Studio"
comments: false
keywords: "OBS Studio, Flatpak"
---

Sempat berpikir, bagaimana caranya saat rapat daring, kamera yang menyala bukan kamera pada komputer, melainkan gambar atau video lainnya. Setelah bertanya pada mbah gugel, ternyata ada teknologi yang namanya Kamera Virtual (*Virtual Camera*). 

Sebelumnya, kamera virtual ini merupakan pengaya (*plugin*) pada OBS Studio. Kabar gembiranya, sejak versi [26.0.0](https://github.com/CatxFish/obs-virtual-cam/blob/master/readme.MD), pengaya ini sudah jadi bawaan (*default*).

Hal berikutnya yang perlu dilakukan adalah memasang `v4l2loopback`. Karena saat ini saya menggunakan [MicroOS](http://microos.opensuse.org/) yang berbasis [Tumbleweed](https://en.opensuse.org/Portal:Tumbleweed), maka cari dulu paketnya dengan `zypper search v4l2loopback`. Hasilnya muncul berikut.

```
S  | Name                     | Summary                                         | Type
---+--------------------------+-------------------------------------------------+------
   | v4l2loopback-autoload    | Autoload driver for V4L2 loopback devices       | paket
   | v4l2loopback-kmp-default | A kernel module to create V4L2 loopback devices | paket
   | v4l2loopback-kmp-pae     | A kernel module to create V4L2 loopback devices | paket
   | v4l2loopback-utils       | Utils for V4L2 loopback devices                 | paket
```
Selanjutnya pasang paket berikut (Di MicroOS, saya masuk dulu ke `transactional-update shell`).

```
sudo zypper in v4l2loopback-utils v4l2loopback-kmp-default v4l2loopback-autoload
```

Untuk distribusi Linux lainnya, harap menyesuaikan ya, kuncinya ada di paket bernama `v4l2loopback`. 

Jika sudah, saat menyalakan OBS Studio, pastikan ada opsi "Start Virtual Camera" seperti gambar berikut.

![https://gitlab.com/cho2/blog-images/-/raw/master/2021-06-14/obs-start.png](https://gitlab.com/cho2/blog-images/-/raw/master/2021-06-14/obs-start.png)

Pastikan nama kameranya adalah "OBS Virtual Camera" atau sejenisnya. Hasil uji coba di beberapa aplikasi sebagai berikut.

* Jitsi (via peramban Google Chrome Flatpak)

  ![https://gitlab.com/cho2/blog-images/-/raw/master/2021-06-14/jitsi.png](https://gitlab.com/cho2/blog-images/-/raw/master/2021-06-14/jitsi.png)

* Google Meet (via peramban Google Chrome Flatpak)

  ![https://gitlab.com/cho2/blog-images/-/raw/master/2021-06-14/google-meet.png](https://gitlab.com/cho2/blog-images/-/raw/master/2021-06-14/google-meet.png)

* Zoom

  ![https://gitlab.com/cho2/blog-images/-/raw/master/2021-06-14/zoom.png](https://gitlab.com/cho2/blog-images/-/raw/master/2021-06-14/zoom.png
  )

* Microsoft Teams

  ![https://gitlab.com/cho2/blog-images/-/raw/master/2021-06-14/ms-teams.png](https://gitlab.com/cho2/blog-images/-/raw/master/2021-06-14/ms-teams.png)


Contoh penggunaannya, pada OBS Studio, misal saya memasang gambar bakso sebagai berikut.

![https://gitlab.com/cho2/blog-images/-/raw/master/2021-06-14/obs-bakso.png](https://gitlab.com/cho2/blog-images/-/raw/master/2021-06-14/obs-bakso.png)

Maka nanti di ruangan rapat (contoh ini pada Google Meet) akan tampil sebagai berikut. Dengan mode kamera menyala, kamera akan menampilkan gambar bakso alih-alih muka saya.

![https://gitlab.com/cho2/blog-images/-/raw/master/2021-06-14/screenshot-meet.google.com-bakso.png](https://gitlab.com/cho2/blog-images/-/raw/master/2021-06-14/screenshot-meet.google.com-bakso.png)

Catatan: Jika gambar yang tampil terbalik, maka pada OBS Studio pada 
bagian Sources > Image, klik kanan, pilih Transform, lalu pilih Flip Horizontal.

Sebagai informasi tambahan, semua aplikasi di atas menggunakan Flatpak.
* [OBS Studio](https://flathub.org/apps/details/com.obsproject.Studio)
* [Zoom](https://flathub.org/apps/details/us.zoom.Zoom)
* [MS Teams](https://flathub.org/apps/details/com.microsoft.Teams)

Untuk peramban, saya menggunakan Google Chrome Flatpak yang saya bangun (*build*) sendiri, bukan Google Chrome di `flathub-beta`. Seharusnya di peramban apapun bisa jalan dengan baik.

Selamat mencoba!

---

Referensi: 
* [Virtual Camera di OBS Studio untuk Linux](https://diskusi.tech/ariya/virtual-camera-di-obs-studio-untuk-linux-9gm)
* [https://opensource.com/article/20/8/obs-virtual-webcam](https://opensource.com/article/20/8/obs-virtual-webcam)