---
layout: post
title: "Backup Flatpak Part 2"
description: "Backup Flatpak Part 2"
comments: false
keywords: "Flatpak"
---

After got complicated with the [previous post](https://blog.kukuh.syafaat.id/2018/backup-flatpak/), this is the continuation. 

 * Backup `.local/share/flatpak/` or rename with `.local/share/flatpak.orig/` 
 * Backup `/var/lib/flatpak/` or rename with `/var/lib/flatpak.orig/`
 * Remove `.local/share/flatpak/*.*` and `/var/lib/flatpak/*.*` 
 * Run `flatpak remotes` and `flatpak list`, the result should be empty
 * Copy `config` and `*.gpg` on `repo` directory from the old one (.orig) to the new one
 * Copy `app` and `runtime` directories from the old one (.orig) to the new one
 * Run `flatpak list`, the result should be your flatpak apps and runtime
 * Run `flatpak update` for `--user` and `--system`
 * If your flatpak version is 1.0.0, run `flatpak repair`.

Note the result may be vary. Happy Flatpaking! 💓📦💓📦