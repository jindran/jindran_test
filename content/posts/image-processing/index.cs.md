+++
title = "Zpracování obrazu"
description = "Průvodce změnou velikosti a zarovnáním obrázků"
date = 2021-08-15T14:19:06+08:00
draft = false
comment = true
toc = true
reward = true
categories = [
  "Markdown"
]
tags = [
  "Image"
]
series = [
  "Docs"
]
images = [
  "images/center.png"
]
[menu.footer]
  parent = "features"
  weight = 2
+++

Tento článek nabízí několik případů použití, které ukazují, jak změnit velikost a zarovnÁNÍ obrázkŮ.
<!--more-->

## Změna velikosti obrázků

Ke změně velikosti obrázků používáme URL adresu obrázku. Například:

### Zadejte šířku a poměr zachovejte

```markdown
![Resize](images/sample.png?width=300px)
```

![Resize](images/sample.png?width=300px)

### Specifikujte výšku a poměr zachovejte

```markdown
![Resize](images/sample.png?height=200px)
```

![Resize](images/sample.png?height=200px)

### Specifikujte šířku i výšku

```markdown
![Resize](images/sample.png?width=300px&height=200px)
```

![Resize](images/sample.png?width=300px&height=200px)

> Lze jej použít nejen pro [zdroje stránky](https://gohugo.io/content-management/page-resources/), ale také pro **statické** obrázky a externí obrázky.
> Kromě zdrojů stránky se však velikost ostatních mění inline stylem, to znamená, že jejich původní velikost se nezmění.

## Zarovnání obrázků

Obrázky můžeme snadno zarovnat přidáním fragmentů URL. Například `#center`, `#floatleft` a `#floatright` představuje zarovnání na střed, plovoucí vlevo a plovoucí vpravo.

### Střed

Přidání `#center` fragment pro zarovnání obrázků na střed.

Například: `![Center](/images/center.png#center)`.

![Center](/images/center.png#center)

### Plovoucí vlevo

![Float Left](/images/left.png#floatleft)

Přidání fragmentu `#floatleft` pro plovoucí obrázky doleva.

Například: `![Float Left](/images/left.png#floatleft)`.

### Plovoucí vpravo

![Float Right](/images/right.png#floatright)

Podobně můžeme také plout obrázky doprava přidáním fragmentu `#floatright`.

Například: `![Float Right](/images/right.png#floatright)`.
