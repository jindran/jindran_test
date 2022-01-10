+++
title = "Jak začít"
date = 2022-01-04T10:43:39+08:00
featured = true
comment = true
toc = true
reward = true
pinned = true
categories = [
]
tags = [
  "Instalace",
  "Upgrade"
]
series = [
  "Docs"
]
images = []
[menu.footer]
  parent = "docs"
  weight = 1
+++

Tento článek popisuje jak instalovat a upgradovat téma a vytváření příspěvků.

<!--more-->

## Instalace

### Jak vytvořit pomocí příkazů "z ruky"

```shell
$ hugo new site myblog
$ cd myblog
$ git init
$ git submodule add https://github.com/razonyang/hugo-theme-bootstrap themes/hugo-theme-bootstrap
$ cp -a themes/hugo-theme-bootstrap/exampleSite/* .
$ hugo server
```

> Pokud používáte Windows, použijte `xcopy .\themes\hugo-theme-bootstrap\exampleSite /E` místo cp.

### Instalace do existující site

```shell
$ cd myblog
$ git submodule add https://github.com/razonyang/hugo-theme-bootstrap themes/hugo-theme-bootstrap
$ mkdir config
$ cp -a themes/hugo-theme-bootstrap/exampleSite/config/* ./config
$ cp -r themes/hugo-theme-bootstrap/exampleSite/content/about/ \
  themes/hugo-theme-bootstrap/exampleSite/content/archives/ \
  themes/hugo-theme-bootstrap/exampleSite/content/categories/ \
  themes/hugo-theme-bootstrap/exampleSite/content/contact/ \
  themes/hugo-theme-bootstrap/exampleSite/content/offline/ \
  themes/hugo-theme-bootstrap/exampleSite/content/search/ \
  themes/hugo-theme-bootstrap/exampleSite/content/series/ \
  themes/hugo-theme-bootstrap/exampleSite/content/tags/ \
  ./content
$ hugo server
```

> Pokud vytváříte nový čistý klon, budete potřebovat načíst submodulu pomocí `git submodule update --init --recursive` nebo klonovat submodul pomocí `git clone --recursive <repo>`.

## Upgrade (aktualizace)

```shell
$ cd themes/hugo-theme-bootstrap
$ git fetch
$ git checkout [version]
$ cd ../../
$ git add themes/hugo-theme-bootstrap
$ git commit -m 'Upgrade the theme'
```

- Nahraďtě `[version]` poslední dostupnou verzí. poslední dostupnou verzi získáte pomocí `git tag -l | sort -rV`.
- Můžete také stáhout `master` branch pro získání poslední comitované verze.

## Psaní článků

> Suppose the default language is `en`.

```shell
$ hugo new posts/new-post/index.md
```

Příkaz výše vytvoří nový příspěvek v českém (defaultním) jazyce. Příspěvky v jiných jazycích se vytváří podobně, můžete vytvořit příspěvek v angličtině:


```shell
$ hugo new posts/new-post/index.en.md
```
> Nezapomeňte prosím, že vytvořené články jsou pouze jako draft. Pro jejich zobrazení musíte připojit parametr `-D` k příkazu `hugo server`, aby příspěvky mohly být zobrazeny.
> Podobně musíte nastavit parametr `draft` na `false`, pokud chcete zvěřejnit příspěvek.
> Similarly, you need to change the `draft` to `false` or remove `draft` parameter if you want to publish the article.

> Své příspěvky můžete uložit kdekoliv, např. jako `blog`, jediné co potřebujete je  připojit `blog` do `mainSections` parametru: `mainSections = ["posts", "blog"]`.

## Up Next

- [Tweak Configuration]({{< ref "/posts/configuration" >}})
- [Menu]({{< ref "/posts/menu" >}})
- [Look and Feel]({{< ref "/posts/look-and-feel" >}})
