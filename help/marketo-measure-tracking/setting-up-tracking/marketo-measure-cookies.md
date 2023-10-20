---
unique-page-id: 18874590
description: 「[!DNL Marketo Measure] の Cookie - [!DNL Marketo Measure] - 製品ドキュメント」
title: 「[!DNL Marketo Measure] クッキー」
exl-id: de6e35ae-af92-43ba-8416-3e07d3dd470c
feature: Tracking
source-git-commit: 69304dddf3569cd92c95a50e9a2e346acdad0f43
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 42%

---

# Marketo Measure の Cookie {#marketo-measure-cookies}

[!DNL Marketo Measure] の JavaScript をランディングページに適用する際に、サイトに読み込まれる様々な [!DNL Marketo Measure] の Cookie について説明します。この情報は、実装時に web 開発チームに役立つ場合があります。

<table>
<thead>
  <tr>
    <th>cookie 名</th>
    <th>cookie タイプ</th>
    <th>目的</th>
    <th>有効期限</th>
    <th>セキュアフラグが設定されているか。<br></th>
    <th>HTTP のみのフラグが設定されていますか？</th>
    <th>Cookie Setter</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>_biz_uid</td>
    <td>ファーストパーティ</td>
    <td>現在のドメインでユーザーを一意に識別します。</td>
    <td>1 年</td>
    <td>いいえ</td>
    <td>いいえ</td>
    <td>bizible.js</td>
  </tr>
  <tr>
    <td>_biz_nA</td>
    <td>ファーストパーティ</td>
    <td>内部診断のためのすべてのリクエストにMarketo Measureが含めるシーケンス番号。</td>
    <td>1 年</td>
    <td>いいえ</td>
    <td>いいえ</td>
    <td>bizible.js</td>
  </tr>
  <tr>
    <td>_biz_flagsA</td>
    <td>ファーストパーティ</td>
    <td>フォーム送信、クロスドメイン移行、ビュースルーピクセル、オプトアウトステータスの追跡など、様々なユーザー情報を保存する cookie。</td>
    <td>1 年</td>
    <td>いいえ</td>
    <td>いいえ</td>
    <td>bizible.js</td>
  </tr>
  <tr>
    <td>_biz_pendingA</td>
    <td>ファーストパーティ</td>
    <td>分析データは、Marketo Measureサーバーに正常に送信されるまで一時的に保存されます。</td>
    <td>1 年</td>
    <td>いいえ</td>
    <td>いいえ</td>
    <td>bizible.js</td>
  </tr>
  <tr>
    <td>_biz_ABTestA</td>
    <td>ファーストパーティ</td>
    <td>Optimizely および Visual Web Optimizer ABTests のデータが既にレポートされている場合に、bizible.js が収集データを再送信できないようにするチェックサムのリスト。</td>
    <td>1 年</td>
    <td>いいえ</td>
    <td>いいえ</td>
    <td>bizible.js</td>
  </tr>
  <tr>
    <td>_biz_EventA</td>
    <td>ファーストパーティ</td>
    <td>bizible.js が収集したデータを再送信するのを防ぐために Bizible イベントが報告したチェックサムのリスト。</td>
    <td>1 年</td>
    <td>いいえ</td>
    <td>いいえ</td>
    <td>bizible.js</td>
  </tr>
  <tr>
    <td>_biz_su</td>
    <td>ファーストパーティ</td>
    <td>複数のドメインにわたってユーザーを識別するユニバーサルユーザー ID。ITP の制限を回避し、統合をおこなったテナントにのみ適用できます。</td>
    <td>1 年</td>
    <td>はい</td>
    <td>いいえ</td>
    <td>Edgecast</td>
  </tr>
  <tr>
    <td>_BUID</td>
    <td>サードパーティ、domain=.<a href="http://bizible.com/">bizible.com</a></td>
    <td>複数のドメインをまたいでユーザーを識別するためのユニバーサルユーザー ID。</td>
    <td>1 年</td>
    <td>はい</td>
    <td>いいえ</td>
    <td>Edgecast</td>
  </tr>
  <tr>
    <td>_BUID</td>
    <td>サードパーティ、domain=.<a href="http://bizibly.com/">bizibly.com</a></td>
    <td>テナントのドメインのMarketo Measure Cookie ID とその Doubleclick インプレッション Cookie ID とのマッピング。</td>
    <td>1 年</td>
    <td>はい</td>
    <td>いいえ</td>
    <td>Edgecast</td>
  </tr>
</tbody>
</table>

JavaScript の設定中に Web Application Firewall（WAF）の警告がトリガーされた場合、ユーザーは、次の例に示すように、その WAF ルールを無効にするか、Cookie を許可リストに登録することができます。

![](assets/marketo-measure-cookies-1.png)
