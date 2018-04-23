---
layout: post
title: "Membuat Halaman Web Menjadi Aplikasi Destop"
description: "Membuat Halaman Web Menjadi Aplikasi Destop"
comments: false
keywords: "Web, NodeJs, Elctron, Nativefier"
---

Sedikit sulapan dari halaman GitHub [ini](https://github.com/jiahaog/nativefier) untuk membuat halaman web menjadi aplikasi destop. 

* Pastikan Anda sudah memasang NodeJS versi >= 4
* Pasang `nativefier`
```
npm install nativefier -g
```

* Penggunaan
```
nativefier --name "Some Awesome App" "http://url.com"
```
misalnya
```
nativefier --name "JOOX" "http://www.joox.com" 
```

* Hasilnya nanti ada pada folder home, lalu `joox-linux-x64`
* Berikut ini penampakannya

![https://gitlab.com/cho2/blog-images/raw/master/2018-04-23/joox.png](https://gitlab.com/cho2/blog-images/raw/master/2018-04-23/joox.png)

