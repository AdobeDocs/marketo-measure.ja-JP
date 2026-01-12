---
description: Marketo接続の設定 –  [!DNL Marketo Measure]
title: Marketo連携の設定
exl-id: 11660539-1cc5-4768-8f22-d6f7cd0b94f3
feature: Integration
source-git-commit: c6090ce0c3ac60cd68b1057c369ce0b3b20aeeee
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 1%

---


# Marketo連携の設定 {#set-up-marketo-connection}

Marketoへの接続を設定する方法を以下に示します。

>[!PREREQUISITES]
>
>[/Marketo Engage連携の &#x200B;](https://experienceleague.adobe.com/docs/marketo/using/product-docs/administration/users-and-roles/create-an-api-only-user.html?lang=ja){target="_blank"}API のみのユーザーの役割を作成 [!DNL Marketo Measure] します。

1. [!DNL Marketo Measure] で、「**[!UICONTROL マイアカウント]**」ドロップダウンをクリックし、「**[!UICONTROL 設定]**」を選択します。

   ![&#x200B; 「設定」オプションを使用したMarketo Measureマイアカウントドロップダウン &#x200B;](assets/set-up-marketo-connection-1.png)

1. [!UICONTROL &#x200B; 統合 &#x200B;] で、「**[!UICONTROL 接続]**」をクリックします。

   ![&#x200B; 接続オプションを含む統合メニュー &#x200B;](assets/set-up-marketo-connection-2.png)

1. **[!UICONTROL 新しい CRM 接続の設定]** をクリックします。

   ![&#x200B; 新しい CRM 接続の設定ボタン &#x200B;](assets/set-up-marketo-connection-3.png)

1. Marketoの横にある **[!UICONTROL 接続]** ボタンをクリックします。

   ![Marketo統合オプションの横にある「接続」ボタン &#x200B;](assets/set-up-marketo-connection-4.png)

1. 新しいタブで、Marketo Engage アカウントにログインします。 **管理者**/**Web サービス** に移動します。 REST API まで下にスクロールします。 エンドポイント ID サービスの URL をハイライト表示して保存します。 これらは、次の手順で必要になります。

   ![REST API エンドポイントと ID URL を表示するMarketo web サービスページ &#x200B;](assets/set-up-marketo-connection-5.png)

1. Marketo Engageのまま、左側のツリーで「**LaunchPoint**」を選択します。 Marketo Measureに接続するカスタムサービスを見つけて、「**詳細を表示**」をクリックします。

   ![&#x200B; カスタムサービスを含む LaunchPoint メニューと詳細を表示オプション &#x200B;](assets/set-up-marketo-connection-6.png)

1. 「クライアント ID」と「クライアント秘密鍵」をハイライト表示して保存します。 「**閉じる**」をクリックします。

   ![&#x200B; クライアント ID とクライアント秘密鍵を示す LaunchPoint サービスの詳細 &#x200B;](assets/set-up-marketo-connection-7.png)

1. [!DNL Marketo Measure] に戻り、収集したデータをフィールドに入力します。

   ![&#x200B; エンドポイントと資格情報のフィールドを含むMarketo接続フォーム &#x200B;](assets/set-up-marketo-connection-8.png)

1. 値を入力したら、「**[!UICONTROL 認証]**」をクリックします。 Marketo Engage アカウントが [!DNL Marketo Measure] に接続されています。

   ![&#x200B; 成功したMarketo接続の確認メッセージ &#x200B;](assets/set-up-marketo-connection-9.png)

   >[!NOTE]
   >[!DNL Marketo Measure] は、Marketo API の制限を消費することなく、あなたに代わってMarketo API への呼び出しを行うので、他の統合機能によるキャップやクレジット配分について心配する必要はありません。
