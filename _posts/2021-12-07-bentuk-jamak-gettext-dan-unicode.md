---
layout: post
title: "Bentuk Jamak gettext dan Unicode"
description: "Bentuk Jamak gettext dan Unicode"
comments: false
keywords: "gettext, Unicode, l10n"
---

Pos ini merupakan pemutakhiran dari [pos sebelumnya](https://blog.kukuh.syafaat.id/2019/Bentuk-Jamak-Untuk-Format-gettext/). Seperti saya tulis [disini](https://github.com/gnome-id/l10n-plural-string#pemutakhiran-2021), ini adalah hasil diskusi singkat saya dengan Pak [Andika Triwidada](https://www.linkedin.com/in/atriwidada/), di kanal telegram GNOME l10n ID. Seperti sudah ditulis [disini](https://i14i.andika.info/index.php?title=Halaman_Utama#Bentuk_Jamak), mana yang benar identifikasi bentuk jamak untuk bahasa Indonesia? Apakah yang digunakan gettext? Atau Unicode?

# GNU gettext
Lihat https://www.gnu.org/software/gettext/manual/html_node/Plural-forms.html.

Two forms, singular used for one onl This is the form used in most existing programs since it is what English is using. A header entry would look like this:

```
Plural-Forms: nplurals=2; plural=n != 1;
```

(Note: this uses the feature of C expressions that boolean expressions have to value zero or one.) Languages with this property include: Austronesian family: Bahasa Indonesian

# Unicode
https://unicode-org.github.io/cldr-staging/charts/37/supplemental/language_plural_rules.html

```
Plural-Forms: nplurals=1; plural=0;
```
# Kasus yang Pernah Ditemui

- Tunggal: `There is one item bla bla bla`
- Jamak: `There are %d items bla bla bla`

# Kesimpulan
- Kembali ke nplurals=1
- Jika menemui kasus seperti di atas, laporkan sebagai kutu

---

Terjemahan antarmuka untuk [GNOME 42](https://l10n.gnome.org/languages/id/gnome-42/ui/) sudah dimulai, saya pun telah membuat [daftar berkas po yang perlu disesuaikan](https://github.com/gnome-id/l10n-plural-string/blob/master/gnome-42-plurals.md). Untuk terjemahan proyek perangkat terbuka yang lain, silakan menyesuaikan ya.