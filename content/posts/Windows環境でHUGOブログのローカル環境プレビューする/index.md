---
title: 'Window環境でHUGブログをローカルプレビューする'
date: 2022-09-05T12:28:01+09:00
tags: ["HUGO"]
draft: false
---

# HUGOのインストール
[HUGOのダウンロード](https://github.com/gohugoio/hugo/releases)

上記のサイトから、Windowsのモジュールをダウンロードして展開する。
hugo.exeをC:\bin等にコピーして環境変数でパスを通す。

# ブログをプレビューする
コマンドプロンプトでHUGOブログのフォルダに移動して、下記のコマンドを実行する。

`hugo server -D`

実行結果は下記

```
C:\Users\win11\IdeaProjects\kenji.blog>hugo server -D
Start building sites …
hugo v0.102.3-b76146b129d7caa52417f8e914fc5b9271bf56fc windows/amd64 BuildDate=2022-09-01T10:16:19Z VendorInfo=gohugoio

                   | JA
-------------------+-----
Pages            | 39
Paginator pages  |  0
Non-page files   |  7
Static files     |  0
Processed images |  0
Aliases          | 13
Sitemaps         |  1
Cleaned          |  0

Built in 161 ms
Watching for changes in C:\Users\win11\IdeaProjects\kenji.blog\{archetypes,content,themes}
Watching for config changes in C:\Users\win11\IdeaProjects\kenji.blog\config.toml
Environment: "development"
Serving pages from memory
Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
Web Server is available at http://localhost:1313/ (bind address 127.0.0.1)
Press Ctrl+C to stop
```

アドレスは実行時に出力されるので、ブラウザにアドレスをコピーする。
プレビューはファイルがこうされるたびに自動更新される。
プレビュー終えるにはコマンドプロンプトでCtrl+Cを入力する。
