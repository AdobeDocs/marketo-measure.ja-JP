---
description: 最新のリリースノート - [!DNL Marketo Measure] - 製品ドキュメント
title: 最新のリリースノート
exl-id: 64b8fce8-af7d-4991-b01e-3fcf375d14e7
feature: Release Notes
source-git-commit: 8ac315e7c4110d14811e77ef0586bd663ea1f8ab
workflow-type: ht
source-wordcount: '232'
ht-degree: 100%

---

# リリースノート：2023年 {#release-notes-2023}

2023年リリースのすべての新機能と更新された機能を以下に示します。

## 第 2 四半期リリース {#q2-release}

<p>

**Salesforce パッケージの統合**

* ユーザーエクスペリエンスを向上させ、使用をシンプル化するために、すべての Salesforce パッケージを単一の包括的なパッケージに統合しています。V1、V2_EXT およびレポートパッケージは、次の四半期に廃止される予定です。新しいパッケージは、以前のすべての機能を組み合わせたもので、より効率的な追跡とより深い顧客インサイトを可能にします。
* 既に V2 パッケージをインストールしているお客様は、新しい統合バージョンに更新する必要があります。
* レポート機能を強化するために、次の 2 つの新しいフィールドを追加しました。
   * form_name：BT/BAT オブジェクトで使用できるようになったこのフィールドにより、ユーザーはフォーム名に基づいてレポートを作成できます。
   * user_touchpoint_id：このフィールドを使用すると、ユーザーは固有のユーザータッチポイント数を含むレポートを作成できます。
* [この記事](/help/configuration-and-setup/marketo-measure-and-salesforce/salesforce-package-consolidation.md){target="_blank"}には、レガシーレポートパッケージからレポートとダッシュボードを再作成する方法に関するガイドが含まれています。

**Salesforce API バージョンのアップデート**

* UserActivityContext クラスを含む、Apex クラスのすべての Salesforce API バージョンが、次のサポート対象のバージョンに更新されます。（31.0～57.0）

**新しいパッケージのインストール**

* 新しい統合パッケージのインストールリンクは、[こちらを参照してください](https://login.salesforce.com/packaging/installPackage.apexp?p0=04t1P000000VY6Z){target="_blank"}

### 次回の予定？ {#whats-coming}

<p>

**IP アドレスストレージの変更**

* アドビでは、プライバシーに関する考慮事項に従い、今後はアドビのシステムに IP アドレスを保存しません。IP アドレスの位置情報の識別と保存は引き続き行いますが、形式は変更される予定です（例：「米国」から「US」）。
