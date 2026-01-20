---
unique-page-id: 18874694
description: Salesforce サンドボックスから実稼動への移行 -  [!DNL Marketo Measure]
title: Salesforce サンドボックスから実稼動への移行
exl-id: b2b71c4a-f192-43ce-a27e-cbd0ec3cf008
feature: Salesforce
source-git-commit: 666812e8bf095170d611cd694b5d0ac5151d8fdd
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 98%

---

# Salesforce サンドボックスから実稼動への移行 {#salesforce-sandbox-to-production-migration}

[!DNL Salesforce] サンドボックス環境で [!DNL Marketo Measure] をテストすることを選択した場合は、準備が整ったら次の手順に従って実稼動環境に移行します。次の手順は、[!DNL Marketo Measure] パッケージを Sandbox 組織にダウンロードし、必要なテストを実行し、[!DNL Marketo Measure] を実稼動環境にプッシュする準備が整っていることを前提としています。

## 手順 1：[!DNL Marketo Measure] パッケージの実稼動 [!DNL Salesforce] インスタンスへのインストール

* 「[!UICONTROL すべてのユーザ]」設定で [!DNL Marketo Measure] パッケージを実稼動環境にインストールします

   * [ 基本パッケージ ](https://appexchange.salesforce.com/appxListingDetail?listingId=a0N3000000B3KLuEAN){target="_blank"}

* [!DNL Marketo Measure] と [!DNL Salesforce] の関係について詳しくは、[この記事](/help/configuration-and-setup/marketo-measure-and-salesforce/how-marketo-measure-and-salesforce-interact.md)を参照してください
* [!DNL Salesforce] の設定が少し必要です。具体的なアクション項目については、[以下の手順 4](#salesforce-configuration) を参照してください

## 手順 2：[!DNL Marketo Measure] アプリでの現在のサンドボックス CRM 接続の削除 {#delete-the-current-sandbox-crm-connection-in-marketo-measure-app}

* experience.adobe.com/marketo-measure で [!DNL Marketo Measure] アプリケーションにログインします
* マイアカウント／[!UICONTROL 設定]／[!UICONTROL 接続]に移動します
* SFDC 接続の横にあるごみ箱アイコンをクリックして削除します
* 削除を確認するプロンプトが表示されます。プロンプトを注意深く読んで、削除の結果を理解します

  ![](assets/salesforce-sandbox-to-production-migration-1.png)

   * 確認モデルのプロンプトに従ってビジネスの名前を入力し、「結果を理解しました。この接続を削除します」をクリックします
* これにより、削除プロセスがトリガーされ、完了するまでに時間がかかります

## 手順 3：[!DNL Marketo Measure] アプリでの実稼動 CRM インスタンスの接続 {#connect-the-production-crm-instance-in-marketo-measure-app}

* experience.adobe.com/marketo-measure で [!DNL Marketo Measure] アプリケーションにログインします
* [!UICONTROL マイアカウント]／[!UICONTROL 設定]／[!UICONTROL 接続]に移動します
* サンドボックス接続の削除が正常に完了すると、接続はページに表示されなくなります。そうでない場合、接続は「削除中」のステータスで引き続き表示されます
* 「[!UICONTROL 新しい CRM 接続を設定]」をクリックします
* 「[!UICONTROL CRM 接続を選択]」モーダルダイアログで、[!DNL Salesforce] プラットフォームの横にある「[!UICONTROL 接続]」アクションをクリックし、「[!UICONTROL 実稼動]」オプションを選択します
* 認証情報の入力を求めるプロンプトが表示されます。実稼動環境のログイン詳細を入力します。

## 手順 4：Salesforce の設定 {#salesforce-configuration}

[ページレイアウト](/help/configuration-and-setup/marketo-measure-and-salesforce/page-layout-instructions.md)

[権限セット](/help/configuration-and-setup/marketo-measure-and-salesforce/marketo-measure-permission-sets.md)

[ レポートの共有 ](https://help.salesforce.com/s/articleView?language=en_US&id=analytics_share_folder.htm&type=0){target="_blank"}

[不要なレポートタイプの非表示](/help/configuration-and-setup/marketo-measure-and-salesforce/hiding-unnecessary-report-types.md)

[カスタムワークフロー（該当する場合）](/help/advanced-marketo-measure-features/custom-revenue-amount/using-a-custom-revenue-amount-field.md)
