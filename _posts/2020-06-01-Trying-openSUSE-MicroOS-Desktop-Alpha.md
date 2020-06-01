---
layout: post
title: "Trying openSUSE MicroOS Desktop Alpha"
description: "Trying openSUSE MicroOS Desktop Alpha"
comments: false
keywords: "openSUSE, MicroOS"
---

# Trying openSUSE MicroOS Desktop Alpha

Tested with [GNOME Boxes](https://wiki.gnome.org/Apps/Boxes) on `Snapshot20200528`. More about [MicroOS, read on the the wiki](https://en.opensuse.org/Kubic:MicroOS).

# Install

* Download latest [MicroOS iso](https://download.opensuse.org/tumbleweed/iso/).
* Boot the iso.
* On the System Role section, choose "MicroOS Desktop" (I choose GNOME).
  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/system-role.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/system-role.png)
* Finish installation as usual, then reboot.

# After Install

* Login (`gnome-display-manager`).
  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/gdm.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/gdm.png)
* Desktop (`gnome-shell`).
  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/shell-1.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/shell-1.png)
  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/shell-2.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/shell-2.png)
  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/shell-menu.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/shell-menu.png)
* About (`gnome-control-center`).
  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/about.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/about.png)
* `podman` installed by default.
  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/podman.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/podman.png)
	* run `hello-world`.
	  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/podman-hello.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/podman-hello.png)
* `flatpak` installed by default.
  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/flatpak.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/flatpak.png)
	* got error when running `flatpak remotes` and `flatpak list`.
	  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/flatpak-list-remotes.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/flatpak-list-remotes.png)
    * got error when add flatpak remotes.
	  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/flatpak-remote-add.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/flatpak-remote-add.png)
	* add flatpak remotes with `--user`.
	  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/flatpak-remote-add-user.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/flatpak-remote-add-user.png)
	* Install Firefox Flatpak.
	  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/install-firefox-flatpak.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/install-firefox-flatpak.png)
	* Run Firefox Flatpak.
	  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/run-firefox-flatpak.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/run-firefox-flatpak.png)
* `snapper`.
  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/snapper%20list.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/snapper%20list.png)
* `zypper`.
  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/zypper.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/zypper.png)
* `transactional-update`.
  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/transactional-update.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/transactional-update.png)

  After install with `transactional-update`, there will be new snapshot, reboot to new snapshot.
  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/transactional-update-2.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/transactional-update-2.png)
* `neofetch` after install with `transactional-update`.
  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/neofetch.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/neofetch.png)
* New snapshot after installation with `transactional-update`.
  ![https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/snapper-list-2.png](https://gitlab.com/cho2/blog-images/-/raw/master/2020-06-01/snapper-list-2.png)

