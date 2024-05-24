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

{{<mermaid align="center">}}
graph TD

A[お正月] -->|お年玉をゲット| B(買い物に行くよ)
B --> C{どれにしようかな}
C -->|これかな| D[iTunes Card]
C -->|これかな| E[iPhone XS Max]
C -->|ま まさか| F[fa:fa-car The CLS Coupé]
{{< /mermaid >}}