+++
title = "Social Links"
date = 2021-12-02T16:27:45+08:00
featured = false
comment = true
toc = true
reward = true
categories = [
  "Social Links"
]
tags = [
]
series = [
  "Docs"
]
images = []
+++

Parametr `social` je sada párů klíčových hodnot sociálních odkazů, které mapují z platformy na jejich identifikátor uživatele.
Podporuje mnoho populárních sociálních platforem, jako je Twitter, Facebook, Reddit, GitHub.
V tomto článku jsou uvedeny všechny podporované platformy a jak je používat.

<!--more-->

## Pou6it9

Existují dvě místa, kam můžete umístit odkazy na sociální sítě, jedno je [Author Widget]({{< ref "/posts/widgets/author" >}}), druhé je zápatí.

### Widget autora

Odkazy na sociální sítě nastavte úpravou souboru `config/_default/author.toml` s následujícím obsahem:

```toml
[social]
  email = "user@domain.tld"
  github = "githubusername"
```

### Zápatí

Odkazy na sociální sítě nastavte vytvořením souboru `config/_default/social.toml` s následujícím obsahem:

```toml
email = "user@domain.tld"
github = "githubusername"
```

## Platformy

| Platform | User Identifier |
|---|---|
| `email` | Emailová adresa |
| `facebook` | Facebook Username |
| `facebookgroup` | Facebook Group Name |
| `github` | GitHub Username |
| `gitlab` | GitLab Username |
| `instagram` | Instagram Username |
| `linkedin` | LinkedIn Username |
| `quora` | Quora Username |
| `stackoverflow` | Stack Overflow User ID |
| `tumblr` | Tumblr Username |
| `twitter` | Twitter Username |
| `weibo` | Weibo Username |
| `zhihu` | Zhihu Username |
| `reddit` | Reddit Username |
| `telegram` | Telegram Username |
| `qq` | QQ Number |
| `dockerhub` | Docker Hub Username |
| `bitbucket` | Bitbucket Workspace ID |
| `kaggle` | Kaggle Username |
| `medium` | Medium Username or custom domain(e.g. https://custom.domain.tld) |
| `lastfm` | Last.fm Username |
| `bibibili` | BiliBili User ID |
| `youtube` | Youtube Channel ID |
| `discord` | Discord Invite Code |
| `discourse` | Forum URL |
| `tiktok` | TikTok Username |
| `pinterest` | Pinterest Username |
