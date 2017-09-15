---
layout: post
title: "Memasang openSUSE Tumbleweed pada Lenovo Thinkpad X1 Carbon"
description: "Memasang openSUSE Tumbleweed pada Lenovo Thinkpad X1 Carbon"
comments: false
keywords: "openSUSE, Tumbleweed"
---

![https://scontent.fjkt1-1.fna.fbcdn.net/v/t1.0-9/21742802_10209928216738924_2843600015354648774_n.jpg?oh=3075be1c1feb3cfd245131956db27c29&oe=5A14944B](https://scontent.fjkt1-1.fna.fbcdn.net/v/t1.0-9/21742802_10209928216738924_2843600015354648774_n.jpg?oh=3075be1c1feb3cfd245131956db27c29&oe=5A14944B)

Jadi ceritanya mumpung [GNOME 3.26](https://www.gnome.org/news/2017/09/gnome-3-26-released/) baru rilis dan bosen dengan Debian Sid, juga kerjaan lagi nunggu umpan lambung dari pemrogram yang tadi sore hampir gagal masak Indomie gara-gara gas habis serta kantor lagi beberes untuk acara [Kerja Bakti GCompris](https://www.facebook.com/photo.php?fbid=1870140546344409&set=a.234793976545749.66457.100000454449972&type=3&theater), maka sore ini saya memutuskan memasang openSUSE Tumbleweed pada [Lenovo Thinkpad X1 Carbon](https://www.cnet.com/products/lenovo-thinkpad-x1-carbon-3rd-generation-intel-core-i7-5600u-2-60ghz-1600mhz-4mb/specs/) yang beli borongan 5 biji, 3 bji diantaranya sudah masuk servisan.

Saya mengunduh berkas iso DVD [openSUSE Tumbleweed](http://download.opensuse.org/tumbleweed/iso/) Snapshot tanggal [14 September](http://download.opensuse.org/tumbleweed/iso/openSUSE-Tumbleweed-DVD-x86_64-Snapshot20170913-Media.iso) yang sudah memuat GNOME 3.26. Saya memasang dengan mode enkripsi penuh pada swap dan root, jangan lupa untuk memformat juga partisi EFI agar komputer dapat boot. O iya, entah mengapa sejak zaman [memasang openSUSE Tumbleweed pada MacBookAir](http://blog.kukuh.syafaat.id/2016/openSUSE-Tumbleweed-MacBook-Air/) (yang belakangan saya pasang Leap), touchpad selalu tidak dapat digunakan pada installer. Jadi, selalu sediakan tetikus eksternal saat memasang openSUSE.  

Setelah selesai memasang, *wireless* langsung terdeteksi. Berikutnya adalah memasang perangkat lunak yang dibutuhkan sehari-hari.
* Google Chrome
* Mozilla Thunderbird
* git
* nano
* htop
* zsh (beserta [oh my zsh](https://github.com/robbyrussell/oh-my-zsh) dengan tema agnoster)
* Oracle Virtualbox
* Mendeley Desktop (beserta plugin untuk LibreOffice)
* Microsoft Visual Studio Code
* Tema gtk [Arc](https://software.opensuse.org/download.html?project=home%3AHorst3180&package=arc-theme)
* Poedit
* Flatpak
* Spotify

Spotify dipasang lewat Flatpak, nanti coba ditulis lain waktu. 
