---
layout: post
title: "Backup Flatpak"
description: "Backup Flatpak"
comments: false
keywords: "Flatpak"
---

Q: Is it possibe to backup flatpak (user data, apps, runtimes, etc) instead of downloading the apps and runtime again?

A: The answer is [yes](https://twitter.com/FlatpakApps/status/1034094451101196288). For apps and runtimes, backup `~/.local/share/flatpak` and `/var/lib/flatpak`. For data, backup `~/.var`.

Then i tried with this scenario:

* Backup flatpak directories above from machine A.
* Copy flatpak directories to machine B.
* Install flatpak packages
* Run flatpak apps
* Voila, it works.
* Note: both, machine A and machine B are openSUSE Leap 15.0 with Flatpak version 0.10.4.

But, when i tried to update, the problem arose. It ends with 
```
OSTree:ERROR:src/libostree/ostree-repo.c:3729:ostree_repo_load_file: assertion failed: (S_ISREG (stbuf.st_mode))
```
Tried to updating flatpak to 1.0.0 but the problem still happened. The problem already reported on [GitHub issue](https://github.com/flatpak/flatpak/issues/1343#issuecomment-421693387). I think this is a problem with `ostree`. Ostree is just like git, zypper said that "Git for operating system binaries". Maybe command like `git stash` or something like that on ostree will fix the problem (?).

By the way, about backup flatpak or copy flatpak to another disk, you should check this [post](https://treitter.livejournal.com/16005.html). The idea is similar, instead of downlading the same apps and runtimes, we can just copy it to the disk and install it. 
