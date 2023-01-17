---
title: 'HUGOでHTMLタグを使う'
date: 2022-01-01T00:00:00+09:00
tags: ["HUGO", "HTML"]
draft: false
cover:
  image: "img.png"
  relative: true
---

HUGOではデフォルトでは、記事中にHTMLタグの使用ができなくなっていますが、config.tomlに下記の記述をするとできるようになります。

```toml
[markup]
  [markup.goldmark]
    [markup.goldmark.renderer]
      unsafe = true
```

参考: [Configure Markup](https://gohugo.io/getting-started/configuration-markup)
