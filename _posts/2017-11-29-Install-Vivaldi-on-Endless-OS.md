---
layout: post
title: "Vivaldi on Endless OS"
description: "Vivaldi on Endless OS"
comments: false
keywords: "Vivaldi, Endless"
---

Download Vivaldi
```
wget http://repo.vivaldi.com/stable/deb/pool/main/vivaldi-stable_1.13.1008.32-1_amd64.deb
```

Download `standalone-vivaldi` script
```
wget https://gist.githubusercontent.com/ruario/8f648cc3069d1a55d9c8/raw/7d7e7c4d2dbe3babf57cedfc32520e6b8e686f23/standalone-vivaldi.sh
```

Install
```
sh standalone-vivaldi.sh vivaldi-stable_1.13.1008.32-1_amd64.deb
```

Test run Vivaldi with temporary settings
```
vivaldi-1.13.1008.32-x64/testrun&

```

Run Vivaldi with normal settings
```
vivaldi-1.13.1008.32-x64/vivaldi&
```

Integrate with desktop environment
```
vivaldi-1.13.1008.32-x64/integrate
```

References:

* [https://vivaldi.com/blog/alternative-install-options-for-linux/](https://vivaldi.com/blog/alternative-install-options-for-linux/)
* [https://gist.github.com/ruario/8f648cc3069d1a55d9c8](https://gist.github.com/ruario/8f648cc3069d1a55d9c8)

Issue:
* `libgconf-2.so.4`

![https://assets.gitlab-static.net/cho2/blog-images/raw/master/2017-11-29/vivaldi.png](https://assets.gitlab-static.net/cho2/blog-images/raw/master/2017-11-29/vivaldi.png)