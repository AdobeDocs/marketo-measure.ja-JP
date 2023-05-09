---
description: 最新のリリースノート — [!DNL Marketo Measure]  — 製品ドキュメント
title: 最新のリリースノート
source-git-commit: 8e8ddd80d69102455fa678a32f31a9fe8319822c
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---

# リリースノート：2023 年 {#release-notes-2023}

2023 リリースのすべての新機能と更新された機能を以下に示します。

## 第 2 四半期リリース {#q2-release}

<p>

**Salesforce パッケージ統合**

* すべての Salesforce パッケージを 1 つの包括的なパッケージに統合し、ユーザーエクスペリエンスを向上させ、使用をシンプル化します。 V1、V2_EXT、およびレポート用の各パッケージは、来四半期に廃止されます。 この新しいパッケージは、以前のすべての機能を組み合わせたもので、より効率的な追跡とより深い顧客インサイトを提供します。
* 既に V2 パッケージをインストールしている場合は、そのパッケージを新しい統合バージョンに更新する必要があります。
* レポート機能を強化するための新しいフィールドが 2 つ追加されました。
   * form_name:BT/BAT オブジェクトで使用できるようになりました。このフィールドを使用すると、フォーム名に基づくレポートを作成できます。
   * user_touchpoint_id:このフィールドを使用すると、ユーザーは個別のユーザータッチポイント数でレポートを作成できます。
* [この記事](/help/configuration-and-setup/marketo-measure-and-salesforce/salesforce-package-consolidation.md){target="_blank"} には、レガシーレポートパッケージからレポートとダッシュボードを再作成する方法に関するガイドが含まれています。

**Salesforce API バージョンの更新**

* UserActivityContext クラスを含む Apex クラスの Salesforce API バージョンはすべて、サポート対象のバージョンに更新されます。 (31.0～57.0)

**新しいパッケージのインストール**

* 新しい統合パッケージのインストールリンク [ここにあります](https://login.salesforce.com/packaging/installPackage.apexp?p0=04t1P000000VY6Z){target="_blank"}

### 何が来る？ {#whats-coming}

<p>

**IP アドレスストレージの変更**

* プライバシーに関する考慮事項に従って、アドビのシステムに IP アドレスを保存しなくなります。 IP アドレスの地域情報は引き続き識別および保存されますが、形式は（「米国」など）「米国」に変更されます。
