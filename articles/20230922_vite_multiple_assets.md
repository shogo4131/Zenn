---
title: "Viteでbuildした際に出力されるassetsディレクトリ構造をキープする"
emoji: "⚡️"
type: "tech"
topics: ["Vite"]
published: false
---

## 背景 / 課題

Snowpack のメンテナンスが 2022 年 4 月に終了し、それに伴い React アプリケーションを Vite に移行しました。
インフラ周りは CloudFront + S3 で画像などは S3 に保存されています。
この S3 に保存されているファイルパスを元に別で API を作成しています。
問題は Snowpack から Vite に移行した際に、 src/assets/\*にあるサブディレクトリ[^1]が削除され、画像ファイルが dist/assets/\*[^2]に一括に出力され、API で画像が取得できない状態になりました。

[^1]: ![ディレクトリ構造](/images/vite_multiple_assets/directory_structer.png)
[^2]: ![ディレクトリ構造](/images/vite_multiple_assets/export_images.png)

実現したい事としては、[^1]のようにサブディレクトリを残したまま build で export させる事です。
本記事ではその方法について記載していきます。
尚、設計についてのツッコミは自分も思うことがありますが、参画した時からこの設計だったので一番工数がかからない方法でやってます。
設計に関する質問は受け付けませんのでご了承ください。

## 調査

## 実装方法

## ライブラリ
