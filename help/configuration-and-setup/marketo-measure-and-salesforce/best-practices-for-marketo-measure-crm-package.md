---
description: ' [!DNL Marketo Measure] CRM パッケージのベストプラクティス - [!DNL Marketo Measure]'
title: ' [!DNL Marketo Measure] CRM パッケージのベストプラクティス'
exl-id: 97ce0ff3-8aa5-4789-9ee0-25d68c001def
feature: Salesforce
source-git-commit: 666812e8bf095170d611cd694b5d0ac5151d8fdd
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 7%

---

# CRM パッケージ [!DNL Marketo Measure] ベストプラクティス {#best-practices-for-marketo-measure-crm-package}

>[!NOTE]
>
>ドキュメント内に「[!DNL Marketo Measure]」を指定する手順が記載されている場合がありますが、CRM には引き続き「Bizible」と表示されます。この情報は更新され、ブランド変更はすぐに CRM に反映されます。

## 概要 {#overview}

[!DNL Marketo Measure] は [!DNL Salesforce] と [!DNL Microsoft Dynamics] の両方と統合されているため、このドキュメントでは、[!DNL Marketo Measure] 用に設計された CRM パッケージの [!DNL Salesforce] のベストプラクティスに焦点を当てています。

実装時に、[!DNL Salesforce] インスタンスに次の 2 つのパッケージがインストールされていました。

ベースパッケージ：カスタムオブジェクトとフィールドを含むベースパッケージです。 すべてのユーザーに対して、を実稼動環境にインストールすることをお勧めします。
ダッシュボード拡張機能パッケージ：これはアドビのダッシュボード拡張機能パッケージで、3 つの事前定義済みダッシュボードが含まれています。 すべてのユーザーに対して、実稼動環境にをインストールすることをお勧めします。 これはオプションですが、のインストールをお勧めします。

これらのパッケージを使用すると、[!DNL Marketo Measure] ユーザーは [!DNL Salesforce] インスタンス全体のタッチポイントデータに簡単にアクセスできます。 これらのパッケージが正しく設定されていることを確認することは、ページレイアウト、権限セット、レポートおよびダッシュボードが [!DNL Marketo Measure] ユーザーに期待どおりに表示されていることを確認するうえで重要です。

## ベストプラクティス {#best-practice}

[!DNL Marketo Measure] [!DNL Salesforce] パッケージを実装および管理する際は、次のベストプラクティスに留意してください。

* 必要なチームメンバー全員が、[!DNL Marketo Measure] のレポートフォルダーにアクセスできることを確認します。 1～3 個の [!DNL Marketo Measure] フォルダーが必要です（これらは以下で説明します）。 アクセスを開くには、パッケージをインストールしたユーザーが、適切なユーザーや役割とレポートフォルダーを共有する必要があります。
   * **Buyer Touchpoint レポート** – すべてのユーザーが利用できます
   * **[!DNL Marketo Measure]アカウントベースのマーケティングレポート** - レポートは、階層 2 以上の顧客にのみ入力されます
   * **Buyer Touchpoint ダッシュボード** – すべてのユーザーが利用できますが、このパッケージはオプションです。

## メンテナンスのベストプラクティス {#best-practice-for-maintenance}

CRM パッケージの設定は最初の実装時にカバーされますが、CRM パッケージの設定は年に 1 回レビューすることをお勧めします。 このレビューでは、すべてのページレイアウトが正しく設定され、適切なチームメンバー全員がレポートとダッシュボードにアクセスでき [!DNL Marketo Measure] ことを確認します。

レビューをトリガーとするその他の理由…

* 新しいチームメンバーの追加
* [!DNL Salesforce] ページレイアウトの更新
* [!DNL Salesforce] Classic から Lightning への移行
* [!DNL Marketo Measure] 契約のアップグレード
* 最新バージョンのバイヤータッチポイントパッケージが [!DNL Salesforce] にインストールされていることを確認します

>[!NOTE]
>
>Salesforceへのデータの書き出しを無効にしても、既存のMarketo Measureは削除されません。 削除するには、[&#x200B; このSalesforce ヘルプ記事 &#x200B;](https://help.salesforce.com/s/articleView?language=en_US&id=sf.c360_a_delete_data_stream_records.htm&type=5){target="_blank"} の手順に従います。

>[!MORELIKETHIS]
>
>* [Buyer Touchpoint パッケージの更新 &#x200B;](/help/configuration-and-setup/marketo-measure-and-salesforce/marketo-measure-salesforce-package-installation-and-set-up.md)
>* [[!DNL Marketo Measure]  アクセス権セット &#x200B;](/help/configuration-and-setup/marketo-measure-and-salesforce/marketo-measure-permission-sets.md)
>* [&#x200B; レポートとダッシュボードのフォルダーの共有 &#x200B;](https://help.salesforce.com/s/articleView?language=en_US&id=analytics_share_folder.htm&type=0)
>* [Marketo MeasureをSalesforceに接続 &#x200B;](/help/configuration-and-setup/marketo-measure-and-salesforce/connect-marketo-measure-to-salesforce.md)
