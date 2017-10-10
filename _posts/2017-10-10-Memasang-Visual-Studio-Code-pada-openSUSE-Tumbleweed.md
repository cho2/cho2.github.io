---
layout: post
title: "Memasang Visual Studio Code pada openSUSE Tumbleweed"
description: "Memasang Visual Studio Code pada openSUSE Tumbleweed"
comments: false
keywords: "openSUSE, Tumbleweed, Visual Studio Code"
---

Buka terminal, lalu pasang repositori Visual Studio Code untuk openSUSE (dapat pula dipasang pada openSUSE Leap)

```
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
```

```
sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" &gt; /etc/zypp/repos.d/vscode.repo'
```

Perbarui repositori Anda
```
sudo zypper refresh
```
Pasang Visual Studio Code
```
sudo zypper install code
```

![https://opensuse.id/wp-content/uploads/2017/10/Cuplikan-layar-dari-2017-10-10-11-53-44.png](https://opensuse.id/wp-content/uploads/2017/10/Cuplikan-layar-dari-2017-10-10-11-53-44.png)