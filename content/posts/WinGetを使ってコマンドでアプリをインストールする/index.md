---
title: 'WinGetを使ってコマンドでアプリをインストールする'
date: 2022-10-05T12:15:20+09:00
tags: ["WinGet"]
draft: false
---

# 前提条件
windows11であること

# 手順
1. Microsoft Store から WinGet をインストールする
   https://www.microsoft.com/store/productId/9NBLGGH4NNS1
2. コマンドプロンプトでアプリをインストールする
    ```powershell
    winget install "Google Chrome"
    ```
# インストールできる主なアプリ
- Google Chrome
- Microsoft Edge
- Microsoft Teams
- Microsoft Office
- Visual Studio Code
- Slack
- Discord
- Docker Desktop
- Git
- などなど

### 参考
[winget ツールを使用したアプリケーションのインストールと管理](https://learn.microsoft.com/ja-jp/windows/package-manager/winget/)