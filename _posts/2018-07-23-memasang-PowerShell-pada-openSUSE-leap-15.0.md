---
layout: post
title: "Memasang PowerShell pada openSUSE Leap 15.0"
description: "Memasang PowerShell pada openSUSE Leap 15.0"
comments: false
keywords: "openSUSE, Leap, snap, powershell"
---

Sudahkah Anda tahu bahwa [PowerShell](https://snapcraft.io/powershell) dapat dipasang pada disribusi Linux kesayangan Anda melalui Snap?
Berikut ini cara memasangnya pada openSUSE Leap 15.0.

* Pasang repo snap

	```
	sudo zypper addrepo --refresh http://download.opensuse.org/repositories/system:/snappy/openSUSE_Leap_15.0/ snappy
	```

* Pasang snap

	```
	sudo zypper install snapd
	```

* Aktifkan soket pada systemd yang dibutuhkan oleh snap

	```
	sudo systemctl enable --now snapd.socket
	```

* Pasang PowerShell

	```
	sudo snap install powershell --classic
	```

* Jalankan PowerShell

    ```
    snap run powershell
    ```