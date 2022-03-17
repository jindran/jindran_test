+++
author = "Hugo Authors"
title = "Podpora emotikonů"
date = "2019-03-05"
description = "Jak používat emotikony (emoji) v Hugovi"
categories = [
]
tags = [
    "Emoji",
]
+++

Emoji lze v projektu Hugo povolit mnoha způsoby.
<!--more-->
[`emojify`](https://gohugo.io/functions/emojify/) funkci lze volat přímo v šablonách popř. [Inline Shortcodes](https://gohugo.io/templates/shortcode-templates/#inline-shortcodes). 

Chcete-li povolit emotikony globálně, nastavte `enableEmoji` na `true` ve Vaší website [konfiguraci](https://gohugo.io/getting-started/configuration/) a pak můžete psát zkrácené kódy emoji přímo do souborů obsahu; např.

<p><span class="nowrap"><span class="emojify">🙈</span> <code>:see_no_evil:</code></span>  <span class="nowrap"><span class="emojify">🙉</span> <code>:hear_no_evil:</code></span>  <span class="nowrap"><span class="emojify">🙊</span> <code>:speak_no_evil:</code></span></p>
<br>

[Emoji cheat sheet](http://www.emoji-cheat-sheet.com/) je užitečný odkaz na zkrácené kódy emodži.
***

**Pozn.:** Výše uvedené kroky povolují znaky a sekvence emodži Unicode Standard v Hugo, avšak vykreslování těchto glyfů závisí na prohlížeči a platformě. Chcete-li upravit styl emotikonu, můžete použít písmo emodži třetí strany nebo zásobník písem; např.

{{< highlight html >}}
.emoji {
  font-family: Apple Color Emoji, Segoe UI Emoji, NotoColorEmoji, Segoe UI Symbol, Android Emoji, EmojiSymbols;
}
{{< /highlight >}}

{{< css.inline >}}
<style>
.emojify {
	font-family: Apple Color Emoji, Segoe UI Emoji, NotoColorEmoji, Segoe UI Symbol, Android Emoji, EmojiSymbols;
	font-size: 2rem;
	vertical-align: middle;
}
@media screen and (max-width:650px) {
  .nowrap {
    display: block;
    margin: 25px 0;
  }
}
</style>
{{< /css.inline >}}
