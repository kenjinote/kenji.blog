---
title: '証明書エラーでGitHub Copilotが使えなくなった場合の対処方法'
date: 2024-04-21T18:47:26+09:00
tags: ["GitHub Copilot", ""]
draft: true
cover:
  image: "img.png"
  relative: true
---

# GitHub Copilotで下記のエラーが表示された場合の対処方法

```
[ERROR] [ghostText] [2024-04-21T04:06:46.900Z] Error on ghost text request: (FetchError) unable to verify the first certificate
[ERROR] [certificates] [2024-04-21T04:06:46.901Z] Your current Copilot license doesn't support proxy connections with custom certificates. Please visit https://gh.io/copilot-network-errors to learn more. Original cause: {"type":"system","_name":"FetchError","code":"UNABLE_TO_VERIFY_LEAF_SIGNATURE"}
```

コマンドプロンプトで下記のコマンドを実行

```
npm config set strict-ssl false
```

```
npm i win-ca
```

```
npm config set strict-ssl true
```

## 参考サイト

- [Error: UNABLE_TO_VERIFY_LEAF_SIGNATURE Phonegap Installation](https://stackoverflow.com/questions/20747817/error-unable-to-verify-leaf-signature-phonegap-installation)

