---
title: 'SOQLで日ごとの作成されたレコード数を取得する'
date: 2023-04-09T02:50:30+09:00
tags: ["salesforce", "soql", "日付", "集計"]
draft: false
cover:
  image: "img.png"
  relative: true
---

# SOQLで日ごとの作成されたレコード数を取得する

1. 開発者コンソールを開く
2. `Query Editor`タブを開く
3. 下記のSOQLを貼り付けて実行する。
```sql
select day_only(createdDate), count(createdDate) from account group by day_only(createdDate) order by count(createdDate) desc limit 10
```
`account`は取得したい任意のオブジェクト名に変えて実行してください。

# 参考
- [Is there a way to group by the date portion of a datetime field in SOQL?](https://stackoverflow.com/questions/9187737/is-there-a-way-to-group-by-the-date-portion-of-a-datetime-field-in-soql)