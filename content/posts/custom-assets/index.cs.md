+++
title = "Přizpůsobení"
date = 2021-11-28T16:00:49+08:00
featured = true
comment = true
toc = true
reward = true
categories = [
  "Assets"
]
tags = [
  "CSS",
  "JS"
]
series = [
  "Docs"
]
images = []
[menu.footer]
  parent = "docs"
  weight = 6
+++

Přizpůsobitelné témata poskytují možnost přizpůsobit chování, ať už jde o přizpůsobení stlů pomocí CSS a JS, nebo zavedení CSS a JS třetích stran.

<!--more-->

## Internal Assets

Stačí vytvořit a upravit soubory `assets/css/custom.css` a `assets/js/custom.js`.

> Tyto soubory budou sloučeny do jednoho pro zmenšení požadavků HTTP.

## External Assets

Jakékoli externí zdroje CSS a JS lze importovat pomocí parametrů `customCSS` a `customJS`.


```toml
customCSS = [
  "external-foo.css",
  "external-bar.css"
]

customJS = [
  "external-foo.js",
  "external-bar.js"
]
```
