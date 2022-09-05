---
title: 'Rustのはじめかた'
date: 2022-09-06T00:12:36+09:00
tags: ["Rust"]
draft: false
---

![](./images/rust_logo.png)

# はじめに
Rustは高速でかつメモリ効率が高いモジュールをモダンな記法で記述できる比較的新しいプログラミング言語です。
マルチプラットフォームに対応しており、WebAssemblyや組み込みの世界でも使われています。
有名なところでは、Firefoxや、DropBox、Cloudflareでも採用されています。

C++の代用としても注目されています。

# インストール方法

[Rust をインストール](https://www.rust-lang.org/ja/tools/install)

上記サイトから各プラットフォーム向けにインストール方法が公開されています。

# 初めてのプログラム

次のプログラムを`main.rs`として保存します。

```
fn main() {
    println!("Hello, world!");
}
```

コマンドプロンプトまたはターミナルから`rustc main.rs`を実行すると、
コンパイルされ、`./main`（Windowsの場合は`main.exe`）を実行すると`Hello, world!`と出力されます。
