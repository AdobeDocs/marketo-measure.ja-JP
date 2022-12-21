---
unique-page-id: 18874570
description: Marketo Measure Framework - Marketo Measure — 製品ドキュメント
title: Marketo Measure Framework
exl-id: fa6de27c-cdd2-4fd9-ac35-7286fe2752d8
source-git-commit: 7eb5ef616e3ae77d53056496f9a1b301ce59d6ee
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Marketo Measure Framework {#marketo-measure-framework}

Marketo Measure フレームワークを構成する 4 つの主要なコンポーネントについて詳しく説明します。 Marketo Measure は、これらのアプリケーションを利用して、データの追跡、整理、および社内データの管理を行い、レポート機能を提供します。 Marketo Measure のフレームワークを構成する 4 つのコンポーネントを次に示します。

* Marketo Measure の JavaScript
* CRM 統合
* サードパーティのアプリケーション/システム
* Marketo Measure Application

## Marketo JavaScript の測定 {#marketo-measure-javascript}

Marketo Measure JavaScript は、見込み客やリードが組織に持つすべてのオンラインマーケティングインタラクション（タッチポイントとも呼ばれる）を追跡します。 これは、終了の前に追加されるカスタムスクリプトです `</head>` タグを Web サイトのすべてのページに追加する必要があります。

`<script type="text/javascript" src="//[cdn.bizible.com/scripts/bizible.js](http://cdn.bizible.com/scripts/bizible.js)" async=""></script>`

>[!NOTE]
>
>Marketo Measure JS を追加する手順については、 [ここをクリック](/help/marketo-measure-tracking/setting-up-tracking/adding-marketo-measure-script.md).

Marketo Measure の JS は、Web 訪問（匿名の Web 訪問を含む）、一般的なトラフィック/ページナビゲーション、コンテンツのダウンロード、フォーム送信からデータを取り込みます。 このデータは CRM にプッシュされ、各マーケティングインタラクションがタッチポイントとして表示されます。

## CRM 統合 {#crm-integrations}

Marketo Measure は CRM と統合され、Marketo Measure JS でキャプチャされたすべてのデータを保管および整理します。 現在、Marketo Measure には 2 つの CRM との API 統合があります。

![](assets/1-2.png)

Marketoの測定データを CRM で表示すると、各タッチポイントに関する詳細な情報を確認し、レポートを生成して、チャネルのパフォーマンスを把握できます。

## サードパーティアプリケーション {#third-party-applications}

ほとんどのマーケターは、マーケティング活動を実行するために、様々なアプリケーションに依存しています。 Marketo Measure は、Salesforce および MS Dynamics に加えて、13 のサードパーティアプリケーション（以下に示す）と統合されています。

![](assets/2-1.png)

上記のアプリケーションを使用してマーケティング活動を実行している場合は、これらのアカウントをMarketo Measure アカウントにリンクできます。 これにより、データの追跡とMarketo Measure アカウントへの転送が簡単になります。

## Marketo Measure Application {#marketo-measure-application}

Marketo Measure アプリケーションは、アトリビューションデータの表示とレポート、アカウント設定の指定、およびアカウント情報の更新に使用します。 Marketo Measure アプリの主なメニュー項目は次のとおりです。

**アカウント構成**

ここで、会社の一般情報を更新し、Marketo Measure JavaScript にアクセスできます。

**設定**

このメニュー項目を使用すると、アトリビューションとチャネルマッピングの設定、CRM およびサードパーティアプリケーションとの統合の管理、Marketoメジャーアカウントユーザーの表示/追加、請求情報の更新をおこなうことができます。

**マーケティング ROI ダッシュボード**

マーケティング ROI ダッシュボードのメニュー項目を使用すると、チャネルのパフォーマンス、アクティビティ、コストの観点からデータを視覚化できます。
