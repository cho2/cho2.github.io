---
layout: post
title: "Install Katalon Studio on openSUSE Leap"
description: "Install Katalon Studio on openSUSE Leap"
comments: false
keywords: "Katalon Studio, openSUSE"
---

![https://gitlab.com/cho2/blog-images/-/raw/master/2020-05-18/katalon-leap.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-05-18/katalon-leap.png)

* Sign up to [Katalon](https://www.katalon.com/sign-up/) web. If you already have an account, please [Sign In](https://www.katalon.com/sign-in/).
* Download [Katalon Studio for Linux](https://www.katalon.com/download/).
* The file name will be `Katalon_Studio_Linux_64-{version}.tar.gz`. Extract it.
* Install OpenJDK (Please use [OpenJDK 8](https://forum.katalon.com/t/how-to-launch-katalon-studio-in-opensuse-15-1/33108/2) instead of 11)
  ```
  sudo zypper in java-1_8_0-openjdk
  ```
* Go to Katalon Studio directory
  ```
  cd Katalon_Studio_Linux_64-{version}/
  ```
* Run Katalon
  ```
  ./katalon
  ```
* Sign in with your account
* Enjoy Katalon Studio
* Additional set-up for Mobile and Web Services see [Katalon Studio for Linux](https://docs.katalon.com/katalon-studio/docs/katalon-studio-gui-beta-for-linux.html).