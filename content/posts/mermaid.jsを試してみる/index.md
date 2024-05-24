---
title: 'mermaid.jsを試してみる'
date: 2024-05-25T02:18:09+09:00
tags: ["mermaid.js"]
draft: false
mermaid: true
cover:
  image: "img.png"
  relative: true
---

## hugoでmermaid.jsを試してみます。

手順は以下の通りです。
1. layouts/partials/extend_head.htmlに以下を追加

```html
{{ if or .Params.mermaid .Site.Params.mermaid }}
<script src="https://cdn.jsdelivr.net/npm/mermaid@10.9.1/dist/mermaid.min.js"></script>
{{ end }}
```

2. layouts/shortcodes/mermaid.htmlを作成

```html
<div class="mermaid" align="{{ if .Get "align" }}{{ .Get "align" }}{{ else }}center{{ end }}">
    {{ safeHTML .Inner }}
</div>
```
3. 記事を書く
記事の定義に下記を追加
```dtd
marmaid: true
```
記事の本文に下記を追加
```markdown
{{</*mermaid align="center"*/>}}
graph TD

A[開始] -->|条件1| B(条件2)
B --> C{条件3}
C -->|条件4| D[終了]
{{</*/mermaid*/>}}
```

{{<mermaid align="center">}}
graph TD

A[開始] -->|条件1| B(条件2)
B --> C{条件3}
C -->|条件4| D[終了]
{{</mermaid>}}

以上です。

### 参考
- [mermaid.js](https://mermaid.js.org/#/)
