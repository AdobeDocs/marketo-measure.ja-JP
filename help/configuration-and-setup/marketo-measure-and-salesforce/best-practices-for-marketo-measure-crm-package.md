---
description: ' [!DNL Marketo Measure] CRM パッケージ - [!DNL Marketo Measure]のベストプラクティス'
title: ' [!DNL Marketo Measure] CRM パッケージのベストプラクティス'
exl-id: 97ce0ff3-8aa5-4789-9ee0-25d68c001def
feature: Salesforce
TQID: https://experienceleague.adobe.com/E8LQ0-uUC-xqhG9D7CSuprsjkABJ54azWFSEdiuFABk
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 415
ht-degree: 8%

---

# [!DNL Marketo Measure] CRM パッケージのベストプラクティス {#best-practices-for-marketo-measure-crm-package}

>[!NOTE]
>
>ドキュメント内に「[!DNL Marketo Measure]」を指定する手順が記載されている場合がありますが、CRM には引き続き「Bizible」と表示されます。 リブランディングはすぐにCRMに反映されます。

## 概要 {#overview}

[!DNL Marketo Measure]は[!DNL Salesforce]と[!DNL Microsoft Dynamics]の両方と統合されています。このドキュメントでは、[!DNL Salesforce]向けに設計されたCRM パッケージの[!DNL Marketo Measure]のベストプラクティスに焦点を当てています。

実装中に、次の2つのパッケージが[!DNL Salesforce] インスタンスにインストールされました。

基本パッケージ：カスタムオブジェクトとフィールドを含む基本パッケージです。 すべてのユーザーは実稼動環境にインストールすることをお勧めします。
ダッシュボード拡張機能パッケージ：これは、3つの事前定義済みのダッシュボードを含むダッシュボード拡張機能パッケージです。 すべてのユーザーには、実稼動環境にインストールすることをお勧めします。 これはオプションですが、インストールすることをお勧めします。

これらのパッケージにより、[!DNL Marketo Measure] ユーザーは[!DNL Salesforce] インスタンス全体でタッチポイントデータに簡単にアクセスできます。 これらのパッケージが正しく設定されていることを確認することは、ページレイアウト、権限セット、レポート、ダッシュボードが[!DNL Marketo Measure] ユーザーに期待どおりに表示されていることを確認するための重要な鍵となります。

## ベストプラクティス {#best-practice}

[!DNL Marketo Measure] [!DNL Salesforce] パッケージを実装および管理する際は、次のベストプラクティスを念頭に置いてください。

* 必要なすべてのチームメンバーが[!DNL Marketo Measure] レポートフォルダーにアクセスできることを確認します。 1 ～ 3 [!DNL Marketo Measure]個のフォルダーが必要です（これらは以下で説明します）。 アクセスを開くには、パッケージをインストールしたユーザーが、適切なユーザーまたは役割とレポートフォルダーを共有する必要があります。
   * **Buyer Touchpoint レポート** – すべてのユーザーが利用できます
   * **[!DNL Marketo Measure]アカウントベースドマーケティングレポート** - レポートは、階層2以上の顧客にのみ入力されます
   * **Buyer Touchpoint ダッシュボード** – このパッケージはオプションですが、誰でも利用できます。

## メンテナンスのベストプラクティス {#best-practice-for-maintenance}

CRM パッケージのセットアップは初期実装中に行われますが、CRM パッケージのセットアップは年に1回確認することをお勧めします。 このレビューにより、すべてのページレイアウトが正しく設定され、すべての適切なチームメンバーが[!DNL Marketo Measure]件のレポートとダッシュボードにアクセスできることが確認されます。

その他の理由により、レビューがトリガーされる可能性があります。

* 新しいチームメンバーの追加
* [!DNL Salesforce] ページレイアウトの更新
* [!DNL Salesforce] ClassicからLighteningへの移行
* [!DNL Marketo Measure] コントラクトへのアップグレード
* [!DNL Salesforce]に最新バージョンのBuyer Touchpoints パッケージがインストールされていることを確認してください

>[!NOTE]
>
>Marketo MeasureからSalesforceへのデータの書き出しを無効にすると、既存のデータは削除されません。 削除するには、[このSalesforce ヘルプ記事](https://help.salesforce.com/s/articleView?language=en_US&id=sf.c360_a_delete_data_stream_records.htm&type=5){target="_blank"}の手順に従います。

>[!MORELIKETHIS]
>
>* [Buyer Touchpoint パッケージの更新](/help/configuration-and-setup/marketo-measure-and-salesforce/marketo-measure-salesforce-package-installation-and-set-up.md)
>* [[!DNL Marketo Measure] 権限セット &#x200B;](/help/configuration-and-setup/marketo-measure-and-salesforce/marketo-measure-permission-sets.md)
>* [&#x200B; レポートとダッシュボード フォルダーの共有](https://help.salesforce.com/s/articleView?language=en_US&id=analytics_share_folder.htm&type=0)
>* [Marketo MeasureをSalesforceに接続](/help/configuration-and-setup/marketo-measure-and-salesforce/connect-marketo-measure-to-salesforce.md)
