---
unique-page-id: 18874694
description: Salesforce サンドボックスから実稼動への移行 — [!DNL Marketo Measure]
title: Salesforce サンドボックスの実稼動への移行
exl-id: b2b71c4a-f192-43ce-a27e-cbd0ec3cf008
feature: Salesforce
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 4%

---

# Salesforce サンドボックスの実稼動への移行 {#salesforce-sandbox-to-production-migration}

テストを選択した場合 [!DNL Marketo Measure] 内 [!DNL Salesforce] サンドボックス環境は、準備が整ったら実稼動環境に移行するために、次の手順に従います。 以下の説明は、 [!DNL Marketo Measure] サンドボックス組織にパッケージ化し、必要なテストを実行し、プッシュする準備が整いました。 [!DNL Marketo Measure] を実稼動環境に追加します。

## 手順 1: [!DNL Marketo Measure] 実稼動環境へのパッケージ化 [!DNL Salesforce] インスタンス

* をインストールします。 [!DNL Marketo Measure] を「[!UICONTROL すべてのユーザー]&quot;設定

   * [ベースパッケージ](https://appexchange.salesforce.com/appxListingDetail?listingId=a0N3000000B3KLuEAN){target="_blank"}

* 詳しくは、 [!DNL Marketo Measure] ～との関係 [!DNL Salesforce]、見て [この記事](/help/configuration-and-setup/marketo-measure-and-salesforce/how-marketo-measure-and-salesforce-interact.md)
* 少しの [!DNL Salesforce] 設定が必要です。 具体的なアクション項目については、以下で概要を説明します。 [以下の手順 4](#salesforce-configuration)

## 手順 2：で現在のサンドボックス CRM 接続を削除する [!DNL Marketo Measure] アプリ {#delete-the-current-sandbox-crm-connection-in-marketo-measure-app}

* にログインします。 [!DNL Marketo Measure] experience.adobe.com/marketo-measureのアプリケーション
* マイアカウントに移動します/[!UICONTROL 設定] >[!UICONTROL 接続]
* 削除する SFDC 接続の横にあるごみ箱アイコンをクリックします。
* 削除を確認するメッセージが表示されます。 プロンプトを慎重に読み上げ、削除の結果を理解してください。

  ![](assets/salesforce-sandbox-to-production-migration-1.png)

   * 確認モデルで求められた通りにビジネスの名前を入力し、「結果を理解しています。この接続を削除します」をクリックします。
* このトリガーは、削除プロセスを実行し、完了するまで時間がかかります

## 手順 3：で実稼動 CRM インスタンスを接続する [!DNL Marketo Measure] アプリ {#connect-the-production-crm-instance-in-marketo-measure-app}

* にログインします。 [!DNL Marketo Measure] experience.adobe.com/marketo-measureのアプリケーション
* に移動します。 [!UICONTROL マイアカウント] >[!UICONTROL 設定] > [!UICONTROL 接続]
* サンドボックス接続の削除が正常に完了すると、接続がページに表示されなくなります。そうしないと、接続は「削除中」というステータスで引き続き表示されます。
* 「[!UICONTROL 新しい CRM 接続を設定する]&quot;
* 「[!UICONTROL CRM 接続を選択]&quot;モーダルダイアログで、&quot;[!UICONTROL 接続]```横のアクション [!DNL Salesforce] プラットフォーム、「[!UICONTROL 実稼動]&quot;オプション
* 資格情報の入力を求められます。実稼動用ログインの詳細を必ず入力してください。

## 手順 4: Salesforce 設定 {#salesforce-configuration}

[ページレイアウト](/help/configuration-and-setup/marketo-measure-and-salesforce/page-layout-instructions.md)

[権限セット](/help/configuration-and-setup/marketo-measure-and-salesforce/marketo-measure-permission-sets.md)

[レポートの共有](https://help.salesforce.com/s/articleView?language=en_US&amp;id=analytics_share_folder.htm&amp;type=0){target="_blank"}

[不要なレポートタイプの非表示](/help/configuration-and-setup/marketo-measure-and-salesforce/hiding-unnecessary-report-types.md)

[カスタムワークフロー（該当する場合）](/help/advanced-marketo-measure-features/custom-revenue-amount/using-a-custom-revenue-amount-field.md)
