---
layout: post
title: "Bentuk Jamak Untuk Format gettext"
description: "Bentuk Jamak Untuk Format gettext"
comments: false
keywords: "gettext"
---

Menurut [catatan Andika Triwidada](https://www.facebook.com/notes/andika-triwidada/bentuk-jamak-untuk-terjemahan-format-gettext-saatnya-kembali-ke-jalan-yang-benar/2104238809628586/), sudah waktunya bagi semua tim terjemahan Indonesia untuk kembali ke jalan yang benar. Pada [dokumentasi ini](http://docs.translatehouse.org/projects/localization-guide/en/latest/l10n/pluralforms.html), dinyatakan bahwa bentuk jamak Indonesia menggunakan bentuk di bawah ini.

```
Plural-Forms: nplurals=1; plural=0;
```

GNOME juga menggunakan bentuk ini untuk bahasa Indonesia, tetapi pada [LIbreOffice Pootle](https://translations.documentfoundation.org/), bentuk jamak tersebut tidak pernah muncul ketika menggunakan antar muka bahasa Indonesia di LibreOffice.

Pada [manual gettext](https://www.gnu.org/software/gettext/manual/html_node/Plural-forms.html#Plural-forms), dinyatakan bentuk jamak yang tepat untuk bahasa Indonesia (Austronesian family) yaitu __Two forms, singular used for one only__.

```
Plural-Forms: nplurals=2; plural= n!=1;
```

Jadi, tahun 2019 ini adalah waktu yang tepat untuk pindah ke bentuk yang dinyatakan oleh gettext.