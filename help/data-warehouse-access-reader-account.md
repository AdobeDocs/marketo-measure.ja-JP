---
description: リーダーアカウントを設定して使用し、Marketo Measure データウェアハウスにアクセスする方法について説明します
title: データウェアハウスへのアクセス - Reader アカウント
exl-id: 2aa73c41-47ab-4f11-96d8-dafb642308fc
feature: Data Warehouse
source-git-commit: 7a4661c8d42214d32e5360dc45d6d880b08ef37c
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 3%

---

# データウェアハウスへのアクセス - Reader アカウント {#data-warehouse-access-reader-account}

## Snowflake Access Link {#snowflake-access-link}

Snowflake データウェアハウスにアクセスするには、Snowflake アカウントの特定のURLに移動する必要があります。 このアクセス リンクを見つけるには、[!DNL Marketo Measure]にログインし、次の手順に従ってData Warehouse情報ページに移動します。

1. [!DNL Marketo Measure]で、ページの上部にある「**[!UICONTROL 自分のアカウント]**」 > 「**[!UICONTROL 設定]**」をクリックします。

   ![1. Marketo Measureで、ページ上部の「](assets/data-account-7.png)」をクリックします

1. 左側のメニューの「セキュリティ」で、「**[!UICONTROL Data Warehouse]**」をクリックします。

   ![1. 左側のメニューの「セキュリティ」で、「Data Warehouse」をクリックします。](assets/data-account-8.png)

1. このページには、Snowflake データウェアハウスへのリンクとユーザー名が表示されます。

   ![1. このページには、Snowflake データウェアハウスおよび](assets/data-account-9.png)へのリンクがあります

   >[!NOTE]
   >
   >これは、個人ユーザーだけでなく、組織でも利用できる読み取り専用のアカウントです。 [!DNL Marketo Measure]へのアクセス権を持つ組織内のユーザーは、このアカウントを使用してSnowflake Data Warehouse reader アカウントにログインできます。

1. Snowflake URLに記載されているリンクをクリックすると、Snowflake ログインページに移動し、ユーザー名とパスワードを入力します。 _パスワードをお持ちでない場合は、次の手順に従ってパスワードをリセットしてください_。

   ![1. Snowflake URLに記載されているリンクをクリックすると、](assets/data-account-5.png)が表示されます

1. ログインしたら、ページ上部の「**[!UICONTROL ワークシート]**」をクリックします。

   ![1. ログインしたら、上部の「](assets/data-account-6.png)」をクリックします

1. BIZIBLE_ROI_V3 データベースオブジェクトは、画面の左側にあります。 クエリウィンドウの上部にあるドロップダウンオプションから、「ウェアハウス」、「データベース」および「スキーマ」を入力します。 選択肢はそれぞれにつき1つだけ必要です。 これで、Snowflakeのクエリエディターでクエリを実行する準備が整いました。

   ![1. BIZIBLEROIV3 データベース オブジェクトは、](assets/data-account-4.png)の左側にあります

## パスワードのリセット {#reset-your-password}

[!DNL Marketo Measure]さんには、Snowflakeのログインパスワードへのアクセス権がありません。 パスワードをリセットする必要がある場合は、Data Warehouseの情報ページの「[!UICONTROL &#x200B; パスワードをリセット &#x200B;]」ボタンをクリックし、指示に従います。 一時的なパスワードがUIにすぐに表示されます。 次のデータウェアハウスのログイン時に、独自のパスワードを作成するように求められます。

>[!NOTE]
>
>* パスワードをリセットすると、現在ログインしているユーザーだけでなく、組織内のすべての[!DNL Marketo Measure] ユーザーに対してパスワードがリセットされます。
>* UIには一時パスワードのみが表示されます。 メールは送信されません。

![一時的なパスワードのみがUIに表示されます。 電子メールは](assets/data-account-3.png)になります

![一時的なパスワードのみがUIに表示されます。 電子メールは](assets/data-account-1.png)になります

## サードパーティ製ツールを介してSnowflakeに接続する {#connecting-to-snowflake-via-third-party-tools}

Snowflakeとサードパーティ製品を連携させるには、いくつかの情報を入力する必要があります。

>[!NOTE]
>
>各ツールには異なる接続要件があります。接続しようとしている特定のツールのドキュメントを参照することをお勧めします。

* **URI** （常に必須）
   * これは、Snowflake アカウントのドメイン名です。 これは、Snowflake ログインリンクの一部に含まれています。
* **ユーザー名** （常に必須）
   * ユーザー名は、[!DNL Marketo Measure]のData Warehouse情報ページに表示されます。
* **パスワード** （常に必須）
   * これは、Snowflake アカウントに初めてログインしたときに設定したパスワードです。 パスワードをリセットするには、上記の手順を参照してください。
* **データベース名** （必ずしも必須ではありません）
   * データベースは、Snowflakeのデータを格納する場所です。 これはストレージリソースです。 データベース名は、[!DNL Marketo Measure]のData Warehouse情報ページに一覧表示されます。
* **ウェアハウス名** （必ずしも必須ではありません）
   * Snowflakeでは、クエリを実行するのがデータウェアハウスです。 計算リソースです。 ウェアハウス名は、[!DNL Marketo Measure]のData Warehouse情報ページに表示されます。

  ![&#x200B; ウェアハウスは、Snowflakeでクエリを実行するものです。 計算された](assets/data-account-2.png)です
