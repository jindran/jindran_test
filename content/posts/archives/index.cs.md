+++
title = "Archlív page"
description = ""
date = 2021-12-03T11:16:51+08:00
featured = false
comment = true
toc = true
reward = true
categories = [
  "Archive"
]
tags = [
]
series = [
  "Docs"
]
images = []
[menu.footer]
  parent = "docs"
  weight = 7
  pre = '<i class="fas fa-fw fa-file-archive"></i>'
+++

Archiv je kolekce příspěvků seskupených po rocích.

<!--more-->

## Prerequisites

Je třeba vytvořit stránku `archives/_index.md` ve složce `content`.

```toml
+++
title = "Archívy"
layout = "archive"
+++
```

## Site Parameters

| Name | Type | Default | Description
|---|:-:|:-:|---
| `archive` | Object | - | Archive.
| `archive.paginate` | Integer | `100` | Archive pagination.
| `archive.dateFormat` | Integer | `Jan 2` | Archive date format.
