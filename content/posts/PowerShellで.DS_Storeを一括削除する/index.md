---
title: 'PowerShellで.DS_Storeを一括削除する'
date: 2022-09-12T10:11:42+09:00
tags: ["PowerShell"]
draft: false
cover:
  image: "img.png"
  relative: true
---
カレントディレクトリを対象のフォルダーに移動し、以下のコマンドを実行する。
```powershell
Get-ChildItem . -include '._*','.DS_Store' -Recurse -Force | Remove-Item -Force
```
