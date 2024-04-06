---
title: 'エクスプローラーの終了・再起動方法'
date: 2024-03-30T15:40:24+09:00
tags: ["エクスプローラー"]
draft: false
cover:
  image: "img_2.png"
  relative: true
---

## タスクバーの右クリックから終了する方法

こちらはWindows 10での方法です。Windows 11ではメニューが表示されないようです。
タスクバーでShiftキーとCtrlキーを押しながら右クリックをすると、メニューに「エクスプローラーの終了」が表示されます。

![img.png](img.png)

## タスクマネージャーから終了する方法

1. Ctrl + Shift + Esc キーを押してタスクマネージャーを起動します。
2. プロセスタブを選択します。

![img_3.png](img_3.png)

3. `explorer.exe` を選択し、Deleteキーを押下し、`explorer.exe を終了しますか？`と聞かれるので、`プロセスの終了`を選択します。

![img_1.png](img_1.png)

## コマンドプロンプトから終了する方法

1. Win + R キーを押して、`cmd` と入力し、Enterキーを押します。
2. `taskkill /f /im explorer.exe` と入力し、Enterキーを押します。

## タスクマネージャーからエクスプローラを起動する方法

1. Ctrl + Shift + Esc キーを押してタスクマネージャーを起動します。
2. ファイルメニューから、`新しいタスクの実行`を選択します。
3. `explorer.exe` と入力し、Enterキーを押します。