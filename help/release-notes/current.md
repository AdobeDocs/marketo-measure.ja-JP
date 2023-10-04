---
description: 最新のリリースノート - [!DNL Marketo Measure] - 製品ドキュメント
title: 最新のリリースノート
exl-id: e93ff03e-ea21-41f4-abb8-32313ee74c0c
feature: Release Notes
source-git-commit: dc4fda07004398207fb5067eb42ecd9e8ffe8624
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 47%

---

# リリースノート：2023年 {#release-notes-2023}

2023年リリースのすべての新機能と更新された機能を以下に示します。

## 第 4 四半期リリース {#q4-release}

<p>

**Discover ダッシュボードの再設計**

すべてのMarketo Measureユーザーは、より優れた操作性と付加価値を組み合わせた、再設計されたアプリ内ダッシュボードを体験できます。 また、B2B の市場投入と購入の間の一般的な遅れを考慮に入れた「実現した ROI」などの新しい指標を導入しています。

新しい事前設計済みダッシュボードのセットは、10 月の第 1 週から 10 月末までに段階的に導入される予定です。 これらの新しいダッシュボードは、製品内情報やドキュメントへのリンクと共に、インスタンスに自動的に表示されます。

* [新しい Discover ダッシュボードガイド](/help/marketo-measure-discover-ui/dashboards/new-discover-dashboard-guide.md){target="_blank"}
* [Discover ダッシュボードの基本](/help/marketo-measure-discover-ui/dashboards/discover-dashboard-basics.md){target="_blank"}
* [収益の概要ダッシュボード](/help/marketo-measure-discover-ui/dashboards/revenue-overview-dashboard.md){target="_blank"}
* [起因する収益ダッシュボード](/help/marketo-measure-discover-ui/dashboards/attributed-revenue-dashboard.md){target="_blank"}
* [ROI ダッシュボード](/help/marketo-measure-discover-ui/dashboards/roi-dashboard.md){target="_blank"}
* [パスポートダッシュボード](/help/marketo-measure-discover-ui/dashboards/passport-dashboard.md){target="_blank"}

>[!NOTE]
>
>現在のダッシュボードは 2024 年 1 月中旬に廃止されますが、それまでの両方のバージョンを利用して、スムーズな移行を実現できます。

### 廃止予定機能 {#deprecations}

<p>

* **&quot;custom_properties&quot;フィールド**

Data Warehouse では、「custom_properties」フィールドは、固定スキーマでカバーされない追加のデータポイントのストレージとして機能していました。 JSON 形式で格納される場合、このフィールドの使用は制限され、SQL クエリとの統合は複雑になり、パフォーマンスに影響を与える可能性があります。 これらの要因から、このフィールドは廃止することにしました。 この変更は、主に Azure テーブルストレージ内のデータ処理レイヤーと、Data Warehouse にエクスポートされたデータに影響を与えます。

* **Dynamics パッケージ関連**

   * Dynamics との連携を維持するには、最新のパッケージバージョン v6.12 をインストールしてください。古いバージョン `(<v6.12)` はサポートされなくなります。 この更新により、履歴レコードの作成が最適化され、ストレージの使用量が削減されます。

   * RefreshToken を持つ古い OAuth メソッドは非推奨（廃止予定）となります。 詳しくは、 [このガイド](/help/marketo-measure-and-dynamics/getting-started-with-marketo-measure-and-dynamics/oauth-with-azure-active-directory-for-dynamics-crm.md){target="_blank"} 資格情報を更新してMicrosoftのベストプラクティスに従うための ClientSecret の使用。

### 次回の予定？ {#q4-whats-coming}

<p>

**アプリ内カスタムレポート**

Marketo Measureを初めてご利用のお客様は、アプリ内で独自のレポートを作成し、保存できます。 これは、2024 年初頭の事前ビルドダッシュボードのリリースに従います。

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
