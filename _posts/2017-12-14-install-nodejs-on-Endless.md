---
layout: post
title: "Install NodeJS on Endless OS"
description: "Install NodeJS on Endless OS"
comments: false
keywords: "NodeJS, Endless"
---

Install nvm
```
wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.33.8/install.sh | bash
```

Run
```
command -v nvm
```
then close your current terminal and open a new terminal.

Install latest node
```
nvm install node
```

Install LTS node
```
nvm install --lts
```

![https://assets.gitlab-static.net/cho2/blog-images/raw/master/2017-12-14/node.png](https://assets.gitlab-static.net/cho2/blog-images/raw/master/2017-12-14/node.png)
Node LTS on Endless

![https://assets.gitlab-static.net/cho2/blog-images/raw/master/2017-12-14/cordova.png](https://assets.gitlab-static.net/cho2/blog-images/raw/master/2017-12-14/cordova.png)
[Cordova](https://cordova.apache.org/) on Endless with `npm install -g cordova`