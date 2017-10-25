---
layout: post
title: "About AppImage on openSUSE Asia Summit 2017"
description: "About AppImage on openSUSE Asia Summit 2017"
comments: false
keywords: "AppImage, openSUSE"
---

There are two AppImage talk on [openSUSE Asia Summit 2017](https://events.opensuse.org/conference/summitasia17). The first one is my talk, [Flatpak & AppImage Usage on openSUSE. Which One Suitable for openSUSE Users? ](https://events.opensuse.org/conference/summitasia17/program/proposal/1502) and the second is [Using OBS to Build Containerized Application Image ](https://events.opensuse.org/conference/summitasia17/program/proposal/1608). At the last day of summit, [Simon Peter](https://github.com/probonopd) write an [issue](https://github.com/cho2/slides/issues/1) about my topics. He give me some additional information that i'm probably missed about AppImage.

| Features | AppImage |
| -------- |:--------:|
| No software necessary to install a package|**Yes**. Actually, with AppImage, software is never "installed". The downloaded format is the same as the executed format. This an advantage |
| Shared runtimes|**No**. By design, AppImage allows no dependencies other than what can be expected to be part of all target systems. Like with apps for iOS, everything is either in the OS or in the app. This removes the need for dependency management on the user's end. This an advantage |
| Sandboxing|**Yes**. AppImage works with various sandboxes such as [Firejail](https://firejail.wordpress.com/documentation-2/appimage-support/). It is not hardcoded toward any particular sandbox. This an advantage|
| Repository support|**No**. Users can just download and run one file without having to manage repositories. This an advantage|
| Central repo|**No**. By design, AppImage is meant to be decentral, so there are no "gatekeepers". An author can put an AppImage onto the download page just like an EXE or DMG. This an advantage|
| Updates|**Yes**. AppImage supports binary delta updates where you only download the few MB that actually have changed from version to version. Additionally, there is [AppImageHub](https://appimage.github.io/apps/) which lists tested AppImages, and that is managed as a GitHub repository to which everyone can contribute. This an advantage| 

Actually, those table above came from [this page](https://www.devpy.me/snapcraft-appimage-flatpak) but the information is obsolete so that Simon gave me clarify of the features that i claimed missing from AppImage.

The other [AppImage guys](https://github.com/TheAssassin) also reminds me about some material that i'm put into the slide from [Simon's slide at openSUSE Conference 2017](https://speakerdeck.com/probonopd/opensuse-conference-2017-obs-b-appimage). Now the [slide](https://github.com/cho2/slides/tree/master/openSUSE-Asia-Summit-2017) updated with url source. 

<iframe src="//www.slideshare.net/slideshow/embed_code/key/f8rszs00kDFOF2" width="595" height="485" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe> <div style="margin-bottom:5px"> <strong> <a href="//www.slideshare.net/cho2marsmellow/flatpak-and-appimage-usage-on-opensuse-81190470" title="Flatpak and AppImage usage on openSUSE" target="_blank">Flatpak and AppImage usage on openSUSE</a> </strong> from <strong><a href="https://www.slideshare.net/cho2marsmellow" target="_blank">Kukuh Syafaat</a></strong> </div>