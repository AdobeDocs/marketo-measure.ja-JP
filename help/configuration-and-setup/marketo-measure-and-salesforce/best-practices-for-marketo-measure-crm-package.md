---
description: のベストプラクティス [!DNL Marketo Measure] CRM パッケージ — [!DNL Marketo Measure]
title: ' [!DNL Marketo Measure] CRM パッケージのベストプラクティス'
exl-id: 97ce0ff3-8aa5-4789-9ee0-25d68c001def
feature: Salesforce
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 3%

---

# のベストプラクティス [!DNL Marketo Measure] CRM パッケージ {#best-practices-for-marketo-measure-crm-package}

>[!NOTE]
>
>この場合、[!DNL Marketo Measure]」 （ドキュメント内）が表示されますが、CRM には「Bizible」が表示されます。 これが更新され、ブランディングの変更がまもなく CRM に反映されます。

## 概要 {#overview}

[!DNL Marketo Measure] 両方とも統合される [!DNL Salesforce] および [!DNL Microsoft Dynamics]を参照する場合、このドキュメントでは、 [!DNL Marketo Measure] 向けに設計された CRM パッケージのベストプラクティス [!DNL Salesforce].

実装時に、次の 2 つのパッケージが [!DNL Salesforce] インスタンス。

基本パッケージ：カスタムオブジェクトとフィールドを含む基本パッケージです。 実稼動環境にすべてのユーザー向けにインストールすることをお勧めします。
ダッシュボード拡張機能パッケージ：これは、3 つの事前ビルドダッシュボードを含む、アドビのダッシュボード拡張機能パッケージです。 実稼動環境内で、すべてのユーザーにインストールすることをお勧めします。 これはオプションですが、のお客様にはをインストールすることをお勧めします。

これらのパッケージにより、 [!DNL Marketo Measure] ユーザーは、 [!DNL Salesforce] インスタンス。 これらのパッケージが正しく設定されていることを確認することは、ページのレイアウト、権限セット、レポート、ダッシュボードが [!DNL Marketo Measure] ユーザーが期待どおりに操作を実行したとします。

## ベストプラクティス {#best-practice}

の実装と管理の際 [!DNL Marketo Measure] [!DNL Salesforce] パッケージでは、次のベストプラクティスに留意してください。

* 必要なチームメンバー全員が [!DNL Marketo Measure] レポートフォルダー。 1-3 が必要です [!DNL Marketo Measure] フォルダー（以下で説明します）。 アクセス権を開くには、パッケージをインストールしたユーザーがレポートフォルダーを適切なユーザーまたは役割と共有する必要があります。
   * **購入者タッチポイントレポート**  — 誰でも利用可能
   * **[!DNL Marketo Measure]アカウントベースドマーケティングレポート**  — レポートは階層 2 以降のお客様にのみ入力されます
   * **購入者タッチポイントダッシュボード**  — 誰でも利用できますが、このパッケージはオプションです。

## メンテナンスのベストプラクティス {#best-practice-for-maintenance}

CRM パッケージの設定は初回実装時に適用されますが、CRM パッケージの設定は年に 1 回確認することをお勧めします。 このレビューでは、すべてのページレイアウトが正しく設定され、適切なチームメンバーが [!DNL Marketo Measure] レポートとダッシュボード。

レビューにトリガーする他の理由…

* 新しいチームメンバーの追加
* の更新 [!DNL Salesforce] ページレイアウト
* の移行 [!DNL Salesforce] 明るくするのにクラシック
* 次に対するアップグレード： [!DNL Marketo Measure] 契約
* に、購入者タッチポイントパッケージの最新バージョンがインストールされていることを確認します。 [!DNL Salesforce]

>[!NOTE]
>
>Salesforce へのMarketo Measureエクスポートデータを無効にした場合、既存のデータは削除されません。 削除するには、 [この Salesforce ヘルプ記事](https://help.salesforce.com/s/articleView?language=en_US&amp;id=sf.c360_a_delete_data_stream_records.htm&amp;type=5){target="_blank"}.

>[!MORELIKETHIS]
>
>* [購入者タッチポイントパッケージの更新](/help/configuration-and-setup/marketo-measure-and-salesforce/marketo-measure-salesforce-package-installation-and-set-up.md)
>* [[!DNL Marketo Measure] 権限セット](/help/configuration-and-setup/marketo-measure-and-salesforce/marketo-measure-permission-sets.md)
>* [レポートとダッシュボードフォルダーの共有](https://help.salesforce.com/s/articleView?language=en_US&amp;id=analytics_share_folder.htm&amp;type=0)
>* [Marketo Measureを Salesforce に接続](/help/configuration-and-setup/marketo-measure-and-salesforce/connect-marketo-measure-to-salesforce.md)
