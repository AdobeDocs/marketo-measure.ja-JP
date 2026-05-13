---
unique-page-id: 18874698
description: ' [!DNL Marketo Measure]  プロファイルの作成 –  [!DNL Marketo Measure]'
title: ' [!DNL Marketo Measure] プロファイルの作成'
exl-id: dab2e2cb-fbd3-464a-9bd7-e9bf153d9848
feature: Salesforce
TQID: https://experienceleague.adobe.com/7LvGF-KnE-FAkp1eLwawZUbFqac4cWAH9YmPKXaqKsM
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
feature_v2:
  - id: c8f57308-7e33-4e41-a385-b55041c78939
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 7%

---

# [!DNL Marketo Measure] プロファイルの作成 {#creating-a-marketo-measure-profile}

[!DNL Marketo Measure] プロファイルの作成方法を説明します。 [!DNL Marketo Measure] プロファイルを作成すると、CRMにデータをプッシュする際に検証エラーが発生しないようにします。

1. 特定の[!DNL Marketo Measure] プロファイルを作成：

   * [!DNL Marketo Measure]管理者権限セットの割り当て
   * コンバージョン済みリードを表示および編集する権限を有効にする

   >[!NOTE]
   >
   >このプロファイルは、[!DNL System Admin] プロファイルのクローンにすることができます

1. 専用の[!DNL Marketo Measure] ユーザーを作成しました：

   * 新しい[!DNL Marketo Measure] プロファイルをそのユーザーに割り当てます
   * ユーザーレベルの権限として「マーケティングユーザー」を有効にする

1. このプロファイルをすべてのトリガー、ワークフロー、プロセスから除外します。
1. [!DNL Marketo Measure] アカウントにログインし、新しいユーザーで[!DNL Salesforce]接続を再認証します。

   * [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"}に移動し、新しいユーザー実稼動Salesforce資格情報でログインします
   * 「[!UICONTROL &#x200B; マイアカウント &#x200B;]」ドロップダウンで「[!UICONTROL 設定]」を選択します
   * 「[!UICONTROL 統合]」グループ内の「[!UICONTROL 接続]」を選択します
   * 現在の接続されている[!DNL Salesforce]接続の右側にあるキーアイコンをクリックし、「実稼動環境で再認証」を選択します。 次に、プロンプトが表示されたら、新しいユーザー資格情報で再度ログインします

   完了!

   専用の[!DNL Marketo Measure] プロファイルの作成について質問がある場合は、Adobe アカウントチーム（アカウントマネージャー）または[Marketo サポート &#x200B;](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"}にお問い合わせください。
