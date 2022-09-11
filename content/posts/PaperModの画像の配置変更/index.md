---
title: 'PaperModの画像の配置変更'
date: 2022-09-11T18:50:40+09:00
tags: ["HUGO", "PaperMod"]
draft: false
cover:
  image: "images/img.png"
  relative: true
---
PaperModの画像の配置を変更しました。変更箇所は下記となります。

## post-entry.css

```css:post-entry.css
.entry-content {
    margin: 8px 0;
    color: var(--secondary);
    font-size: 14px;
    line-height: 1.6;
    overflow: hidden;
    display: -webkit-box;
    -webkit-box-orient: vertical;
    // -webkit-line-clamp: 2; // 2 → 4 に変更
    -webkit-line-clamp: 4; // 2 → 4 に変更
}

.entry-footer {
    color: var(--secondary);
    font-size: 13px;
	text-align: right; // 追加
}

.entry-cover {
    // margin-bottom: var(--gap); // 削除
    text-align: center;
}

.entry-cover img {
    // border-radius: var(--radius); // 削除
    border-radius: 4px; // 追加
    pointer-events: none;
    // width: 100%; // 削除
    display: inline; // 追加
    max-width: 100%; // 追加
    height: auto;
}
```

## list.html

```html:list.html
<article class="{{ $class }}">
  <!-- {{- $isHidden := (site.Params.cover.hidden | default site.Params.cover.hiddenInList) }} --><!-- 下に移動 -->
  <!-- {{- partial "cover.html" (dict "cxt" . "IsHome" true "isHidden" $isHidden) }} --><!-- 下に移動 -->
  <header class="entry-header">
    <h2>
      {{- .Title }}
      {{- if .Draft }}<sup><span class="entry-isdraft">&nbsp;&nbsp;[draft]</span></sup>{{- end }}
    </h2>
  </header>
  <div style="display:flex;"><!-- 追加 -->
    <div style="max-width:150px;margin: 11px 15px 0px 0px;"><!-- 追加 -->
      {{- $isHidden := (site.Params.cover.hidden | default site.Params.cover.hiddenInList) }}<!-- 上から移動 -->
      {{- partial "cover.html" (dict "cxt" . "IsHome" true "isHidden" $isHidden) }}<!-- 上から移動 -->
    </div><!-- 追加 -->
    {{- if (ne (.Param "hideSummary") true) }}
    <div style="width:100%;"><!-- 追加 -->
      <div class="entry-content">
        <p>{{ .Summary | plainify | htmlUnescape }}{{ if .Truncated }}...{{ end }}</p>
      </div>
      {{- end }}
      {{- if not (.Param "hideMeta") }}
      <footer class="entry-footer">
        {{- partial "post_meta.html" . -}}
      </footer>
      {{- end }}
      <a class="entry-link" aria-label="post link to {{ .Title | plainify }}" href="{{ .Permalink }}"></a>
    </div><!-- 追加 -->
  </div><!-- 追加 -->
</article>
```

他に変えたところあったかなぁ・・・？