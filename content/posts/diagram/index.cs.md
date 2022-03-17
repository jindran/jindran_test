+++
title = "Používání diagramů"
description = "Jak pracovat s diagramy pomocí Markup"
date = 2021-09-01T11:36:50+08:00
featured = false
draft = false
comment = true
toc = true
reward = true
diagram = true
categories = [
  "Markdown"
]
tags = [
  "Diagram"
]
series = [
  "Docs"
]
+++

Tento článek nabízí ukázku použití základních vývojářských diagramů, které lze použít v souborech s obsahem pro Hugo.

Prosím, více zde [Mermaid](https://mermaid-js.github.io).
<!--more-->

## Flow Chart

{{< mermaid >}}
graph TD
    A[Christmas] -->|Get money| B(Go shopping)
    B --> C{Let me think}
    C -->|One| D[Laptop]
    C -->|Two| E[iPhone]
    C -->|Three| F[fa:fa-car Car]
{{< /mermaid >}}

## Sequence Diagram

{{< mermaid >}}
sequenceDiagram
    Alice->>+John: Hello John, how are you?
    Alice->>+John: John, can you hear me?
    John-->>-Alice: Hi Alice, I can hear you!
    John-->>-Alice: I feel great!
{{< /mermaid >}}

## Class Diagram

{{< mermaid >}}
classDiagram
    Animal <|-- Duck
    Animal <|-- Fish
    Animal <|-- Zebra
    Animal : +int age
    Animal : +String gender
    Animal: +isMammal()
    Animal: +mate()
    class Duck{
      +String beakColor
      +swim()
      +quack()
    }
    class Fish{
      -int sizeInFeet
      -canEat()
    }
    class Zebra{
      +bool is_wild
      +run()
    }
{{< /mermaid >}}
