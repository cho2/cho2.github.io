---
layout: post
title: "openSUSE Tumbleweed on MacBook Air"
description: "openSUSE Tumbleweed on MacBook Air"
comments: false
keywords: "openSUSE, Tumbleweed, MacBook Air"
---

![https://scontent-sit4-1.xx.fbcdn.net/v/t1.0-9/14690862_10207368452346414_1439740797160973501_n.jpg?oh=3c68b5821d029640e747d263e099930b&oe=58AA84EB](https://scontent-sit4-1.xx.fbcdn.net/v/t1.0-9/14690862_10207368452346414_1439740797160973501_n.jpg?oh=3c68b5821d029640e747d263e099930b&oe=58AA84EB)

My MacBook Air model is [MacBook Air 5.1](https://support.apple.com/kb/SP650?locale=en_US&viewlocale=en_US). Previously, this Mac system are dualboot containing Mac OS Sierra and BlankOn (with [rEFInd](http://www.rodsbooks.com/refind/)). After i got ThinkPad X1 Carbon, i decided to install BlankOn on it. So, i backup up my data and move them to X1 Carbon. Then trying to install openSUSE Tumbleweed on my MacBook Air.

First of all, download openSUSE Tumbleweed from [http://download.opensuse.org/tumbleweed/iso/](http://download.opensuse.org/tumbleweed/iso/), i choose [current](http://download.opensuse.org/tumbleweed/iso/openSUSE-Tumbleweed-DVD-x86_64-Current.iso). I use `dd` to write Tumbleweed iso to USB flash disk. Find out the name of your USB flash disk with `lsblk`. Make sure that it is not mounted. Run the following command, replacing `/dev/sdx` with your drive, e.g. `/dev/sdb`. (do not append a partition number, so do not use something like `/dev/sdb1`):
`# dd bs=4M if=/path/to/openSUSE-Tumbleweed-DVD-x86_64-Current.iso of=/dev/sdx status=progress && sync`.

Booting Mac to USB flash disk. Because i installed [rEFInd](https://sourceforge.net/projects/refind/) before, it's easy to choose booting from USB flash disk. Then the openSUSE installer will be appear. Unfortunately, touchpad isn't detected. I use USB mouse to move cursor. Run the installer as well as usual until finish.

After installation finish, reboot and login, you'll find that WiFi is not active. Download  [driver](https://software.opensuse.org/package/broadcom-wl) and
[kernel module](https://software.opensuse.org/package/broadcom-wl-kmp-default) manually, choose Tumbleweed. Reboot and ...voila, WiFi will active.

Well, remember that openSUSE Tumbleweed overwrite the default EFI boot manager. So that, you need to install rEFInd manually if you want boot into Mac OS. Download the rpm binary file [here](http://www.rodsbooks.com/refind/getting.html). Extract and install it. [Here is the step](http://www.rodsbooks.com/refind/installing.html#linux):

* `# cp -r refind /boot/efi/EFI/`
* `# cd /boot/efi/EFI/refind`
* `# mv refind.conf-sample refind.conf.`
* `#  efibootmgr -c -l \\EFI\\refind\\refind_x64.efi -L rEFInd`

Reboot and rEFInd back again.

There is instruction from openSUSE about [installation on a Mac](https://en.opensuse.org/SDB:Installation_on_a_Mac). You should follow those instruction if you never install GNU/Linux on Mac. Good luck.
