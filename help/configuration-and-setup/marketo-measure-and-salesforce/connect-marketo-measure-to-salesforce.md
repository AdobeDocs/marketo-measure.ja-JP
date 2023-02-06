---
unique-page-id: 18874580
description: Marketo Measureを Salesforce に接続 — [!DNL Marketo Measure]  — 製品ドキュメント
title: Marketo Measureを Salesforce に接続
exl-id: 9be8d3fa-1045-4e41-bc2e-5b9d4d3513ae
source-git-commit: 993a326c377b3b6ff48c4e0114b59297f9ca2ca6
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# Marketo Measureを Salesforce に接続 {#connect-marketo-measure-to-salesforce}

この記事では、 [!DNL Salesforce] アカウント [!DNL Marketo Measure] アカウント

## 接続中 [!DNL Marketo Measure] と [!DNL Salesforce] {#connecting-marketo-measure-with-salesforce}

1. 匿名ブラウザーを使用してにログイン [!DNL Marketo Measure].

1. 画面上部のメニューバーで、に移動します。 **[!UICONTROL マイアカウント]** をクリックし、 [!UICONTROL 設定] オプション。

1. 左側の設定オプションの列で、 [!UICONTROL 接続] の下に位置する [!UICONTROL 統合] 」セクションに入力します。

   ![](assets/1.png)

1. 「接続」の「 CRM 」セクションで、 **[!UICONTROL 新しい CRM 接続の設定]**.

   ![](assets/2.png)

1. CRM 接続を選択するよう求めるポップアップウィンドウが表示されます。 次をクリック： [!UICONTROL 接続] ボタン [!DNL Salesforce] ロゴ

   ![](assets/3.png)

1. 最後のポップアップウィンドウが表示され、 [!DNL Salesforce] 資格情報、サンドボックス、実稼動環境。 情報を入力し、 **[!UICONTROL 許可]** アカウントを接続する [!DNL Marketo Measure].

>[!NOTE]
>
>[!DNL Marketo Measure] 1 つにしか接続できません [!DNL Salesforce] インスタンスを一度に作成します。
>
>* A [!DNL Marketo Measure] インスタンスを SFDC サンドボックスインスタンスに接続して、SFDC 本番インスタンスに接続を切り替える前に統合をテストできます。
>* SFDC サンドボックスで最初にテストする場合は、リード、連絡先、アカウント、商談、キャンペーン、事例の各オブジェクトのフィールドに関して、SFDC 本番インスタンスの正確なレプリカを使用してテストすることを強くお勧めします。 実稼動環境で、リード、連絡先、アカウント、商談、キャンペーン、および事例オブジェクトの更新時に実行されるアクティブな APEXトリガーがある場合は、サンドボックス内でそれらをアクティブにしてみる必要があります。
>* テストが完了したら、 [!DNL Marketo Measure] 実稼動環境を指すアカウント [!DNL Salesforce] （サンドボックスの代わりに） [!DNL Salesforce]) をクリックします。 統合の構築方法により、 [!DNL Marketo Measure] アカウントが実稼動に接続されています [!DNL Salesforce]に戻って、サンドボックスに接続することはできません。 [!DNL Salesforce] 組織


