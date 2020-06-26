---
layout: post
title: "Menjalankan Swagger Editor dengan Docker"
description: "Menjalankan Swagger Editor dengan Docker"
comments: false
keywords: "Swagger, Docker"
---

Jadi ceritanya, ada kebutuhan membaca dokumentasi, supaya mudah membacanya  maka dokumentasi tersebut dibuka Swagger editor. Alih-alih menggunakan `npm`, Swagger editor dijalankan di lokal dengan menggunakan Docker.

Tahapannya:

* Pastikan sudah memasang `docker` dan service-nya jalan
* Tarik image `swagger-editor`
  ```
  docker pull swaggerapi/swagger-editor
  ```
* Jalankan `swagger-editor` di lokal
  ```
  docker run -d -p 80:8080 swaggerapi/swagger-editor
  ```
* Buka alamat `http://localhost` di peramban kesayangan Anda
* Swagger editor telah siap

Selamat mencoba!

Referensi: [https://github.com/swagger-api/swagger-editor](https://github.com/swagger-api/swagger-editor)