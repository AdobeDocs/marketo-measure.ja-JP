---
description: 最新のリリースノート - [!DNL Marketo Measure] - 製品ドキュメント
title: 最新のリリースノート
exl-id: e93ff03e-ea21-41f4-abb8-32313ee74c0c
feature: Release Notes
source-git-commit: 40cd00c8edeb04c1939db9402d537d4c0e7a3406
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 61%

---

# リリースノート：2023年 {#release-notes-2023}

2023年リリースのすべての新機能と更新された機能を以下に示します。

## 第 4 四半期リリース {#q4-release}

<p>

**ウェブトラフィックダッシュボード**

新しく再設計された [ウェブトラフィックダッシュボード](/help/marketo-measure-discover-ui/dashboards/web-traffic-dashboard.md){target="_blank"} は、すべての顧客がアクセスできるようになりました。 このダッシュボードは、Web サイトの訪問者のインタラクションの完全な概要を提供します。 特定のフォーム URL やランディングページから、URL ごとの個別訪問者数、全体的な訪問回数、ページビュー数、フォーム送信回数などの指標を分析できます。 また、月別のトラフィック傾向を追跡し、パフォーマンスの高い有料メディアを特定することもできます。これは、最適な売上高生成のために戦略を絞り込むのに役立ちます。

事前設計された新しいダッシュボードのセットは、今年末までに段階的に導入される予定です。

>[!NOTE]
>
>現在のダッシュボードは 2024年1月中旬に廃止されますが、それまでは両方のバージョンを利用して、スムーズな移行を実現できます。

**IP アドレスのデータの削除**

データのプライバシーコンプライアンスを確保するため、長期ストレージから IP アドレスデータを削除しています。 現在、次のSnowflakeテーブルおよびビューには IP アドレスが含まれています。このデータを削除し、新しい位置情報を追加する予定です。

<table style="width:400px">
<thead>
  <tr>
    <th style="width:50%">テーブル</th>
    <th>ビュー</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>CUSTOMER_AB_TESTS</td>
    <td>BIZ_CUSTOMER_AB_TESTS</td>
  </tr>
  <tr>
    <td>CUSTOMER_EVENTS</td>
    <td>BIZ_CUSTOMER_EVENTS</td>
  </tr>
  <tr>
    <td>FORM_SUBMITS</td>
    <td>BIZ_FORM_SUBMITS</td>
  </tr>
  <tr>
    <td>IMPRESSIONS</td>
    <td>BIZ_IMPRESSIONS</td>
  </tr>
  <tr>
    <td>PAGE_VIEWS</td>
    <td>BIZ_PAGE_VIEWS</td>
  </tr>
  <tr>
    <td>SESSIONS</td>
    <td>BIZ_SESSIONS</td>
  </tr>
  <tr>
    <td>WEB_HOST_MAPPINGS</td>
    <td>BIZ_WEB_HOST_MAPPINGS</td>
  </tr>
</tbody>
</table>

* 今後は、国名、市区町村名、地域名の代わりに、国コード、市区町村名、地域コードをダウンロードします。
* すべての履歴 Web アクティビティを処理する際に、レコード間で場所情報に不整合が生じる場合があります。 これらの不整合には、位置情報の詳細がない IP アドレスの存在、IP アドレスがない更新された位置情報、国名や地域名とコードの組み合わせなどが含まれます。
* _**この混在データの期間は、01/04/2023 ～ 02/29/2023の間に発生すると想定されます。**_

**URL 表のページタイトルデータ**

URL テーブル ( [データウェアハウス](/help/marketo-measure-data-warehouse/data-warehouse-schema.md){target="_blank"} Web データテーブルに加えて、ページタイトルフィールドが含まれるようになりました。

URL テーブル内のページタイトルが、他の Web テーブル内のページタイトルと一致しない場合があることに注意してください。 URL テーブルには、最新のページタイトルが表示されます。 Web アクティビティの発生後に URL のタイトルが変更された場合、URL テーブルのタイトルと一致しません。

**Discover ダッシュボードの刷新**

すべての Marketo Measure ユーザは、より優れた操作性と付加価値を組み合わせ、刷新されたアプリ内ダッシュボードを体験できます。また、B2G GTM 戦略においてマーケティング投資と購入の間に発生する一般的な遅れを考慮に入れた「実質 ROI」などの新しい指標を導入しています。

新しい事前定義済みダッシュボードのセットは、10月の第 1 週から年末までに段階的に導入される予定です。これらの新しいダッシュボードは、製品内情報やドキュメントへのリンクと共に、インスタンスに自動的に表示されます。

* [新しい Discover ダッシュボードガイド](/help/marketo-measure-discover-ui/dashboards/new-discover-dashboard-guide.md){target="_blank"}
* [Discover ダッシュボードの基本](/help/marketo-measure-discover-ui/dashboards/discover-dashboard-basics.md){target="_blank"}
* [収益の概要ダッシュボード](/help/marketo-measure-discover-ui/dashboards/revenue-overview-dashboard.md){target="_blank"}
* [起因する収益ダッシュボード](/help/marketo-measure-discover-ui/dashboards/attributed-revenue-dashboard.md){target="_blank"}
* [ROI ダッシュボード](/help/marketo-measure-discover-ui/dashboards/roi-dashboard.md){target="_blank"}
* [パスポートダッシュボード](/help/marketo-measure-discover-ui/dashboards/passport-dashboard.md){target="_blank"}

>[!NOTE]
>
>現在のダッシュボードは 2024年1月中旬に廃止されますが、それまでは両方のバージョンを利用して、スムーズな移行を実現できます。

### 廃止予定機能 {#deprecations}

<p>

* **Salesforce フィールドの廃止**

統合を簡略化し、Salesforce 標準オブジェクトにエクスポートする必要をなくすために、リード/連絡先オブジェクトへのエクスポートジョブを段階的に廃止する予定です。 お客様はタッチポイントオブジェクトから同じデータを取得できるので、以下に示す非正規化されたフィールドも非推奨（廃止予定）となります。 _**廃止予定は 2024 年 6 月です。**_

<table style="width:300px">
<tbody>
  <tr>
    <td>bizible2__Ad_Campaign_Name_FT__c</td>
  </tr>
  <tr>
    <td>bizible2__Ad_Campaign_Name_LC__c</td>
  </tr>
  <tr>
    <td>bizible2__Landing_Page_FT__c</td>
  </tr>
  <tr>
    <td>bizible2__Landing_Page_LC__c</td>
  </tr>
  <tr>
    <td>bizible2__Touchpoint_Date_FT__c</td>
  </tr>
  <tr>
    <td>bizible2__Touchpoint_Date_LC__c</td>
  </tr>
  <tr>
    <td>bizible2__Touchpoint_Source_FT__c</td>
  </tr>
  <tr>
    <td>bizible2__Touchpoint_Source_LC__c</td>
  </tr>
  <tr>
    <td>bizible2__Marketing_Channel_FT__c</td>
  </tr>
  <tr>
    <td>bizible2__Marketing_Channel_LC__c</td>
  </tr>
</tbody>
</table>

* **Dynamics パッケージ関連**

   * Dynamics との接続を維持するには、最新のパッケージバージョン v6.12 をインストールしてください。古いバージョン `(<v6.12)` はサポートされなくなります。この更新により、履歴レコードの作成が最適化され、ストレージの使用量が削減されます。

   * RefreshToken を使用した古い OAuth メソッドは非推奨（廃止予定）となります。ClientSecret の使用に関する Microsoft のベストプラクティスに従った資格情報の更新について詳しくは、[このガイド](/help/marketo-measure-and-dynamics/getting-started-with-marketo-measure-and-dynamics/oauth-with-azure-active-directory-for-dynamics-crm.md){target="_blank"}を参照してください。

* **「custom_properties」フィールド**

データウェアハウスでは、「custom_properties」フィールドは、固定スキーマでカバーされない追加のデータポイントのストレージとして機能していました。JSON 形式で格納される場合、このフィールドの使用は制限され、SQL クエリとの統合は複雑になり、パフォーマンスに影響を与える可能性があります。これらの要因から、このフィールドは廃止することにしました。この変更は、主に Azure テーブルストレージ内のデータ処理レイヤーおよびデータウェアハウスに書き出されたデータに影響を与えます。

### 今後の予定 {#q4-whats-coming}

<p>

**アプリ内カスタムレポート**

Marketo Measure を初めてご利用のお客様は、アプリ内で独自のレポートを作成し、保存できます。続いて 2024年初頭に事前定義済みダッシュボードのリリースが予定されています。

<br>

## 第 2 四半期リリース {#q2-release}

<p>

* **Salesforce パッケージの統合**

ユーザーエクスペリエンスを向上させ、使用をシンプル化するために、すべての Salesforce パッケージを単一の包括的なパッケージに統合しています。V1、V2_EXT およびレポートパッケージは、次の四半期に廃止される予定です。新しいパッケージは、以前のすべての機能を組み合わせたもので、より効率的な追跡とより深い顧客インサイトを可能にします。

既に V2 パッケージをインストールしているお客様は、新しい統合バージョンに更新する必要があります。

レポート機能を強化するために、次の 2 つの新しいフィールドを追加しました。

* form_name：BT/BAT オブジェクトで使用できるようになったこのフィールドにより、ユーザーはフォーム名に基づいてレポートを作成できます。
* user_touchpoint_id：このフィールドを使用すると、ユーザーは固有のユーザータッチポイント数を含むレポートを作成できます。

[この記事](/help/configuration-and-setup/marketo-measure-and-salesforce/salesforce-package-consolidation.md){target="_blank"}には、レガシーレポートパッケージからレポートとダッシュボードを再作成する方法に関するガイドが含まれています。

* **Salesforce API バージョンのアップデート**

UserActivityContext クラスを含む、Apex クラスのすべての Salesforce API バージョンが、次のサポート対象のバージョンに更新されます。（31.0～57.0）

* **新しいパッケージのインストール**

新しい統合パッケージのインストールリンクは、[こちらを参照してください](https://login.salesforce.com/packaging/installPackage.apexp?p0=04t1P000000VY6Z){target="_blank"}

### 次回の予定？ {#q2-whats-coming}

<p>

**IP アドレスストレージの変更**

アドビでは、プライバシーに関する考慮事項に従い、今後はアドビのシステムに IP アドレスを保存しません。IP アドレスの位置情報の識別と保存は引き続き行いますが、形式は変更される予定です（例：「米国」から「US」）。
