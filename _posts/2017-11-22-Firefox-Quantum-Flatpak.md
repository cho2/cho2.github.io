---
layout: post
title: "Firefox Quantum Flatpak"
description: "Firefox Quantum Flatpak"
comments: false
keywords: "Firefox, Quantum, Flatpak"
---

Cant't wait [Firefox Quantum with Flatpak](https://github.com/cho2/org.mozilla.Firefox/raw/master/firefox.flatpak)? Here's my experiment.
After got headache with the [first experiment](https://github.com/cho2/firefox-quantum-flatpak), then i tried the [second experiment](https://github.com/cho2/org.mozilla.Firefox). The steps are:

## Build and install locally
* `flatpak-builder --repo=repo firefox org.mozilla.Firefox.json`
* `flatpak build-export repo firefox`
* `flatpak --user remote-add --no-gpg-verify --if-not-exists firefox-repo repo`
* `flatpak --user install firefox-repo org.mozilla.Firefox`
* `flatpak run org.mozilla.Firefox`

## Bundle
* `flatpak build-bundle repo firefox.flatpak org.mozilla.Firefox`
* `flatpak build-import-bundle repo firefox.flatpak`

## Clean 
* `flatpak uninstall --user org.mozilla.Firefox`
* `flatpak remote-delete --user firefox-repo`

## Install `firefox.flatpak`
* `flatpak install firefox.flatpak`
    * require GNOME 3.24 runtime, if there's no runtime, add the repository `flatpak remote-add --from gnome https://sdk.gnome.org/gnome.flatpakrepo`
    * then install the runtime `flatpak install gnome org.gnome.Sdk/x86_64/3.24`

## Run
* `flatpak run org.mozilla.Firefox`

### Tested on
* Endless OS 3.3.3
![https://gitlab.com/cho2/blog-images/raw/master/2017-11-22/Endless.png](https://gitlab.com/cho2/blog-images/raw/master/2017-11-22/Endless.png)

* openSUSE Leap 42.3
![https://gitlab.com/cho2/blog-images/raw/master/2017-11-22/Leap.png](https://gitlab.com/cho2/blog-images/raw/master/2017-11-22/Leap.png)

* Ubuntu 16.04
![https://gitlab.com/cho2/blog-images/raw/master/2017-11-22/Ubuntu.png](https://gitlab.com/cho2/blog-images/raw/master/2017-11-22/Ubuntu.png)

### Issue
* ~~Icon doesn't appear~~ fix on this [pull request](https://github.com/cho2/org.mozilla.Firefox/pull/1)
