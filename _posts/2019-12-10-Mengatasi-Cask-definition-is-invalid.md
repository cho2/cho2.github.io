---
layout: post
title: "Mengatasi galat invalid 'depends_on macos' value pada Brew"
description: "Mengatasi galat invalid 'depends_on macos' value pada Brew"
comments: false
keywords: "Brew"
---

Jadi ceritanya habis memutakhirkan mesin Mac lama yang ternyata masih dapat [Catalina](https://www.apple.com/id/macos/catalina/). Setelah memutakhirkan, ternyata perlu memasang ulang Spotify yang dipasang melalui `brew`. Spotify ini sebelumnya telah terhapus, tapi tidak dihapus melalui `brew`. Coba pasang ulang melalui `brew` ternyata mendapat galat sebagai berikut

```
brew cask reinstall spotify                                                                      
==> Downloading https://download.scdn.co/Spotify.dmg
Already downloaded: /Users/cho2/Library/Caches/Homebrew/downloads/5ef9b045e7e6dfeb70b32abfa9ca2da11e85c9b27ab7f6403658ddb1fcfdc00a--Spotify.dmg
==> No SHA-256 checksum defined for Cask 'spotify', skipping verification.
Error: Cask 'spotify' definition is invalid: invalid 'depends_on macos' value: ">= :lion"
```

Googling kesana-kemari, solusinya jalankan 

```
/usr/bin/find "$(brew --prefix)/Caskroom/"*'/.metadata' -type f -name '*.rb' -print0 | /usr/bin/xargs -0 /usr/bin/perl -i -pe 's/depends_on macos: \[.*?\]//gsm;s/depends_on macos: .*//g'
```

seperti yang dijelaskan [disini](https://github.com/Homebrew/homebrew-cask/issues/58046).