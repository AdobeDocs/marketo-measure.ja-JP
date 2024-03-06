---
unique-page-id: 18874570
description: Marketo Measure フレームワーク - Marketo Measure - 製品ドキュメント
title: Marketo Measure フレームワーク
exl-id: fa6de27c-cdd2-4fd9-ac35-7286fe2752d8
feature: Fundamentals
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 62%

---

# Marketo Measure フレームワーク {#marketo-measure-framework}

Marketo Measure フレームワークを構成する 4 つのメインコンポーネントについて詳しく説明します。Marketo Measure は、これらのアプリケーションに依存して、データをトラッキング、整理および保管し、レポート機能を提供します。Marketo Measureのフレームワークを構成する 4 つのコンポーネントは、次のとおりです。

* Marketo Measure JavaScript の使用
* CRM 統合
* サードパーティのアプリケーション/システム
* Marketo Measure アプリケーション

## Marketo Measure JavaScript {#marketo-measure-javascript}

Marketo Measure JavaScript は、見込み客／リードがお客様の組織に対して行うすべてのオンラインマーケティングインタラクション（タッチポイントとも呼ばれる）をトラッキングします。web サイトの各ページの終了 `</head>` タグの前に追加されるカスタムスクリプトです。

`<script type="text/javascript" src="//[cdn.bizible.com/scripts/bizible.js](http://cdn.bizible.com/scripts/bizible.js)" async=""></script>`

>[!NOTE]
>
>Marketo Measure JS の追加方法については、 [ここをクリック](/help/marketo-measure-tracking/setting-up-tracking/adding-marketo-measure-script.md).

Marketo Measureの JS は、Web 訪問（匿名の Web 訪問を含む）、一般的なトラフィック/ページナビゲーション、コンテンツのダウンロード、フォーム送信からデータを取り込みます。 このデータは、お使いの CRM にプッシュされ、各マーケティングインタラクションがタッチポイントとして表示されます。

## CRM 統合 {#crm-integrations}

Marketo Measure は、CRM と統合され、Marketo Measure JS によって取得されたすべてのデータを保管および整理します。現在、Marketo Measure は、2 つの CRM と API 統合されています。

![](assets/1-2.png)

CRM でMarketo Measureのデータを表示することで、各タッチポイントに関する詳細な情報を確認し、レポートを生成して、チャネルのパフォーマンスを把握できます。

## サードパーティアプリケーション {#third-party-applications}

ほとんどのマーケターは、マーケティング活動を実行するために、いくつかの異なるアプリケーションに依存しています。Salesforce や MS Dynamics に加えて、Marketo Measure は、13 種類のサードパーティアプリケーション（以下を参照）と統合されています。

![](assets/2-1.png)

上記のアプリケーションを使用して任意のマーケティング活動を実行している場合、それらのアカウントを Marketo Measure アカウントにリンクできます。これにより、データを簡単にトラッキングして、Marketo Measure アカウントに転送できます。

## Marketo Measure アプリケーション {#marketo-measure-application}

Marketo Measure アプリケーションは、アトリビューションデータの表示およびレポート、アカウントの設定およびアカウント情報の更新に使用されます。以下に、Marketo Measure アプリのメインメニュー項目を示します。

**アカウント構成**

ここで、会社の一般情報を更新し、Marketo Measure JavaScript にアクセスできます。

**設定**

このメニュー項目を使用すると、アトリビューションとチャネルマッピングの設定、CRM およびサードパーティアプリケーションとの統合の管理、Marketo Measureアカウントユーザーの表示/追加、請求情報の更新をおこなうことができます。

**Marketing ROI ダッシュボード**

マーケティング ROI ダッシュボードのメニュー項目を使用すると、チャネルのパフォーマンス、アクティビティ、コストの観点からデータを視覚化できます。
