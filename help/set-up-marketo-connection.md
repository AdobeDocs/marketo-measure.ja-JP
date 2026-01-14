---
description: Marketo Measure ユーザー用のMarketo接続ガイダンスの設定
title: Marketo連携の設定
exl-id: 11660539-1cc5-4768-8f22-d6f7cd0b94f3
feature: Integration
source-git-commit: fcd8e276c85669ddf12bd7404fb12d3e99b2642a
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 4%

---

# Marketo連携の設定 {#set-up-marketo-connection}

Marketoへの接続を設定する方法を以下に示します。

>[!PREREQUISITES]
>
>[/Marketo Engage連携の &#x200B;](https://experienceleague.adobe.com/docs/marketo/using/product-docs/administration/users-and-roles/create-an-api-only-user.html?lang=ja)API のみのユーザーの役割を作成 [!DNL Marketo Measure] します。

1. [!DNL Marketo Measure] で、「**[!UICONTROL マイアカウント]**」ドロップダウンをクリックし、「**[!UICONTROL 設定]**」を選択します。

   ![1.Marketo Measureで、マイアカウント ドロップダウンをクリックし、](assets/set-connection-7.png) の操作を行います。

1. [!UICONTROL &#x200B; 統合 &#x200B;] で、「**[!UICONTROL 接続]**」をクリックします。

   ![1.「統合」で、「接続」をクリックします。](assets/set-connection-8.png)

1. **[!UICONTROL 新しい CRM 接続の設定]** をクリックします。

   ![1.「新しい CRM 接続の設定」をクリックします。](assets/set-connection-9.png)

1. Marketoの横にある **[!UICONTROL 接続]** ボタンをクリックします。

   ![1.Marketo.](assets/set-connection-5.png) の横にある「接続」ボタンをクリックします。

1. 新しいタブで、Marketo Engage アカウントにログインします。 **管理者**/**Web サービス** に移動します。 REST API まで下にスクロールします。 エンドポイント ID サービスの URL をハイライト表示して保存します。 これらは、次の手順で必要になります。

   ![1.新しいタブで、Marketo Engage アカウントにログインします。](assets/set-connection-6.png)

1. Marketo Engageのまま、左側のツリーで「**LaunchPoint**」を選択します。 Marketo Measureに接続するカスタムサービスを見つけて、「**詳細を表示**」をクリックします。

   ![1.Marketo Engageのまま、](assets/set-connection-4.png) のツリーで「LaunchPoint」を選択します。

1. 「クライアント ID」と「クライアント秘密鍵」をハイライト表示して保存します。 「**閉じる**」をクリックします。

   ![1.「クライアント ID」と「クライアント秘密鍵」をハイライト表示して保存します。 「閉じる」をクリックします。](assets/set-connection-3.png)

1. [!DNL Marketo Measure] に戻り、収集したデータをフィールドに入力します。

   ![1.Marketo Measureに戻り、フィールドにデータを入力し &#x200B;](assets/set-connection-1.png) す。

1. 値を入力したら、「**[!UICONTROL 認証]**」をクリックします。 Marketo Engage アカウントが [!DNL Marketo Measure] に接続されています。

   ![1.値を入力したら、「認証」をクリックします。 Marketo Engage](assets/set-connection-2.png)

   >[!NOTE]
   >
   >[!DNL Marketo Measure] は、Marketo API の制限を消費することなく、あなたに代わってMarketo API への呼び出しを行うので、他の統合機能によるキャップやクレジット配分について心配する必要はありません。
