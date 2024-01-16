---
unique-page-id: 18874590
description: 「[!DNL Marketo Measure] の Cookie - [!DNL Marketo Measure] - 製品ドキュメント」
title: 「[!DNL Marketo Measure] クッキー」
exl-id: de6e35ae-af92-43ba-8416-3e07d3dd470c
feature: Tracking
source-git-commit: 327daa56fe1b346d067f2e0fb39006b91e6849ee
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 74%

---

# Marketo Measure の Cookie {#marketo-measure-cookies}

[!DNL Marketo Measure] の JavaScript をランディングページに適用する際に、サイトに読み込まれる様々な [!DNL Marketo Measure] の Cookie について説明します。この情報は、実装時に web 開発チームに役立つ場合があります。

>[!IMPORTANT]
>
>プライバシーに関する問題により、サードパーティ Cookie は廃止されます。 Google Chrome が 2024 年第 3 四半期に発表したサードパーティ cookie の廃止は、この形式のトラッキングの終了を示します。 その結果、Adobeでは、サードパーティ Cookie に依存するMarketo Measure関数、特にGoogle/DoubleClick インプレッション Cookie を使用するクロスドメイントラッキングとビュースルーアトリビューションは廃止されます。 Marketo Measureのその他の機能に影響はありません。 また、ファーストパーティ Cookie の使用にも影響はありません。 Googleのスケジュールに照らして、上記 2 つの関数の廃止予定日は6/1/2024です。 この日より前に収集された関連データは、Adobeのお客様が引き続き利用できます。

<table>
<thead>
  <tr>
    <th>cookie 名</th>
    <th>cookie タイプ</th>
    <th>目的</th>
    <th>有効期限</th>
    <th>セキュリティで保護されたフラグが設定されていますか？<br></th>
    <th>HTTP のみのフラグが設定されていますか？</th>
    <th>cookie セッター</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>_biz_uid</td>
    <td>ファーストパーティ</td>
    <td>現在のドメインでユーザを一意に識別します。</td>
    <td>1 年</td>
    <td>いいえ</td>
    <td>いいえ</td>
    <td>bizible.js</td>
  </tr>
  <tr>
    <td>_biz_nA</td>
    <td>ファーストパーティ</td>
    <td>内部診断目的で、Marketo Measure がすべてのリクエストに含めるシーケンス番号です。</td>
    <td>1 年</td>
    <td>いいえ</td>
    <td>いいえ</td>
    <td>bizible.js</td>
  </tr>
  <tr>
    <td>_biz_flagsA</td>
    <td>ファーストパーティ</td>
    <td>フォーム送信、クロスドメイン移行、ビュースルーピクセル、トラッキングのオプトアウトステータスなど、様々なユーザ情報を保存する cookie です。</td>
    <td>1 年</td>
    <td>いいえ</td>
    <td>いいえ</td>
    <td>bizible.js</td>
  </tr>
  <tr>
    <td>_biz_pendingA</td>
    <td>ファーストパーティ</td>
    <td>Marketo Measure サーバーに正常に送信されるまで、分析データを一時的に保存します。</td>
    <td>1 年</td>
    <td>いいえ</td>
    <td>いいえ</td>
    <td>bizible.js</td>
  </tr>
  <tr>
    <td>_biz_ABTestA</td>
    <td>ファーストパーティ</td>
    <td>既に報告されている Optimizely および Visual Web Optimizer AB テストデータからのチェックサムのリストです。これにより、bizible.js では収集したデータを再送信できなくなります。</td>
    <td>1 年</td>
    <td>いいえ</td>
    <td>いいえ</td>
    <td>bizible.js</td>
  </tr>
  <tr>
    <td>_biz_EventA</td>
    <td>ファーストパーティ</td>
    <td>bizible.js で収集したデータを再送信するのを防ぐために、Bizible イベントによって報告されるチェックサムのリストです。</td>
    <td>1 年</td>
    <td>いいえ</td>
    <td>いいえ</td>
    <td>bizible.js</td>
  </tr>
  <tr>
    <td>_biz_su</td>
    <td>ファーストパーティ</td>
    <td>複数のドメイン間でユーザを識別するユニバーサルユーザ ID です。ITP 制限をバイパスする統合を備えたテナントにのみ適用されます。</td>
    <td>1 年</td>
    <td>はい</td>
    <td>いいえ</td>
    <td>Edgecast</td>
  </tr>
  <tr>
    <td>_BUID</td>
    <td>サードパーティ、ドメイン =.<a href="http://bizible.com/">bizible.com</a></td>
    <td>複数のドメイン間でユーザを識別するユニバーサルユーザ ID です。</td>
    <td>1 年</td>
    <td>はい</td>
    <td>いいえ</td>
    <td>Edgecast</td>
  </tr>
  <tr>
    <td>_BUID</td>
    <td>サードパーティ、ドメイン =.<a href="http://bizibly.com/">bizibly.com</a></td>
    <td>テナントのドメインの Marketo Measure cookie ID とその Doubleclick インプレッション cookie ID 間のマッピングです。</td>
    <td>1 年</td>
    <td>はい</td>
    <td>いいえ</td>
    <td>Edgecast</td>
  </tr>
</tbody>
</table>

JavaScript の設定中に Web Application Firewall（WAF）の警告がトリガーされた場合、ユーザーは、次の例に示すように、その WAF ルールを無効にするか、Cookie を許可リストに登録することができます。

![](assets/marketo-measure-cookies-1.png)
