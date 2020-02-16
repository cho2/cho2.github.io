---
layout: post
title: "Membersihkan Cache Flatpak"
description: "Membersihkan Cache Flatpak"
comments: false
keywords: "Flatpak"
---

Ketika menggunakan Flatpak dan sering memasang/memutakirkan, maka Flatpak akan meninggalkan cache yang ukurannya bisa sangat besar. Untuk membersihkannya jalankan
```
bash -c "! pgrep -x flatpak && rm -r /var/tmp/flatpak-cache-*"
```

Kita bisa juga membuatnya menjadi service systemd dan dapat berjalan setiap kali boot.

* Buat berkas `.service` dengan nama `clear_flatpak_cache.service` pada direktori `/lib/systemd/system` dengan isi berkas sebagai berikut
    ```
    [Unit]
    Description=Flatpak cache clearer

    [Service]
    ExecStart=bash -c "! pgrep -x flatpak && rm -r /var/tmp/flatpak-cache-*"

    [Install]
    WantedBy=multi-user.target
    ```
* Coba jalankan dengan
  ```
  sudo systemctl start clear_flatpak_cache
  ```

* Aktifkan agar berjalan setiap kali boot
  ```
  sudo systemctl enable clear_flatpak_cache
  ```

Selamat mencoba dan selamat ngoprek!

Referensi:

* [https://github.com/flatpak/flatpak/issues/1119](https://github.com/flatpak/flatpak/issues/1119)