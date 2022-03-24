+++
title = "Jak se zapojit"
date = 2021-11-27T19:54:29+08:00
comment = true
toc = true
reward = true
categories = [
]
tags = [
]
series = [
  "Docs"
]
images = []
[menu.main]
  parent = "support"
  weight = 5
[menu.footer]
  parent = "support"
  weight = 5
+++

Rádi si vyslechneme vaše názory a zpětnou vazbu a uvítáme, když se zapojíte.

<!--more-->

## Komunity

- [Feature Request](https://github.com/razonyang/hugo-theme-bootstrap/issues/new?template=feature_request.md)
- [Bug Report](https://github.com/razonyang/hugo-theme-bootstrap/issues/new?template=bug_report.md)
- [Discussions](https://github.com/razonyang/hugo-theme-bootstrap/discussions): ask questions, share ideas etc.

## Přispět

Vítány jsou jakékoli příspěvky, jako jsou dokumenty, opravy chyb a nové funkce.

### Pravidla

S ohledem na snadnou údržbu jsme vypracovali některá pravidla.

#### Specifikace konvenčních závazků

Dodržujte prosím [Specifikaci konvenčních závazků] (https://www.conventionalcommits.org/en/v1.0.0/).

Například:

- bug fix: `fix: opravte překlepy`
- new feature: `feat: přidejte parametr foobar`
- docs: `docs: dokumentujte parametr foobar`
- style: `style: změňte barvu pozadí na modrou`
- rebuild assets: `chore: obnovte aktiva`

### Rozvoj

Téma se opírá o `npm` a `webpack` pro vytváření aktiv: JS, CSS, fonty atd.

> Zdrojový kód byl umístěn do adresáře `src`.

#### Nainstalujte závislosti

```shell
$ npm install
```

#### Obnovte aktiva

```shell
$ npm run build
```

> `npm run watch` znovu vytvoří aktiva při změně.

#### Náhled

```shell
$ npm run serve
```
