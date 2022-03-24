+++
title = "Widget autora"
date = 2021-12-03T11:10:19+08:00
featured = false
comment = true
toc = true
reward = true
categories = [
  "Widget"
]
tags = [
]
series = [
  "Docs"
]
images = []
+++

Widget pro autora se nachází v postranním panelu, abyste se krátce představili.

<!--more-->

## Konfigurace webu

Konfigurační soubor je standardně umístěn v `config/_default/author.toml`.
Můžete jej vypnout odstraněním konfigurace `autor`.

| Jméno | Typ | Výchozí | Popis
|---|:-:|:-:|---
| `author` | Objekt | - | Profil autora zobrazený na postranním panelu.
| `autor.name` | Řetězec | - | Název.
| `autor.avatar` | Řetězec | `images/profile.webp` | Avatar.
| `autor.bio` | Řetězec | - | Bio.
| `autor.company` | Řetězec | - | Společnost.
| `autor.location` | Řetězec | - | Umístění.
| `autor.o` | Řetězec | - | Externí o stránce. Není-li nastavena, použije se interní stránka informací.
| `autor.params` | Objekt | - |
| `author.params.layout` | Řetězec | - | Nepovinné hodnoty: `kompaktní`.
| `autor.social` | Objekt | - | [Sociální odkazy]({{< ref "/posts/widgets/social-links" >}}).
