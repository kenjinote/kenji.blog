---
title: 'mermaid.jsを試してみる'
date: 2024-05-25T02:18:09+09:00
tags: ["mermaid.js"]
draft: false
mermaid: true
cover:
  image: "img_2.png"
  relative: true
---

## mermaid.jsとは

mermaid.jsは、JavaScriptのライブラリで、テキストベースの独自の構文(Mermaid記法)を記述し、フローチャートやダイヤグラム、ガントチャートなど、複雑な図表をグラフィカルに表示できます。
GitHubやQiita、Notionなど、いろいろなサービスでも採用されています。今回は、hugoでmermaid.jsを使えるようにしてみます。

## hugoでmermaid.jsを使えるようにする

手順は以下の通りです。

1. layouts/partials/extend_head.htmlに以下を追加。

```html
{{ if or .Params.mermaid .Site.Params.mermaid }}
<script src="https://cdn.jsdelivr.net/npm/mermaid@10.9.1/dist/mermaid.min.js"></script>
{{ end }}
```
※if文で`mermaid: true`とした場合のみ`mermaid.min.js`を読み込むようにしています。このライブラリは3MBほどあり意外と大きい。

2. layouts/shortcodes/mermaid.htmlを作成

```html
<div class="mermaid" align="{{ if .Get "align" }}{{ .Get "align" }}{{ else }}center{{ end }}">
  {{ safeHTML .Inner }}
</div>
```

以上でmermaid.jsを使える準備が整いました。

## mermaid.jsを使ってみる

1. 記事の定義に下記を追加

```dtd
marmaid: true
```

2. 記事の本文に下記を追加

**フローチャート**

```markdown
{{</*mermaid align="center"*/>}}
graph TD

A[開始] -->|条件1| B(条件2)
B --> C{条件3}
C -->|条件4| D[終了]
{{</*/mermaid*/>}}
```

**出力結果**

{{<mermaid align="center">}}
graph TD

A[開始] -->|条件1| B(条件2)
B --> C{条件3}
C -->|条件4| D[終了]
{{</mermaid>}}

**ガントチャート**

```markdown
{{</*mermaid align="center"*/>}}
gantt
title A Gantt Diagram
dateFormat  YYYY-MM-DD
section Section
A task           :a1, 2024-05-25, 30d
Another task     :after a1  , 20d
section Another
Task in sec      :2014-01-01  , 12d
another task      : 24d
{{</*/mermaid*/>}}
```

**出力結果**

{{<mermaid align="center">}}
gantt
    title A Gantt Diagram
    dateFormat  YYYY-MM-DD
    section Section
    A task           :a1, 2024-05-25, 30d
    Another task     :after a1  , 20d
    section Another
    Task in sec      :2024-04-01  , 12d
    another task      : 24d
{{</mermaid>}}

以上です。

### 参考
- [mermaid.js](https://mermaid.js.org/#/)
- [mermaid.live](https://mermaid.live/)
