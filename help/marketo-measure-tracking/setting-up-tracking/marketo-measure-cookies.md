---
unique-page-id: 18874590
description: '"[!DNL Marketo Measure] Cookie - [!DNL Marketo Measure]  — 製品ドキュメント»'
title: "[!DNL Marketo Measure] クッキー"
exl-id: de6e35ae-af92-43ba-8416-3e07d3dd470c
source-git-commit: 3a13ab3e497652d1975e69280a3d224ac95504aa
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---

# Marketoの測定の cookie {#marketo-measure-cookies}

様々な [!DNL Marketo Measure] 適用時にサイトに読み込まれる cookie [!DNL Marketo Measure] JavaScript をランディングページに追加します。 この情報は、実装時に Web 開発チームに役立つ場合があります。

| **Cookie 名** | **Cookie のタイプ** | **目的** |
|---|---|---|
| _BUID | .bizible.com ドメインに保存されたサードパーティ | 複数のクライアントのドメインをまたいで同じユーザーを識別するユニバーサルユーザー ID。 |
| _biz_uid | ファーストパーティ | 現在のドメインのユーザー ID。 |
| _biz_sid | ファーストパーティ | ユーザーのセッション ID。 |
| _biz_flagsA | ファーストパーティ | ユーザーがフォームを送信したかどうか、クロスドメイン移行を実行したか、ビュースルーピクセルを送信したか、トラッキングをオプトアウトしたかなど、複数の情報を保存する単一の Cookie。 |
| _biz_nA | ファーストパーティ | シーケンス番号 [!DNL Marketo Measure] すべてのリクエストに含まれ、内部診断用に |
| _biz_dfsA | ファーストパーティ | 以前に発生したフォーム送信データを一時的に保存する [!DNL bizible.js] は、設定 JS を受け取り、HTTPS でのトラッキングフォームが有効かどうかを判定します。 |
| _biz_pendingA | ファーストパーティ | に正常に送信されなかった分析データを一時的に保存する [!DNL Marketo Measure] サーバーを使用しています。 |

JavaScript の設定中に Web Application Firewall(WAF) 警告がトリガーされた場合、次の例に示すように、ユーザーは WAF ルールを無効にするか、Cookie を許可リストに登録できます。

![](assets/marketo-measure-cookies-1.png)
