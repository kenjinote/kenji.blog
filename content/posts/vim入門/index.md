---
title: 'vim入門'
date: 2024-04-19T22:06:34+09:00
tags: ["vim", "テキストエディタ"]
draft: false
cover:
  image: "img.png"
  relative: true
---

![img_1.png](img_1.png)

# vim入門

## ダウンロードとインストール

[https://www.vim.org/download.php](https://www.vim.org/download.php)

上記のサイトから、インストールしたいOSに合わせてモジュールをダウンロードおよびインストールします。

Windowsの場合は`gvim_X.X.X_x64_signed.exe`を選ぶとよいと思います。

##  起動方法

Windowsの場合は環境変数に`vim.exe`があるフォルダーをPathに登録しておく必要があります。

起動方法

```
vim
```

ファイル名を指定して起動する場合

```
vim filename.txt
```

## 終了方法

終了する場合は`:`(コロン)を入力後、`q`を入力して、Enterを入力
```
:q
```

ファイルを更新していた場合は`最後の変更が保存されていません（！を追加で変更を破棄）`と表示されます。
内容を破棄して強制的に終了することができます。
```
:q!
```

ファイルを書き込んで終了する場合は
```
:wq
```

下記でも同じ意味となります。
```
:x
```

また、`Shift`を押しながら`z`を2回押すことでも終了できます。（:wqと同じ）
