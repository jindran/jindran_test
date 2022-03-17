+++
title = "FAQ stránka"
date = 2021-12-07T21:46:43+08:00
featured = false
comment = true
toc = true
reward = true
categories = [
  "FAQ"
]
tags = [
]
series = [
  "Docs"
]
images = []
+++

Stránka [FAQ]({{< ref "/faq" >}}) obsahuje odpovědi na časté dotazy.
<!--more-->

## Předpoklady

Musíte vytvořit stránku nazvanou `faq/index.md` v adresáři `content`.

```toml
+++
title = "Časté dotazy"
layout = "faq"
+++
```

## Data

Data jsou uložena v adresáři `data`, adresářová struktura je následující:

```text
data
  /en
    /faq
      foo.json
      bar.json
  /zh-cn
    /faq
      foo.json
      bar.json
```

Jak vidíte, otázky klasifikujeme podle jejich jazyka. A každý soubor představuje skupinu otázek, které mají následující formát:

```json
{
  "title": "Název skupiny",
  "weight": 1,
  "questions": [
    {
      "question": "Dotaz",
      "answer": "Odpověď"
    }
  ]
}
```

- Parametr `weight` se používá pro třídění skupiny ve vzestupném pořadí.
