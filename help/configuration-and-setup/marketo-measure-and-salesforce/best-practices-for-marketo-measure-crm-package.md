---
description: のベストプラクティス [!DNL Marketo Measure] CRM パッケージ — [!DNL Marketo Measure]  — 製品ドキュメント
title: のベストプラクティス [!DNL Marketo Measure] CRM パッケージ
exl-id: 97ce0ff3-8aa5-4789-9ee0-25d68c001def
source-git-commit: 00268f49ff6e5dfc105fa7ea21837375eae49647
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# のベストプラクティス [!DNL Marketo Measure] CRM パッケージ {#best-practices-for-marketo-measure-crm-package}

>[!NOTE]
>
>&quot;[!DNL Marketo Measure]」 （アドビのドキュメント内）。ただし、CRM には「Bizible」が表示されます。 アドビは現在、その更新をおこなっており、ブランディングの変更が CRM に反映される予定です。

## 概要 {#overview}

[!DNL Marketo Measure] 両方とも統合 [!DNL Salesforce] および [!DNL Microsoft Dynamics]このドキュメントでは、 [!DNL Marketo Measure] 用に設計された CRM パッケージのベストプラクティス [!DNL Salesforce].

実装時に、次の 2 つのパッケージが [!DNL Salesforce] インスタンス。

ベースパッケージ：これは、カスタムオブジェクトとフィールドを含む基本パッケージです。 実稼動環境内で、すべてのユーザーにインストールすることをお勧めします。
ダッシュボード拡張機能パッケージ：これは、3 つの事前ビルドダッシュボードを含む、アドビのダッシュボード拡張機能パッケージです。 実稼動環境内で、すべてのユーザーにインストールすることをお勧めします。 これはオプションですが、のお客様にはをインストールすることをお勧めします。

これらのパッケージにより、 [!DNL Marketo Measure] ユーザーは、 [!DNL Salesforce] インスタンス。 これらのパッケージが正しく設定されていることを確認することは、ページのレイアウト、権限セット、レポート、ダッシュボードが [!DNL Marketo Measure] ユーザーが期待どおりに操作を実行したとします。

## ベストプラクティス {#best-practice}

の実装と管理に関しては、 [!DNL Marketo Measure] [!DNL Salesforce] パッケージでは、次のベストプラクティスに留意してください。

* 必要なチームメンバーがすべて、 [!DNL Marketo Measure] レポートフォルダー。 1-3 が必要です [!DNL Marketo Measure] フォルダー（以下で説明します）。 アクセス権を開くには、パッケージをインストールしたユーザーが、適切なユーザーまたは役割とレポートフォルダーを共有する必要があります。
   * **購入者タッチポイントレポート**  — 誰でも利用可能
   * **[!DNL Marketo Measure]アカウントベースドマーケティングレポート**  — レポートは階層 2 以降のお客様にのみ入力されます
   * **購入者タッチポイントダッシュボード**  — 誰でも利用できますが、このパッケージはオプションです。

## メンテナンスのベストプラクティス {#best-practice-for-maintenance}

CRM パッケージの設定は初回実装時に適用されますが、CRM パッケージの設定は年に 1 回確認することをお勧めします。 このレビューでは、すべてのページレイアウトが正しく設定され、適切なチームメンバーが [!DNL Marketo Measure] レポートとダッシュボード。

レビューにトリガーする他の理由

* 新しいチームメンバーの追加
* 更新内容 [!DNL Salesforce] ページレイアウト
* の移行 [!DNL Salesforce] 明るくするのにクラシック
* 次に対するアップグレード： [!DNL Marketo Measure] 契約
* アドビの購入者タッチポイントパッケージの最新バージョンがにインストールされていることを確認します。 [!DNL Salesforce]

>[!NOTE]
>
>Salesforce へのMarketo Measureエクスポートデータを無効にしても、既存のデータは削除されません。 削除するには、 [この Salesforce ヘルプ記事](https://help.salesforce.com/s/articleView?id=sf.c360_a_delete_data_stream_records.htm&amp;type=5){target="_blank"}.

>[!MORELIKETHIS]
>
>* [購入者タッチポイントパッケージの更新](/help/configuration-and-setup/marketo-measure-and-salesforce/marketo-measure-salesforce-package-installation-and-set-up.md)
>* [[!DNL Marketo Measure] 権限セット](/help/configuration-and-setup/marketo-measure-and-salesforce/marketo-measure-permission-sets.md)
>* [レポートとダッシュボードフォルダーの共有](https://help.salesforce.com/articleView?id=analytics_share_folder.htm&amp;type=0)
>* [Marketo Measureを Salesforce に接続](/help/configuration-and-setup/marketo-measure-and-salesforce/connect-marketo-measure-to-salesforce.md)

