+++
title = "Image Viewer"
date = 2021-12-03T20:46:50+08:00
featured = false
comment = true
toc = true
reward = true
categories = [
  "Image Viewer"
]
tags = [
]
series = [
  "Docs"
]
images = []
[menu.footer]
  parent = "features"
  weight = 3
+++

Prohlížeč obrázků je galerie obrázků, zobrazí se, když kliknete na obrázek, na který nelze odkazovat.

Poskytuje také mnoho nástrojů, jako je přiblížení, oddálení a otočení.

<!--more-->

> Avatar autora byl ve výchozím nastavení filtrován.

## Site Parameters

Prohlížeč obrázků byl ve výchozím nastavení zapnutý, můžete jej vypnout nastavením parametru `viewer` na `false`.
## Options

Možnosti můžete vyladit vytvořením `assets/js/viewer.config.js`.

```js
window.viewerOptions = {
    className: "image-viewer",
    // ...
};
```

Dostupné možnosti jsou uvedeny v [Možnosti Viewer.js] (https://github.com/fengyuanchen/viewerjs#options).
