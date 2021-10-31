---
layout: post
title: "Virtualbox di openSUSE MicroOS Desktop"
description: "Virtualbox di openSUSE MicroOS Desktop"
comments: false
keywords: "openSUSE, Virtualbox, MicroOS"
---

Apakah bisa memasang Virtualbox di openSUSE MicroOS Desktop? Bisa, pasti bisa.

# Memasang Virtualbox
```
$ sudo tukit execute bash
    # zypper ref
    # zypper in virtualbox-qt
    # usermod -a -G vboxusers <myuser>
    # exit
$ sudo reboot
```

# Memasang Extension Pack
Pastikan Anda sudah reboot ke snapshot terbaru setelah memasang Virtualbox pada langkah di atas.
```
$ sudo tukit execute bash
    # cd /tmp
    # LatestVirtualBoxVersion=$(wget -qO - https://download.virtualbox.org/virtualbox/LATEST-STABLE.TXT) && wget "https://download.virtualbox.org/virtualbox/${LatestVirtualBoxVersion}/Oracle_VM_VirtualBox_Extension_Pack-${LatestVirtualBoxVersion}.vbox-extpack"
    # VBoxManage extpack install --replace Oracle_VM_VirtualBox_Extension_Pack-${LatestVirtualBoxVersion}.vbox-extpack
    # exit
$ sudo reboot
```

Mudah bukan, selamat mencoba!

Have fun!

Sumber: [https://opensuse.github.io/openSUSE-docs-revamped-temp/microos_getting_started/#installing-virtualbox](https://opensuse.github.io/openSUSE-docs-revamped-temp/microos_getting_started/#installing-virtualbox)