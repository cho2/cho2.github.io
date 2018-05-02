---
layout: post
title: "Chroot Pada Diska Terenkripsi"
description: "Chroot Pada Diska Terenkripsi"
comments: false
keywords: "chroot"
---

Buat catatan pribadi saja. Kebetulan openSUSE Tumbleweed saya terenkripsi. 

* Pertama, temukan partisi mana yang terenkripsi pada diska. Jalankan
```
lsblk -f
```
lalu cari yang `FSTYPE`-nya `crypto_LUKS`, misalnya `sda1`

* Lalu jalankan 
```
sudo cryptsetup open --type luks /dev/sda1 crypto_LUKS
```
dan masukkan sandi enkripsi diska Anda.

* Berturut-turut, jalankan
```
sudo mount /dev/mapper/crypto_LUKS /mnt
sudo mount /dev/sda2 /mnt/boot #bila sistem memiliki partisi /boot yang berbeda 
sudo mount /dev/sda3 /mnt/boot/efi #bila sistem boot dalam mode UEFI
sudo mount -t proc proc /mnt/proc
sudo mount -t sysfs sys /mnt/sys
sudo mount -o bind /dev /mnt/dev
sudo mount -o bind /run /mnt/run
sudo mount -t devpts pts /mnt/dev/pts/
cp /etc/resolv.conf /mnt/etc/resolv.conf
```

* Terakhir jalankan `chroot`
```
sudo chroot /mnt
```


[Referensi](https://forum.manjaro.org/t/how-to-chroot-into-an-encrypted-root-partition/10760) 
