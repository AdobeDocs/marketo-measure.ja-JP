---
unique-page-id: 18874580
description: Marketo Measureを Salesforce に接続 — [!DNL Marketo Measure]
title: Marketo Measureを Salesforce に接続
exl-id: 9be8d3fa-1045-4e41-bc2e-5b9d4d3513ae
feature: Salesforce
source-git-commit: 741ab20845de2f3bcde589291d7446a5b4f877d8
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 1%

---

# Marketo Measureを Salesforce に接続 {#connect-marketo-measure-to-salesforce}

この記事では、 [!DNL Salesforce] アカウントを [!DNL Marketo Measure] アカウント。

## 接続中 [!DNL Marketo Measure] 次を使用 [!DNL Salesforce] {#connecting-marketo-measure-with-salesforce}

1. 匿名ブラウザーを使用してにログイン [!DNL Marketo Measure].

1. 画面上部のメニューバーで、に移動します。 **[!UICONTROL マイアカウント]** をクリックし、 **[!UICONTROL 設定]** オプション。

1. 左側の設定オプションの列で、 **[!UICONTROL 接続]** ～の下に位置する [!UICONTROL 統合] 」セクションに入力します。

   ![](assets/connect-marketo-measure-to-salesforce-1.png)

1. 「接続」の「 CRM 」セクションで、 **[!UICONTROL 新しい CRM 接続の設定]**.

   ![](assets/connect-marketo-measure-to-salesforce-2.png)

1. 「 CRM 接続を選択」を選択するよう求めるポップアップウィンドウが表示されます。 クリック **[!UICONTROL 接続]** の横 [!DNL Salesforce] ロゴ。

   ![](assets/connect-marketo-measure-to-salesforce-3.png)

1. 最後のポップアップウィンドウが表示され、 [!DNL Salesforce] 資格情報、サンドボックス、実稼動環境のいずれかです。 情報を入力し、 **[!UICONTROL 許可]** アカウントを接続する [!DNL Marketo Measure].

>[!NOTE]
>
>[!DNL Marketo Measure] 1 つにしか接続できません [!DNL Salesforce] インスタンスを一度に作成します。
>
>* A [!DNL Marketo Measure] インスタンスを SFDC サンドボックスインスタンスに接続して、SFDC 本番インスタンスに接続を切り替える前に統合をテストすることができます。
>* SFDC サンドボックスで最初にテストする場合は、リード、連絡先、アカウント、商談、キャンペーン、ケースの各オブジェクトのフィールドに関して、SFDC 本番インスタンスの正確なレプリカを使用してテストすることを強くお勧めします。 実稼動環境で、リード、連絡先、アカウント、商談、キャンペーン、および事例オブジェクトの更新時に実行されるアクティブな APEXトリガーがある場合は、サンドボックス内でそれらをアクティブにしてみる必要があります。
>* テストが完了したら、 [!DNL Marketo Measure] 実稼動環境を指すアカウント [!DNL Salesforce] （サンドボックスの代わりに） [!DNL Salesforce]) をクリックします。 統合の構築方法により、 [!DNL Marketo Measure] アカウントが実稼動に接続されています [!DNL Salesforce]に戻って、サンドボックスに接続することはできません。 [!DNL Salesforce] 組織。

## API クレジットの使用状況 {#api-credits-usage}

Marketo Measureは、統合ユーザーを通じてクライアントの Salesforce と連携する CRM 統合タスクを採用しています。 このユーザーを介したすべてのデータ交換では、Salesforce API のクレジットが使用されます。 統合ユーザーにクレジットクォータを割り当てる機能があり、この機能を使用して過剰な API 呼び出しを規制できます。 このクォータまたは制限は 24 時間ごとにリセットされます。

この制限には、次の方法でMarketo Measureでアクセスできます。 **マイアカウント** > **設定** > **CRM** > **一般** > **1 日の CRM API 制限**&#x200B;を設定し、テナントに対して設定できます。

![](assets/connect-marketo-measure-to-salesforce-4.png)

### API クレジットの制限の設定 {#setting-a-limit-for-api-credits}

1. に移動します。 **マイアカウント** > **設定**.

1. CRM で、 **一般**. 次のように表示されます。 **1 日の CRM API 制限** オプション。

1. 編集するには、「ロック」アイコンをクリックします。

   ![](assets/connect-marketo-measure-to-salesforce-5.png)

1. 100,000 以上の制限を入力します。 終了したら「**保存**」をクリックします。

   ![](assets/connect-marketo-measure-to-salesforce-6.png)

>[!NOTE]
>
>接続ソリューションで利用可能な Salesforce API クレジットを増やすには、Salesforce 管理者にお問い合わせください [この Salesforce ドキュメント](https://developer.salesforce.com/docs/atlas.en-us.salesforce_app_limits_cheatsheet.meta/salesforce_app_limits_cheatsheet/salesforce_app_limits_platform_api.htm){target="_blank"}.

>[!MORELIKETHIS]
>
>[エラー通知](/help/configuration-and-setup/getting-started-with-marketo-measure/error-notifications.md){target="_blank"}
