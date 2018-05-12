---
layout: post
title: "Chrome Remote Desktop pada openSUSE Leap"
description: "Chrome Remote Desktop pada openSUSE Leap"
comments: false
keywords: "Google Chrome, openSUSE, Leap"
---

Ketika memasang pengaya Chrome Remote Desktop dengan Google Chrome, biasanya Chrome akan mengunduh sebuah paket bernama `chrome-remote-desktop`. Sayangnya yang diunduh adalah `chrome-remote-desktop_current_amd64.deb`, padahal yang dibutuhkan adalah berkas tersebut dengan ekstensi `.rpm`. Maka kita perlu mengubah paket tersebut dari `.deb` menjadi `.rpm`.

* Pasang `alien` dengan perintah berikut
```
zypper in https://download.opensuse.org/repositories/utilities/openSUSE_Leap_42.3/x86_64/alien-8.88-3.1.x86_64.rpm`
```
* Pasang juga `rpmbuild` dengan perintah berikut
```
sudo zypper in rpmbuild
```
* Jalankan `alien`
```
sudo alien -c -r chrome-remote-desktop_current_amd64.deb
```
* Nanti hasilnya berupa berkas `chrome-remote-desktop-66.0.3359.12-2.x86_64.rpm` (dalam contoh ini). Pasang paket tersebut dengan perintah berikut
```
sudo zypper in chrome-remote-desktop-66.0.3359.12-2.x86_64.rpm
```
Selamat mencoba