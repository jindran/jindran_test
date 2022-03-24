+++
title = "Reward Widget"
date = 2021-12-03T11:10:19+08:00
featured = false
comment = true
toc = true
reward = true
categories = [
  "Widget"
]
tags = [
  "Buy Me a Coffee"
]
series = [
  "Docs"
]
images = []
[menu.footer]
  parent = "features"
  weight = 7
  pre = '<i class="fas fa-fw fa-coffee"></i>'
+++

Widget odměny, AKA kupte si mi kávu widget, poskytuje čtenářům způsob, jak podpořit tvůrce pomocí darů nebo tipů.

<!--more-->

## Parametry webu

`Odměna` je pár klíčových hodnot, který mapuje z platformy na jejich obrázek QR kódu, a proto je podporována jakákoli platforma, která podporuje kód QR.

| Name | Type | Default | Description
|---|:-:|:-:|---
| `reward` | Object | - | 
| `reward.alipay` | String | - | Obrázek QR kódu Alipay.
| `reward.wechat` | String | - | Obrázek QR kódu Wechat.

## Parametr stránky

| Name | Type | Default | Description
|---|:-:|:-:|---
| `reward` | Boolean | `true` | Zapnutí/vypnutí widgetu odměny.
