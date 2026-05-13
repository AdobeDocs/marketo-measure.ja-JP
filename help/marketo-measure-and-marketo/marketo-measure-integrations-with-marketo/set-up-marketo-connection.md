---
unique-page-id: 42762762
description: Marketo Connectionの設定 –  [!DNL Marketo Measure]
title: Marketo Connectionの設定
exl-id: 11660539-1cc5-4768-8f22-d6f7cd0b94f3
feature: Integration
TQID: https://experienceleague.adobe.com/IQhZzu6iqS-5BdooPRA6-A8BoJtQ936NRFJHPGu3Xp4
product_v2: id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
feature_v2: id: c8f57308-7e33-4e41-a385-b55041c78939
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 206
ht-degree: 8%

---

# Marketo Connectionの設定 {#set-up-marketo-connection}

Marketoへの接続を設定する方法は次のとおりです。

>[!PREREQUISITES]
>
>[[!DNL Marketo Measure]/Marketo Engage接続用のAPIのみのユーザーロール ](https://experienceleague.adobe.com/docs/marketo/using/product-docs/administration/users-and-roles/create-an-api-only-user.html?lang=ja){target="_blank"}を作成します。

1. [!DNL Marketo Measure]で、**[!UICONTROL マイアカウント]** ドロップダウンをクリックし、**[!UICONTROL 設定]**&#x200B;を選択します。

   ![](assets/set-up-marketo-connection-1.png)

1. [!UICONTROL 統合]で、**[!UICONTROL 接続]**&#x200B;をクリックします。

   ![](assets/set-up-marketo-connection-2.png)

1. **[!UICONTROL 新しいCRM接続の設定]**&#x200B;をクリックします。

   ![](assets/set-up-marketo-connection-3.png)

1. Marketoの横にある「**[!UICONTROL Connect]**」ボタンをクリックします。

   ![](assets/set-up-marketo-connection-4.png)

1. 新しいタブで、Marketo Engage アカウントにログインします。 **管理者** > **Web サービス**&#x200B;に移動します。 REST APIまでスクロールダウンします。 エンドポイントとID サービスのURLをハイライト表示して保存します。 次の手順で必要になります。

   ![](assets/set-up-marketo-connection-5.png)

1. まだMarketo Engageで、左側のツリーで「**LaunchPoint**」を選択します。 Marketo Measureに接続するカスタムサービスを見つけて、**詳細を表示**&#x200B;をクリックします。

   ![](assets/set-up-marketo-connection-6.png)

1. クライアント IDとクライアントシークレットをハイライト表示して保存します。 「**閉じる**」をクリックします。

   ![](assets/set-up-marketo-connection-7.png)

1. [!DNL Marketo Measure]に戻って、収集したデータをフィールドに入力します。

   ![](assets/set-up-marketo-connection-8.png)

1. 値を入力したら、**[!UICONTROL 認証]**&#x200B;をクリックします。 お使いのMarketo Engage アカウントは[!DNL Marketo Measure]に接続されています。

   ![](assets/set-up-marketo-connection-9.png)

   >[!NOTE]
   >
   >[!DNL Marketo Measure]は、Marketo APIの制限を使用せずにMarketo APIに代わって呼び出しを行うため、他の統合との上限やクレジット割り当てについて心配する必要はありません。
