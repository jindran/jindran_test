+++
title = "Hooks"
date = 2021-11-27T19:54:29+08:00
featured = true
comment = true
toc = true
reward = true
categories = [
  "Hook"
]
tags = [
]
series = [
  "Docs"
]
images = []
[menu.footer]
  parent = "docs"
  weight = 6
+++

Jako flexibilní téma by mělo mít možnost upravit kód a integrovat služby třetích stran. Proto jsme přinesli funkci zvanou hook.

V tomto článku si představíme všechny hooky a uvedeme některé případy použití.

<!--more-->

## Přehled

| Hook | Popis |
|---|---|
| `head-end` | Before the `<head>` end |
| `body-end` | Before the `<body>` end |
| `main-begin` | Above of the `<main>` |
| `main-end` | Follow the `<main>` |
| `list-begin` | Above of the posts list |
| `list-end` | Follow the posts list |
| `sidebar-begin` | At very top of the sidebar |
| `sidebar-end` | Before the sidebar end |
| `content-begin` | Above of the post content |
| `content-end` | Follow the post content |
| `comments-begin` | Above of the comments |
| `comments-end` | Follow the comments |
| `footer-begin` | At very top of the footer |
| `footer-end` | Before the footer end |
| `post-panel-begin` | At very top of the post panel |
| `post-panel-end` | Before the post panel end |

## Užití
Je snadné použít hook, co musíte udělat, je vytvořit HTML soubor se stejným názvem jako hook v adresáři `layouts/partials/hooks`.

Vezměme si jako příklad `sidebar-begin`:

``` shell
echo '<section class="row card component text-center"><div class="card-body">ZAČÁTEK BOČNÍ LIŠTY</div></section>' \
   > layouts/partials/hooks/sidebar-begin.html
```
