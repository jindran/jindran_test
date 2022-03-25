+++
title = "Widget pro komentáře"
date = 2021-11-27T19:54:29+08:00
featured = true
comment = true
toc = true
reward = true
categories = [
  "Comments",
  "Widget"
]
tags = [
  "Disqus",
  "Utterances"
]
series = [
  "Docs"
]
images = []
[menu.footer]
  parent = "features"
  weight = 7
  pre = '<i class="fas fa-fw fa-comments"></i>'
+++

Widgety pro komentáře [Disqus](https://disqus.com/) a [Utterances](https://utteranc.es/) jsou podporovány již po instalaci.
Tento článek ukazuje, jak je nakonfigurovat a dokonce přizpůsobit své vlastní widgety pro komentáře.

<!--more-->

## Disqus

[Disqus](https://disqus.com/) widget pro koment85e je podporov8n v Hugo.

```toml
disqusShortname = "yourdiscussshortname"
```

> Mějte prosím na paměti, že `disqusShortname` je konfigurace webu, **není** parametr. Vložení do `params` nebude fungovat.

## Promluvy

[Utterances](https://utteranc.es/) je jednoduchý widget pro komentáře vytvořený na základě problémů GitHubu.

```toml
[utterances]
  repo = "uživatel/repo"
  #issueTerm = "název cesty" # název cesty, url, název, og:název.
  #label = "komentář" # Volitelné.
  #theme = ""
```

> Na rozdíl od Disqus je Utterances **** parametr. Měli byste to zadat do "params".

### Parametry

| Jméno | Typ | Výchozí | Popis |
|:---|:---|:---|:---
| `utterances.repo` | Řetězec | - | úložiště GitHub.
| `utterances.issueTerm` | Řetězec | `cesta` | Mapování mezi blogovými příspěvky a problémy GitHub: `pathname` | `pathname`, `url`, `title` a `og:title`.
| `utterances.label` | Řetězec | - | Štítek, který bude přiřazen problémům vytvořeným pomocí Utterances.
| `utterances.theme` | Řetězec | - | `github-light` a `github-dark` budou použity ve světlém a tmavém režimu, pokud nejsou nastaveny. Volitelné hodnoty: `github-light`, `github-dark`, `preferred-color-scheme`, `github-dark-orange`, `icy-dark`, `dark-blue` a `photon-dark`.

### Odstraňování problémů

- Ujistěte se, že repo je veřejné, jinak vaši čtenáři nebudou moci zobrazit problémy/komentáře.
- Ujistěte se, že je v úložišti nainstalována aplikace [utterances](https://github.com/apps/utterances), jinak uživatelé nebudou moci přidávat komentáře.
- Pokud je vaše repo fork, přejděte na jeho kartu nastavení a potvrďte, že je zapnutá funkce problémů.

## Widget pro vlastní komentáře

Nemáme v úmyslu podporovat všechny widgety pro komentáře, ale nebojte se, svůj vlastní widget pro komentáře si můžete přizpůsobit.

> Před vytvořením vlastního widgetu pro komentáře budete muset deaktivovat ostatní.

``` shell
mkdir -p layouts/partials/post/comments
echo "WIDGET MOJE KOMENTÁŘE" > layouts/partials/post/comments/custom.html
```

Mezitím možná budete muset zavést aktiva třetích stran, což lze vyřešit [přizpůsobením aktiv]({{< ref "/posts/custom-assets" >}}) nebo [Hooks]({{< ref " /posts/hooks" >}}) snadno.