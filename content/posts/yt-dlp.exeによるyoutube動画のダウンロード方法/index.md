---
title: 'yt-dlp.exeによるYouTube動画のダウンロード方法'
date: 2024-09-03T14:09:26+09:00
tags: ["YouTube", "ダウンロード"]
draft: false
cover:
  image: "yt-dlp.png"
  relative: true
---

# yt-dlp.exeによるYouTube動画のダウンロード方法

yt-dlpは、YouTube動画をダウンロードするためのコマンドラインツールです。
yt-dlpは、YouTube-dlのフォークであり、より多くの機能とサポートを提供しています。

## インストール

1. [yt-dlpのリリースページ](https://github.com/yt-dlp/yt-dlp/releases)から最新のyt-dlp.exeをダウンロードします。
2. yt-dlp.exeを任意のフォルダに配置します。
3. yt-dlp.exeのフォルダパスを環境変数Pathに追加します。

## 使用方法

yt-dlp.exeをコマンドプロンプトで実行し、YouTube動画のURLを指定します。

```
yt-dlp.exe "https://www.youtube.com/watch?v=VIDEO_ID"
```
※引数は VIDEO_ID の部分だけでもOKです。

音楽ファイルmp3としてダウンロードする場合は、以下のコマンドを実行します。

```
yt-dlp.exe --extract-audio --audio-format mp3 --embed-thumbnail --add-metadata "https://www.youtube.com/watch?v=VIDEO_ID"
```

これで、コマンドを実行したカレントディレクトリに動画がダウンロードされます。

以上。

