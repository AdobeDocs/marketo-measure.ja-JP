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

Marketo Measureフレームワークを構成する 4 つの主要なコンポーネントについて詳しく説明します。 Marketo Measureは、これらのアプリケーションを利用して、データの追跡、整理、および社内データの管理、およびレポート機能の提供を行っています。 Marketo Measureのフレームワークを構成する 4 つのコンポーネントは、次のとおりです。

* Marketo Measure JavaScript の使用
* CRM 統合
* サードパーティのアプリケーション/システム
* Marketo Measure Application

## Marketo Measure JavaScript {#marketo-measure-javascript}

Marketo Measure JavaScript は、見込み客やリードが組織に持つすべてのオンラインマーケティングインタラクション（タッチポイントとも呼ばれます）を追跡します。 これは、終了の前に追加されるカスタムスクリプトです `</head>` タグを Web サイトのすべてのページに追加する必要があります。

`<script type="text/javascript" src="//[cdn.bizible.com/scripts/bizible.js](http://cdn.bizible.com/scripts/bizible.js)" async=""></script>`

>[!NOTE]
>
>Marketo Measure JS の追加方法については、 [ここをクリック](/help/marketo-measure-tracking/setting-up-tracking/adding-marketo-measure-script.md).

Marketo Measureの JS は、Web 訪問（匿名の Web 訪問を含む）、一般的なトラフィック/ページナビゲーション、コンテンツのダウンロード、フォーム送信からデータをキャプチャします。 このデータは CRM にプッシュされ、各マーケティングインタラクションがタッチポイントとして表示されます。

## CRM 統合 {#crm-integrations}

Marketo Measureは CRM と統合され、Marketo Measure JS によってキャプチャされたすべてのデータを保存および整理します。 現在、Marketo Measureには 2 つの CRM との API 統合があります。

![](assets/1-2.png)

CRM でMarketo Measureのデータを表示することで、各タッチポイントに関する詳細な情報を確認し、レポートを生成して、チャネルのパフォーマンスを把握できます。

## サードパーティアプリケーション {#third-party-applications}

ほとんどのマーケターは、マーケティング活動を実行するために、様々なアプリケーションに依存しています。 Marketo Measureは、Salesforce および MS Dynamics に加えて、13 のサードパーティアプリケーション（以下に示す）と統合されています。

![](assets/2-1.png)

上記のアプリケーションを使用してマーケティング活動を行っている場合は、これらのアカウントをMarketo Measureアカウントにリンクできます。 これにより、データの追跡とMarketo Measureアカウントへの転送が簡単になります。

## Marketo Measure Application {#marketo-measure-application}

Marketo Measureアプリケーションは、アトリビューションデータの表示とレポート、アカウント設定、およびアカウント情報の更新に使用されます。 Marketo Measureアプリの主なメニュー項目は次のとおりです。

**アカウント構成**

ここで、会社の一般情報を更新し、Marketo Measure JavaScript にアクセスできます。

**設定**

このメニュー項目を使用すると、アトリビューションとチャネルマッピングの設定、CRM およびサードパーティアプリケーションとの統合の管理、Marketo Measureアカウントユーザーの表示/追加、請求情報の更新をおこなうことができます。

**マーケティング ROI ダッシュボード**

マーケティング ROI ダッシュボードのメニュー項目を使用すると、チャネルのパフォーマンス、アクティビティ、コストの観点からデータを視覚化できます。
