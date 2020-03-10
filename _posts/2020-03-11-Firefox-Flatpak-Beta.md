---
layout: post
title: "Mencoba Firefox Flatpak Beta"
description: "Mencoba Firefox Flatpak Beta"
comments: false
keywords: "Flatpak Firefox"
---

![https://gitlab.com/cho2/blog-images/-/raw/master/2020-03-11/firefox-flatpak-beta.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-03-11/firefox-flatpak-beta.png)

Kabar gembira bagi pengguna [Flatpak](https://flatpak.org/) dan [Firefox](https://www.mozilla.org), Firefox Flatpak akan tersedia dalam waktu dekat, kemungkinan di versi 75.0.

Sebelumnya, Firefox Flatpak hanya tersedia versi Nightly dan Developer Edition yang repositorinya disediakan secara [unofficial](https://firefox-flatpak.mojefedora.cz/) oleh RedHat. Selain itu,  [Endless](https://endlessos.com/) juga menyediakan [Firefox Flatpak](https://community.endlessos.com/t/how-to-install-firefox-on-endless-os-3/665) yang hanya tersedia di Endless. Penulis juga pernah membangun [Firefox Flatpak](https://github.com/cho2/org.mozilla.Firefox) beserta [reponya](https://github.com/cho2/firefox-flatpak-repo) untuk penggunaan pribadi.

Cara memasang Firefox Flatpak Beta yaitu:

* Pastikan paket `flatpak` sudah terpasang
* Tambahkan repo `flathub-beta` jika belum ada
  ```
  flatpak remote-add flathub-beta https://flathub.org/beta-repo/flathub-beta.flatpakrepo
  ```
* Pasang Firefox dari `flathub-beta`
  ```
  flatpak install flathub-beta org.mozilla.firefox
  ```

Jika menemukan kutu, jangan lupa laporkan. Selamat mencoba!

Referensi:

* [Mozilla makes Firefox Beta available on Flathub](https://eischmann.wordpress.com/2020/03/10/mozilla-makes-firefox-beta-available-on-flathub/)
* [Bugzilla Firefox](https://bugzilla.mozilla.org/show_bug.cgi?id=1441922#c59)
* [An Official Firefox Flatpak is on the Way](https://www.omgubuntu.co.uk/2020/03/official-firefox-flatpak-app)