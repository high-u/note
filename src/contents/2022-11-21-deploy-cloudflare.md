---
author: High U
datetime: 2022-11-21T23:05:00+09:00
title: Cloudflare にデプロイした
slug: 2022-11-21-deploy-to-cloudflare-pages
featured: false
draft: false
tags:
  - cloudflare
  - deployment
  - nodejs
ogImage: ""
description:
  Cloudflare Pages にデプロイしたら、Node.js のバージョンが古くて失敗した。ログを見たらデプロイに使用している Node.js のバージョンが古かった。
---

## 一発しくったのでその内容

特にドキュメントも見ずに、Cloudflare にサインインして Pages から `Create a project` の `Connect to Git` でデプロイ処理まではいった。  
  
しかし、エラー。  
  
ログを見ると、Node.js のバージョンが `12` で、Astro が対応してないよって。  
なので、環境変数に `NODE_VERSION` を追加し、値を `v16.18.1` で登録した。  
  
`Retry deployment` でもう一度処理してもらったら、OK だったよ。
  
## 参考にさせてもらった記事

- [Cloudflare PagesでNode.jsのバージョンを指定する | DevelopersIO](https://dev.classmethod.jp/articles/cloudflare-pages-node-version/)
- [Build configuration · Cloudflare Pages docs](https://developers.cloudflare.com/pages/platform/build-configuration)
    - 現時点（2022-11-21）では、Node.js のデフォルトバージョンは `12.18.0` 、`17.x` までのバージョンが指定できる、とのこと。今回は環境変数の登録で対応したけど、ファイルでも出来るっぽい。
