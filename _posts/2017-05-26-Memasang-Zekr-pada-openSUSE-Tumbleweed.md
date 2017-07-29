---
layout: post
title: "Memasang Zekr pada openSUSE Tumbleweed"
description: "Memasang Zekr pada openSUSE Tumbleweed"
comments: false
keywords: "openSUSE, Tumbleweed, Zekr"
---

<a href="http://zekr.org/quran/en/quran-for-linux">Zekr</a> merupakan salah satu aplikasi Al Quran yang bebas dan terbuka. Sampai dengan panduan ini ditulis, sudah mencapai versi 1.1.0.
<ul>
 	<li>Pada laman <a href="http://zekr.org/quran/en/quran-for-linux">http://zekr.org/quran/en/quran-for-linux</a>, pilih <a href="http://sourceforge.net/projects/zekr/files/Zekr/zekr-1.1.0/zekr-1.1.0-linux.tar.gz/download">Red Hat RPM Package</a>.</li>
 	<li>Lalu ekstrak, misalnya<em> /home/userAnda/zekr</em></li>
 	<li>Pasang paket <em>eclipse-swt </em>dan<em> libwebkitgtk-1_0-0 </em>, dengan menggunakan terminal, ketik
<pre>sudo zypper in eclipse-swt libwebkitgtk-1_0-0</pre>
</li>
 	<li>Masuk ke direktori Zekr, misalnya <em>/home/userAnda/zekr</em></li>
 	<li>Jalankan berkas <em>zekr.sh</em>, dengan menggunakan terminal, ketik
<pre>./zekr.sh</pre>
</li>
</ul>
<img src="https://opensuse.id/wp-content/uploads/2017/05/VirtualBox_Tumbleweed_25_05_2017_20_17_13.png" />
<ul>
 	<li>Untuk memasang translasi Bahasa Indonesia, unduh translasinya <a href="http://zekr.org/resources.html#translation">disini</a>. Untuk Bahasa Indonesia sendiri ada 3, yaitu:
<ul>
 	<li><a href="http://tanzil.ca/trans/id.indonesian.trans.zip">Departemen Agama</a></li>
 	<li><a href="http://tanzil.ca/trans/id.muntakhab.trans.zip">Quraish Shihab</a></li>
 	<li><a href="http://tanzil.ca/trans/id.jalalayn.trans.zip">Tafsir Jalalayn</a></li>
</ul>
</li>
 	<li>Sebagai contoh, panduan ini menggunakan translasi Departemen Agama. Berkas unduhan akan bernama <em>id.indonesian.trans.zip</em>.</li>
 	<li>Salin atau pindahkan berkas unduhan tersebut ke dalam direktori <em>/home/userAnda/zekr/res/text/trans</em>.</li>
 	<li>Jalankan Zekr, pilih menu <strong>View, </strong>lalu<strong> Translation, </strong>kemudian<strong> </strong>pilih<strong> [in] unknown</strong>.</li>
</ul>
<img src="https://opensuse.id/wp-content/uploads/2017/05/VirtualBox_Tumbleweed_25_05_2017_20_31_45.png" />
<ul>
 	<li>Translasi akan berubah ke Bahasa Indonesia sekarang.</li>
</ul>
<img src="https://opensuse.id/wp-content/uploads/2017/05/VirtualBox_Tumbleweed_25_05_2017_20_31_55.png" />
<div>
<div>Akhir kata, selamat menunaikan ibadah puasa.</div>
</div>