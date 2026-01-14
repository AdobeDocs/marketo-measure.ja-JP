---
description: リーダーアカウントを設定してMarketo Measure Data Warehouse にアクセスする方法について説明します
title: データウェアハウスへのアクセス - Reader アカウント
exl-id: 2aa73c41-47ab-4f11-96d8-dafb642308fc
feature: Data Warehouse
source-git-commit: fcd8e276c85669ddf12bd7404fb12d3e99b2642a
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 3%

---

# データウェアハウスへのアクセス - Reader アカウント {#data-warehouse-access-reader-account}

## Snowflake アクセスリンク {#snowflake-access-link}

Snowflake Data Warehouse にアクセスするには、Snowflake アカウントの専用 URL に移動する必要があります。 このアクセスリンクは、[!DNL Marketo Measure] にログインし、次の手順に従ってData Warehouseの情報ページに移動すると表示されます。

1. [!DNL Marketo Measure] で、ページ上部の **[!UICONTROL マイアカウント]**/**[!UICONTROL 設定]** をクリックします。

   ![1.Marketo Measureで、ページ上部のをクリックします &#x200B;](assets/data-account-7.png)

1. 左側のメニューの [ セキュリティ ] で、[**[!UICONTROL Data Warehouse]**] をクリックします。

   ![1.左側のメニューの「セキュリティ」で、「Data Warehouse」をクリックします。](assets/data-account-8.png)

1. このページには、Snowflake Data Warehouse へのリンクとユーザー名が記載されています。

   ![1.このページには、Snowflake Data Warehouse へのリンクがあり、](assets/data-account-9.png) のことが可能です。

   >[!NOTE]
   >
   >これは、個々のユーザーだけでなく、組織で使用できる読み取り専用アカウントです。 [!DNL Marketo Measure] へのアクセス権を持つ組織内のすべてのユーザーは、このアカウントを使用してSnowflake Data Warehouse リーダーアカウントにログインできます。

1. Snowflakeの URL に記載されているリンクをクリックすると、Snowflakeのログインページが表示されます。このページで、ユーザー名とパスワードを入力します。 _パスワードがない場合は、次の手順を参照してリセットしてください_。

   ![1.Snowflakeの URL に記載されているリンクをクリックすると、](assets/data-account-5.png) の画面が表示されます。

1. ログインしたら、ページ上部の「**[!UICONTROL ワークシート]**」をクリックします。

   ![1.ログインしたら、](assets/data-account-6.png) のページの上部にある「ワークシート」をクリックします。

1. BIZIBLE_ROI_V3 データベースオブジェクトが画面の左側に表示されます。 クエリー・ウィンドウの上部にあるドロップダウン・オプションから、「ウェアハウス」、「データベース」、「スキーマ」を入力します。 それぞれにオプションは 1 つだけにする必要があります。 これで、Snowflake クエリエディター内でクエリを実行する準備が整いました。

   ![1.BIZIBLEROIV3 データベース オブジェクトは &#x200B;](assets/data-account-4.png) の左側にあります。

## パスワードのリセット {#reset-your-password}

[!DNL Marketo Measure] はSnowflake ログインパスワードへのアクセス権を持っていません。 パスワードをリセットする必要がある場合は、Data Warehouse情報ページの [!UICONTROL &#x200B; パスワードのリセット &#x200B;] ボタンをクリックし、指示に従ってください。 一時パスワードが UI に直ちに表示されます。 次に Data Warehouse にログインする際に、独自のパスワードを作成するよう求められます。

>[!NOTE]
>
>* パスワードをリセットすると、現在ログインしてい [!DNL Marketo Measure] ユーザーだけでなく、組織内のすべてのユーザーに対してパスワードがリセットされます。
>* UI には一時パスワードのみが表示されます。 メールは送信されません。

![UI には一時パスワードのみが表示されます。 電子メールは &#x200B;](assets/data-account-3.png) のようになります。

![UI には一時パスワードのみが表示されます。 電子メールは &#x200B;](assets/data-account-1.png) のようになります。

## サードパーティ製ツールを使用したSnowflakeへの接続 {#connecting-to-snowflake-via-third-party-tools}

Snowflake データウェアハウスをサードパーティのツールに接続するには、いくつかの情報を入力する必要があります。

>[!NOTE]
>
>ツールごとに接続要件が異なります。接続する特定のツールのドキュメントを参照することをお勧めします。

* **URI** （常に必須）
   * これは、Snowflake アカウントのドメイン名です。 Snowflakeのログインリンクの一部に含まれています。
* **ユーザー名** （常に必須）
   * ユーザー名の一覧は、[!DNL Marketo Measure] のData Warehouseの情報ページに表示されます。
* **パスワード** （常に必須）
   * これは、Snowflake アカウントに初めてログインしたときに設定したパスワードです。 パスワードをリセットするには、上記の手順を参照してください。
* **データベース名** （必ずしも必須ではありません）
   * データベースは、Snowflakeにデータを保存するものです。 これはストレージリソースです。 データベース名は、[!DNL Marketo Measure] のData Warehouseの情報ページに一覧表示されます。
* **ウェアハウス名** （必ずしも必須ではありません）
   * ウェアハウスはSnowflakeでクエリを実行するものです。 これは計算されたリソースです。 ウェアハウス名は [!DNL Marketo Measure] のData Warehouse情報ページにリストされます。

  ![&#x200B; ウェアハウスはSnowflakeでクエリを実行するものです。 計算済みです &#x200B;](assets/data-account-2.png)
