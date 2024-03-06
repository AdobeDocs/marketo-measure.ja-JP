---
unique-page-id: 42762762
description: Marketo接続のセットアップ — [!DNL Marketo Measure]
title: Marketo接続のセットアップ
exl-id: 11660539-1cc5-4768-8f22-d6f7cd0b94f3
feature: Integration
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 1%

---

# Marketo接続のセットアップ {#set-up-marketo-connection}

Marketoへの接続を設定する方法を次に示します。

>[!PREREQUISITES]
>
>[API 専用のユーザーロールの作成](https://experienceleague.adobe.com/docs/marketo/using/product-docs/administration/users-and-roles/create-an-api-only-user.html) （の） [!DNL Marketo Measure]/Marketo Engage接続。

1. In [!DNL Marketo Measure]をクリックし、 **[!UICONTROL マイアカウント]** ドロップダウンして「 」を選択します。 **[!UICONTROL 設定]**.

   ![](assets/set-up-marketo-connection-1.png)

1. の下 [!UICONTROL 統合]をクリックし、 **[!UICONTROL 接続]**.

   ![](assets/set-up-marketo-connection-2.png)

1. クリック **[!UICONTROL 新しい CRM 接続の設定]**.

   ![](assets/set-up-marketo-connection-3.png)

1. 次をクリック： **[!UICONTROL 接続]** ボタンをクリックします。Marketo

   ![](assets/set-up-marketo-connection-4.png)

1. 新しいタブで、Marketo Engageアカウントにログインします。 に移動します。 **管理者** > **Web サービス**. 下にスクロールして REST API を表示します。 エンドポイントと ID サービスの URL をハイライトして保存します。 次の手順で必要になります。

   ![](assets/set-up-marketo-connection-5.png)

1. まだMarketo Engage中、 **LaunchPoint** 左の木に。 Marketo Measureに接続するカスタムサービスを見つけ、 **詳細を表示**.

   ![](assets/set-up-marketo-connection-6.png)

1. クライアント ID とクライアント秘密鍵をハイライト表示して保存します。 「**閉じる**」をクリックします。

   ![](assets/set-up-marketo-connection-7.png)

1. 戻る [!DNL Marketo Measure]を設定し、フィールドに収集したデータを入力します。

   ![](assets/set-up-marketo-connection-8.png)

1. 値を入力した後、 **[!UICONTROL 認証]**. Marketo Engageアカウントが [!DNL Marketo Measure].

   ![](assets/set-up-marketo-connection-9.png)

   >[!NOTE]
   >
   >[!DNL Marketo Measure] は、Marketo API の制限を消費することなく、お客様に代わってMarketo API への呼び出しをおこなうので、他の統合との間でキャップやクレジットの割り当てについて心配する必要はありません。
