+++
title = "Kontaktní formulář"
date = 2022-03-04T23:56:00+08:00
featured = false
comment = true
toc = true
reward = true
categories = [
  "Contact Form"
]
tags = [
  "Netlify",
  "Getform"
]
series = [
  "Docs"
]
images = []
[menu.footer]
  parent = "features"
  weight = 6
  pre = '<i class="fas fa-fw fa-question-circle"></i>'
+++

Můžeme uvést naši e-mailovou adresu [social links]({{< ref "/posts/widgets/social-links" >}}) aby nás čtenáři mohli kontaktovat. Bohužel, e-maily budou víceméně považovány za spam a dokonce i filtrovány.
Proto přinášíme funkci zvanou kontaktní formulář.

<!--more-->

## Prerequisites

Potřebujeme vytvořit kontaktní stránku s názvem `contact/index.md` v adresáři `content`, abychom měli přístup k kontaktnímu formuláři.

```toml
+++
title = "Kontaktujte nás"
layout = "contact"
+++
```

Po vytvoření se odkaz objeví ve widgetu profilu.


## Parameters

| Name | Type | Default | Description
|---|:-:|:-:|---
| `contact` | Object | - | 
| `contact.endpoint` | String | - | See also [Backends](#backends).
| `contact.file` | Boolean | `false` | Enable/Disable file upload.
| `contact.fileField` | String | - | The name of file field.

## Backends

Je navržen tak, aby byl kompatibilní s většinou backendů, jako je [Netlify form](https://docs.netlify.com/forms/setup), [Getform](https://getform.io/) a [Formspree]( https://formspree.io/).

### Netlify

[Netlify form](https://docs.netlify.com/forms/setup) jsou podporovány již po instalaci, proto nemusíte zadávat parametr `contact.endpoint`.

> Demo stránka používá Getform místo formuláře Netlify, protože Netlify automaticky upgraduje vaši úroveň formuláře, pokud překročíte limit aktuálního plánu, což povede k dalším výdajům.

> Pokud chcete použít formulář Netlify, ujistěte se, že je parametr `contact.endpoint` prázdný.


### Others

Vezměme si [Getform](https://getform.io) jako příklad:


```toml
[contact]
  endpoint = "YOUR_ENDPOINT"
```
