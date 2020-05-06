---
layout: post
title: "Install Pop Shell on openSUSE Tumbleweed"
description: "Install Pop Shell on openSUSE Tumbleweed"
comments: false
keywords: "openSUSE Tumbleweed, Pop Shell"
---

![https://gitlab.com/cho2/blog-images/-/raw/master/2020-05-07/Tumbleweed-Tiling.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-05-07/Tumbleweed-Tiling.png)

- Idea: Bring Pop Shell Window Tiling Extension to openSUSE Tumbleweed
- Note: It only works on Xorg (https://github.com/pop-os/shell/issues/166)
- Requirements:
	- GNOME Shell 3.36
	- TypeScript 3.8
	- GNU Make
- Install dependencies

  ```
  sudo zypper in typescript make git
  ```
- Build & Install

  ```
  git clone https://github.com/pop-os/shell
  cd shell
  ./rebuild.sh 
  ```

## Extra: Install Pop Shell Shortcuts

- Install dependencies

  ```
  sudo zypper in cargo rust gtk3-devel
  ```
- Build & Install

  ```
  git clone https://github.com/pop-os/shell-shortcuts
  cd shell-shortcuts
  make
  sudo make install
  ```

## Extra Pt. 2: Remove Pop Shell & Reset Keyboard Shortcuts
 
```
rm -r ~/.local/share/gnome-shell/extensions/pop-shell@system76.com
```

**Enjoy!**

---

References:

- [How To Install Pop Shell Window Tiling Extension](https://www.linuxuprising.com/2020/05/how-to-install-pop-shell-tiling.html)
- [Pop Shell Repository](https://github.com/pop-os/shell)
- [Pop Shell Shortcuts](https://github.com/pop-os/shell-shortcuts)
