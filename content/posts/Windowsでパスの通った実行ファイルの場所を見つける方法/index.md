---
title: 'Windowsでパスの通った実行ファイルの場所を見つける方法'
date: 2023-04-03T00:02:55+09:00
tags: ["Windows", "パス", "実行ファイル"]
draft: false
cover:
  image: "img.png"
  relative: true
---

# Windowsでパスの通った実行ファイルの場所を見つける方法

実行ファイルを指定してコマンドを実行するとき、その実行ファイルががどこにあるのかを知りたいときがあります。そんな時は下記のコマンドで実行ファイルの場所を調べることができます。

```powershell
where.exe <実行ファイル名>
```
# 参考

- [How do I find the location of an executable in Windows?](https://superuser.com/questions/49104/how-do-i-find-the-location-of-an-executable-in-windows)