---
layout: post
title: "Mencoba Microsoft Edge Dev Pada openSUSE Leap"
description: "Mencoba Microsoft Edge Dev Pada openSUSE Leap"
comments: false
keywords: "Microsoft Edge, openSUSE Leap"
---
Panduan ini dicoba pada openSUSE Leap 15.2. Langkahnya:

1. Tambahkan kunci dari Microsoft

	```
	sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
	```

2. Tambahkan repositori Microsoft Edge Dev

	```
	sudo zypper ar https://packages.microsoft.com/yumrepos/edge microsoft-edge-dev
	```

3. Segarkan repositori

	```
	sudo zypper refresh
	```

4. Pasang Microsoft Edge Dev

	```
	sudo zypper install microsoft-edge-dev
	```

Selamat mencoba!


