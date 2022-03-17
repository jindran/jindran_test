+++
title = "Vzhled"
date = 2022-01-04T19:42:57+08:00
featured = true
comment = true
toc = true
reward = true
pinned = true
categories = [
]
tags = [
  "Color",
  "Palette",
  "Fonts",
  "Syntax Highlighting",
  "Icons"
]
series = [
  "Docs"
]
images = []
[menu.footer]
  parent = "docs"
  weight = 3
  pre = '<i class="fas fa-fw fa-palette"></i>'
+++
Ve výchozím nastavení používá web výchozí font, barvy a vzhled.
Ačkoliv výchozí vzhled neuspokojí všechny, neobávejte se, můžete snadno změnit výchozí vzhled, jako jsou barvy, fonty, zvýraznění syntaxe.

<!--more-->

## Palettes

Systém vzhledů motivů je založen na proměnných CSS, proto můžeme snadno přizpůsobit barvu na paletu.

Ukažme si to na příkladu.

```CSS
[data-palette=blue] {
  --hbs-primary: darkblue;
  --hbs-on-primary: #fff;
}
```

Po připojení stylu k "assets/css/custom.css" se barva "modré" palety změní na "tmavě modrou".

## Fonts

### Font Family

Nepřednastavujeme žádné písmo, takže ve většině prohlížečů bude použito "system-ui".

Můžete snadno používat fonty, například [Písma Google](https://fonts.google.com/). Vezměme písmo Roboto jako příklad.

Nejprve importujeme písmo pomocí `customCSS`:


```
customCSS = [
  "https://fonts.googleapis.com/css2?family=Roboto&display=swap"
]
```

A pak přepište proměnnou `--hbs-body-font-family` v `assets/css/custom.css`:

```CSS
:root {
  --hbs-body-font-family: 'Roboto', sans-serif;
}
```

## Zvýraznění syntaxe

Motiv vyžaduje, aby následující parametry značek byly nastaveny na konkrétní hodnoty.

- `lineNos`: `true`
- `lineNumbersInTable`: `false`
- `noClasses`: `false`

Viz také [Configure Highlight](https://gohugo.io/getting-started/configuration-markup#highlight).

### Style

```shell
$ hugo gen chromastyles --style=solarized-dark > assets/css/highlight.css
```

Viz také [All Supported Styles](https://xyproto.github.io/splash/docs/all.html).

## Icons

Používáme vlastní sadu ikon [Font Awesome] (https://fontawesome.com/), abychom zmenšili velikost souboru ikon.
Z tohoto důvodu si můžete vybrat další ikony.

### Font Awesome

#### Custom Build

>Tato sekce obsahuje front-end technologie, jako je `JavaScript` a `npm`.
 
Poskytli jsme soubor s názvem "assets / js / icons.js" pro přizpůsobení ikon, proto můžete podle potřeby přidat ikony.
Prostředí e build jsme pro vás již nastavili v ukázkovém webu.

1. Instalace závislostí
 
```shell
$ npm install
```

2. Add icons into `src/icons/index.js`:

```js
import { faGlobe, faClock } from '@fortawesome/free-solid-svg-icons';

library.add(faGlobe, faClock);
```

3. Rebuild `assets/js/icons.js`:

```shell
$ npm run build
```

Je to doporučený způsob, jak přidat ikony, pokud jste obeznámeni s vývojem front-endu.

#### CustomJS

Vzhledem k tomu, že motiv používá rámec JS + SVG k nahrazení ikon do SVG, takže `customCSS` nebude fungovat, musíte místo toho použít `customJS`.

```toml
customJS = [
  "https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@5.15.4/js/solid.min.js" # Import solid icons.
  #"https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@5.15.4/js/regular.min.js" # Import regular icons.
  #"https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@5.15.4/js/brands.min.js" # Import brand icons.
  #"https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@5.15.4/js/all.min.js" # Import the full icon set.
]
```

### Others

Ostatní ikony lze importovat pomocí `customCSS`, `customJS` nebo [Hooks]({{< ref "/posts/hooks" >}}).

- [Iconify](https://iconify.design/)
- [Bootstrap Icons](https://icons.getbootstrap.com/)
- [Material Design Icons](https://materialdesignicons.com/)
