---
description: Data Warehouseアクセス —Readerアカウント — 製品ドキュメント
title: Data Warehouseアクセス —Readerアカウント
exl-id: 2aa73c41-47ab-4f11-96d8-dafb642308fc
source-git-commit: f13e55f009f33140ff36523212ed8b9ed5449a4d
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

---

# Data Warehouseアクセス —Readerアカウント {#data-warehouse-access-reader-account}

## Snowflakeアクセスリンク {#snowflake-access-link}

SnowflakeData Warehouse にアクセスするには、Snowflakeアカウントの特定の URL に移動する必要があります。 このアクセスリンクは、 [!DNL Marketo Measure] 次の手順に従って、「Data Warehouse情報」ページに移動します。

1. In [!DNL Marketo Measure]、ページ上部の「 **[!UICONTROL マイアカウント]** > **[!UICONTROL 設定]**.

   ![](assets/data-warehouse-access-reader-account-1.png)

1. 左側のメニューの [ セキュリティ ] で、[ **[!UICONTROL Data Warehouse]**.

   ![](assets/data-warehouse-access-reader-account-2.png)

1. このページには、SnowflakeData Warehouse へのリンクとユーザー名が表示されます。

   ![](assets/data-warehouse-access-reader-account-3.png)

   >[!NOTE]
   >
   >これは、個々のユーザーだけでなく、組織で使用できる読み取り専用アカウントです。 組織内で、にアクセスできるユーザー [!DNL Marketo Measure] このアカウントを使用して、SnowflakeData Warehouseリーダーアカウントにログインできます。

1. SnowflakeURL に記載されているリンクをクリックすると、Snowflakeログインページが開き、ユーザー名とパスワードを入力できます。 _パスワードをお持ちでない場合は、以下の手順を参照してリセットしてください_.

   ![](assets/data-warehouse-access-reader-account-4.png)

1. ログインしたら、「 **[!UICONTROL ワークシート]** をクリックします。

   ![](assets/data-warehouse-access-reader-account-5.png)

1. BIZIBLE_ROI_V3 データベースオブジェクトは画面の左側に表示されます。 クエリー・ウィンドウの上部にあるドロップダウン・オプションから「ウェアハウス」、「データベース」および「スキーマ」を入力します。 それぞれに 1 つのオプションのみを指定します。 これで、クエリクエリエディター内でクエリをSnowflakeする準備が整いました。

   ![](assets/data-warehouse-access-reader-account-6.png)

## パスワードをリセット {#reset-your-password}

[!DNL Marketo Measure] は、お使いのログインパスワードへのSnowflakeアクセス権を持っていません。 パスワードをリセットする必要がある場合は、 [!UICONTROL パスワードをリセット] ボタンをクリックし、Data Warehouse情報ページの指示に従います。 一時パスワードが UI に直ちに表示されます。 次の Data Warehouse ログイン時に、独自のパスワードを作成するよう求められます。

>[!NOTE]
>
>* パスワードをリセットすると、すべての [!DNL Marketo Measure] 現在ログインしているユーザーだけでなく、組織内のユーザー。
>* UI には一時パスワードのみが表示されます。 E メールは送信されません。


![](assets/data-warehouse-access-reader-account-7.png)

![](assets/data-warehouse-access-reader-account-8.png)

## サードパーティSnowflakeを使用したツールへの接続 {#connecting-to-snowflake-via-third-party-tools}

SnowflakeData Warehouse をサードパーティのツールに接続するには、情報をいくつか入力する必要があります。

>[!NOTE]
>
>各ツールには、異なる接続要件があります。接続しようとしている特定のツールについては、ドキュメントを参照することをお勧めします。

* **URI** （常に必須）
   * ドメインアカウントのSnowflake名です。  これは、ログインログインリンクの一部のSnowflake内に含まれます。
* **ユーザー名** （常に必須）
   * ユーザー名は、 [!DNL Marketo Measure].
* **パスワード** （常に必須）
   * これは、初めてSnowflake・アカウントにログインしたときに設定するパスワードです。  パスワードをリセットするには、上記の手順を参照してください。
* **データベース名** （必ずしも必須ではありません）
   * データベースは、データをSnowflakeに格納する場所です。 これはストレージリソースです。 データベース名は、 [!DNL Marketo Measure].
* **ウェアハウス名** （必ずしも必須ではありません）
   * ウェアハウスは、クエリを実行するSnowflakeです。 計算リソースです。  ウェアハウス名は、 [!DNL Marketo Measure].
   ![](assets/data-warehouse-access-reader-account-9.png)
