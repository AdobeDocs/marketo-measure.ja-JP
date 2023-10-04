---
unique-page-id: 18874590
description: 「[!DNL Marketo Measure] の Cookie - [!DNL Marketo Measure] - 製品ドキュメント」
title: 「[!DNL Marketo Measure] クッキー」
exl-id: de6e35ae-af92-43ba-8416-3e07d3dd470c
feature: Tracking
source-git-commit: 8ac315e7c4110d14811e77ef0586bd663ea1f8ab
workflow-type: ht
source-wordcount: '205'
ht-degree: 100%

---

# Marketo Measure の Cookie {#marketo-measure-cookies}

[!DNL Marketo Measure] の JavaScript をランディングページに適用する際に、サイトに読み込まれる様々な [!DNL Marketo Measure] の Cookie について説明します。この情報は、実装時に web 開発チームに役立つ場合があります。

| **cookie 名** | **cookie タイプ** | **目的** |
|---|---|---|
| _BUID | サードパーティ、.bizible.com ドメインに保存 | 複数のクライアントのドメイン間で同じユーザーを識別するユニバーサルユーザー ID です。 |
| _biz_uid | ファーストパーティ | 現在のドメインのユーザー ID です。 |
| _biz_sid | ファーストパーティ | ユーザーのセッション ID です。 |
| _biz_flagsA | ファーストパーティ | ユーザーがフォームを送信したかどうか、クロスドメイン移行を実行したかどうか、ビュースルーピクセルを送信したかどうか、トラッキングをオプトアウトしたかどうかなど、複数の情報を保存する単一の cookie です。 |
| _biz_nA | ファーストパーティ | 内部診断目的で、[!DNL Marketo Measure] がすべてのリクエストに含めるシーケンス番号です。 |
| _biz_dfsA | ファーストパーティ | [!DNL bizible.js] が設定 JS を受信して HTTPS でのフォームのトラッキングが有効かどうかを判断する前に発生するフォーム送信データを一時的に保存します。 |
| _biz_pendingA | ファーストパーティ | まだ [!DNL Marketo Measure] サーバーに正常に送信されていない分析データを一時的に保存します。 |

JavaScript の設定中に Web Application Firewall（WAF）の警告がトリガーされた場合、ユーザーは、次の例に示すように、その WAF ルールを無効にするか、Cookie を許可リストに登録することができます。

![](assets/marketo-measure-cookies-1.png)
