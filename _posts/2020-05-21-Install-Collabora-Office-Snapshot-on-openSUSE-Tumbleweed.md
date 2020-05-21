---
layout: post
title: "Install Collabora Office (Snapshot) on openSUSE Tumbleweed"
description: "Install Collabora Office (Snapshot) on openSUSE Tumbleweed"
comments: false
keywords: "openSUSE, Collabora Office"
---

![https://gitlab.com/cho2/blog-images/-/raw/master/2020-05-21/collabora-office.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-05-21/collabora-office.png)

What is Collabora Office? Collabora Office is the enterprise office suite of LibreOffice, the world’s most widely used Open Source office suite.

Have you ever try Collabora Office? Let's try the latest snapshot. You can also try it on openSUSE Leap.

* Download and import key

    ```
    wget https://www.collaboraoffice.com/Collabora-Office-6.2-Snapshot/Linux/yum/repodata/repomd.xml.key && sudo rpm --import repomd.xml.key
    ```
* Add repository

    ```
    sudo zypper addrepo 'https://www.collaboraoffice.com/Collabora-Office-6.2-Snapshot/Linux/yum' 'Collabora Office 6.2 Snapshot'
    ```

* Refresh

    ```
    sudo zypper ref
    ```

* Install

    ```
    sudo zypper install collaboraoffice
    ```

* Enjoy!
