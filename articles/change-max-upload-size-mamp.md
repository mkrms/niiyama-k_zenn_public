---
title: "MAMPによるWordPress開発環境の最大アップロード容量を変更する"
emoji: "🌟"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["MAMP", "WordPress", "PHP"]
published: false
---

## MAMPのデフォルト最大アップロード容量による制限
All-in-one wp migration によって 本番環境 → 開発環境へインポートする際に、"デフォルト容量 8MB だから受け付けられんわ！" と怒られたので変更した。

## 変更手順
MAMP / bin / php / php{version} / conf / php.ini ←これをいじる
（※ php{version} は php7.4.33 など、使用しているversionのファイルを見る）

``` memory_limit ```
``` post_max_size ```
``` upload_max_filesize ```

↑をそれぞれ検索かけて、500MBくらいにしとく。
