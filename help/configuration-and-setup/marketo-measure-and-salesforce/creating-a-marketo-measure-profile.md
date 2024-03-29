---
unique-page-id: 18874698
description: の作成 [!DNL Marketo Measure] プロファイル — [!DNL Marketo Measure]
title: ' [!DNL Marketo Measure] プロファイルの作成'
exl-id: dab2e2cb-fbd3-464a-9bd7-e9bf153d9848
feature: Salesforce
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 3%

---

# の作成 [!DNL Marketo Measure] プロファイル {#creating-a-marketo-measure-profile}

を作成する方法を学ぶ [!DNL Marketo Measure] プロファイル。 の作成 [!DNL Marketo Measure] プロファイルを使用すると、データを CRM にプッシュする際に、検証エラーが発生しないようにします。

1. 特定の [!DNL Marketo Measure] プロファイル：

   * 割り当て [!DNL Marketo Measure] 管理者権限セット
   * 変換済みリードの表示と編集の権限を有効にします

   >[!NOTE]
   >
   >このプロファイルは、 [!DNL System Admin] profile

1. 専用のを作成しました [!DNL Marketo Measure] ユーザー：

   * 新しい [!DNL Marketo Measure] そのユーザーに対するプロファイル
   * ユーザーレベルの権限として「マーケティングユーザー」を有効にします

1. すべてのトリガー、ワークフローおよびプロセスからこのプロファイルを除外します。
1. にログインします。 [!DNL Marketo Measure] アカウントと再認証 [!DNL Salesforce] 新しいユーザーとの接続：

   * に移動します。 [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"} 新しいユーザ本番 Salesforce 認証情報を使用してログインします。
   * 「[!UICONTROL 設定]」内の[!UICONTROL マイアカウント]「 」ドロップダウン
   * 「[!UICONTROL 接続]」内の[!UICONTROL 統合]&quot;グループ化&quot;
   * 現在接続されているの右にあるキーアイコンをクリックします。 [!DNL Salesforce] 接続し、「実稼動環境で再認証」を選択します。 その後、要求された場合は、新しいユーザーの資格情報を使用して再度ログインします

   完了!

   専用の [!DNL Marketo Measure] プロファイルにアクセスするには、Adobeアカウントチーム（担当のアカウントマネージャー）に問い合わせるか、 [Marketoサポート](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"}.
