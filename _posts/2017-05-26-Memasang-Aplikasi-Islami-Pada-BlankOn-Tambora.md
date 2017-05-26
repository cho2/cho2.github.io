---
layout: post
title: "Memasang Aplikasi Islami Pada BlankOn Tambora"
description: "Memasang Aplikasi Islami Pada BlankOn Tambora"
comments: false
keywords: "BlankOn, Tambora, Sajadah"
---

![http://panduan.blankonlinux.or.id/wp-content/uploads/2017/05/VirtualBox_Tambora_25_05_2017_16_00_38.png](http://panduan.blankonlinux.or.id/wp-content/uploads/2017/05/VirtualBox_Tambora_25_05_2017_16_00_38.png)

Dalam rangka menyambut bulan Ramadhan, BlankOn biasanya menerbitkan <a href="http://sajadah.blankonlinux.or.id/">BlankOn Sajadah</a>. Versi terakhir yang terbit adalah BlankOn Sajadah 8.0. Versi sebelumnya yang pernah terbit dapat Anda tilik pada tautan <a href="http://cdimage.blankonlinux.or.id/blankon/blankon-sajadah/rilis/">http://cdimage.blankonlinux.or.id/blankon/blankon-sajadah/rilis/</a>. Nasib Sajadah selanjutnya dapat Anda baca pada <a href="https://groups.google.com/forum/#!searchin/BlankOn-dev/sajadah|sort:date/blankon-dev/QuxWVVfa1Gs/NoOaq6yQQcsJ">Milis Pengembangan BlankOn</a>.

Nah, menyambut Ramadhan 1438 H, bagi yang rindu dengan BlankOn Sajadah, tidak ada salahnya memasang aplikasi Islami yang terdapat pada lumbung BlankOn.

Paska insiden pada lumbung BlankOn, maka saya menggunakan lumbung <a href="http://repo.ridon.id/">Ridon</a> sebagai berikut.
<pre>## Compatible Repository BlankOn X Tambora
deb http://repo.ridon.id/blankon tambora main restricted extras extras-restricted
deb-src http://repo.ridon.id/blankon tambora main restricted extras extras-restricted

## Compatible Repository BlankOn X Tambora Updates
deb http://repo.ridon.id/blankon tambora-updates main restricted extras extras-restricted
deb-src http://repo.ridon.id/blankon tambora-updates main restricted extras extras-restricted

## Compatible Repository BlankOn X Tambora Security
deb http://repo.ridon.id/blankon tambora-security main restricted extras extras-restricted
deb-src http://repo.ridon.id/blankon tambora-security main restricted extras extras-restricted
</pre>
Buka terminal dan salin tempel saja perintah berikut
<pre>sudo apt install zekr hijra-applet monajat othman thawab stellarium zacalc nawala noor minbar hadis-web qioo islamic-menus folder-islami elforkane elkirtasse blankon-sajadah-wallpapers blankon-wallpapers-sajadah-rote eclipse libwebkitgtk-1.0-0
</pre>
Bagi Anda yang belum pernah mengetahui apa itu BlankOn Sajadah, saya menemukan <a href="https://groups.google.com/forum/#!searchin/BlankOn-dev/sajadah|sort:date/blankon-dev/UATqrPKkjqo/GOGcRlhz56UJ">salindia</a> dari Pak <a href="https://twitter.com/utianayuba">Utian Ayuba</a> yang keren itu :D. Silakan unduh <a href="http://www.google.com/url?q=http%3A%2F%2Fdev.blankonlinux.or.id%2Fattachment%2Fwiki%2FPemasaran%2FPresentasiBlankon%2FBlankOn_Sajadah_6.1_Utian.odp%3Fformat%3Draw&amp;sa=D&amp;sntz=1&amp;usg=AFQjCNE63ZC6iWEZqoICkAOcGpB9B09EvA">disini</a>.

Ternyata saja juga pernah menyumbangkan gambar latar untuk BlankOn Sajadah versi 7.0, ya tidak bagus-bagus amat sebenarnya. Bagi yang penasaran, silakan unduh <a href="https://groups.google.com/forum/#!searchin/BlankOn-dev/sajadah|sort:date/blankon-dev/hePCSN23uoY/HyOsW0eaD9sJ">disini</a>.

Akhir kata, selamat menunaikan ibadah puasa.