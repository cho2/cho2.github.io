---
layout: post
title: "Installing and Using GNOME Builder on openSUSE Tumbleweed"
description: "Installing and Using GNOME Builder on openSUSE Tumbleweed"
comments: false
keywords: "openSUSE, Tumbleweed, GNOME, Builder"
---

This is English version of [https://opensuse.id/2017/04/16/memasang-dan-menggunakan-gnome-builder-pada-opensuse-tumbleweed/](https://opensuse.id/2017/04/16/memasang-dan-menggunakan-gnome-builder-pada-opensuse-tumbleweed/), but i'm sorry that the screenshot in Indonesia.

Actually this guide refers to the following article: [https://csorianognome.wordpress.com/2017/04/07/the-new-contribution-workflow-for-gnome/](https://csorianognome.wordpress.com/2017/04/07/the-new-contribution-workflow-for-gnome/). The first thing to do is of course installing GNOME Builder. Make sure you're using the GNOME desktop. The installation process is more or less like in the following picture. Just type `sudo zypper in gnome-builder` at your favorite terminal.

![https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_12_47_45.png](https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_12_47_45.png)

![https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_12_50_37.png](https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_12_50_37.png)

Then open GNOME Builder.

![https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_12_55_29.png](https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_12_55_29.png)

The GNOME Builder window will appear as follows.

![https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_12_56_26.png](https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_12_56_26.png)

GNOME has its own git repository located at [https://git.gnome.org](https://git.gnome.org). We will try to clone a repository and try to build it. Press the "Clone ..." button.

![https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_12_56_26-1.png](https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_12_56_26-1.png)

Enter the URL of the repository to be cloned.

![https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_13_00_24.png](https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_13_00_24.png)

For example, the repository to be cloned is GNOME Maps ([https://git.gnome.org/browse/gnome-maps](https://git.gnome.org/browse/gnome-maps)) with the git address [https://git.gnome.org/browse/maps](https://git.gnome.org/browse/maps). Enter the URL address as shown below, then press the blue "Clone" button on the top right.

![https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_13_51_26.png](https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_13_51_26.png)

The clone process will take place. *PS: This process may take a long time (depending on the size of the repository being localized, such as the git clone process in git)*

![https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_13_51_34.png](https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_13_51_34.png)

Once the clone process is complete, the GNOME Builder view will look like the following.

![https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_13_52_37.png](https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_13_52_37.png)

Click on the omnibar will appear as follows.

![https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_13_55_16.png](https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_13_55_16.png)

We will try to build GNOME Maps using GNOME Builder. In the picture above, click the "Build" button. Then the process of building GNOME Maps will run like the picture below. PS: This process may take a long time (2).

![https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_13_56_34.png](https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_13_56_34.png)

After the build process is successful, the display will be as follows.

![https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_14_47_11.png](https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_14_47_11.png)

At the top right, it appears that the build process is successful.

![https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_14_44_23.png](https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_14_44_23.png)

To try the build result, press the button with the play icon as shown below.

![https://opensuse.id/wp-content/uploads/2017/04/Cuplikan-layar-dari-2017-04-16-14-49-40.png](https://opensuse.id/wp-content/uploads/2017/04/Cuplikan-layar-dari-2017-04-16-14-49-40.png)

The installation process will run (see Build Output).

![https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_14_51_53.png](https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_14_51_53.png)

Then, the GNOME Maps will appear.

![https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_14_54_26.png](https://opensuse.id/wp-content/uploads/2017/04/VirtualBox_Tumbleweed_16_04_2017_14_54_26.png)

Congratulations, you have successfully installing and using GNOME Builder. You can also try to build other apps from GNOME available in the GNOME repository ([https://git.gnome.org/browse/](https://git.gnome.org/browse/)).

More on GNOME Builder, you can read the documentation at [https://builder.readthedocs.io/en/latest/index.html](https://builder.readthedocs.io/en/latest/index.html).
