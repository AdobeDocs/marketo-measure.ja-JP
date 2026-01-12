---
description: データウェアハウスへのアクセス - Reader アカウント
title: データウェアハウスへのアクセス - Reader アカウント
exl-id: 2aa73c41-47ab-4f11-96d8-dafb642308fc
feature: Data Warehouse
source-git-commit: c6090ce0c3ac60cd68b1057c369ce0b3b20aeeee
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 3%

---


# データウェアハウスへのアクセス - Reader アカウント {#data-warehouse-access-reader-account}

## Snowflake アクセスリンク {#snowflake-access-link}

Snowflake Data Warehouse にアクセスするには、Snowflake アカウントの専用 URL に移動する必要があります。 このアクセスリンクは、[!DNL Marketo Measure] にログインし、次の手順に従ってData Warehouseの情報ページに移動すると表示されます。

1. [!DNL Marketo Measure] で、ページ上部の **[!UICONTROL マイアカウント]**/**[!UICONTROL 設定]** をクリックします。

   ![&#x200B; 「マイアカウント」と「設定」のオプションを使用したMarketo Measureのナビゲーションメニュー &#x200B;](assets/data-warehouse-access-reader-account-1.png)

1. 左側のメニューの [ セキュリティ ] で、[**[!UICONTROL Data Warehouse]**] をクリックします。

   ![&#x200B; 「セキュリティ」セクションの「Data Warehouse」オプションを含む設定サイドバー &#x200B;](assets/data-warehouse-access-reader-account-2.png)

1. このページには、Snowflake Data Warehouse へのリンクとユーザー名が記載されています。

   ![Data Warehouseの URL とユーザー名を示すSnowflake情報ページ &#x200B;](assets/data-warehouse-access-reader-account-3.png)

   >[!NOTE]
   >これは、個々のユーザーだけでなく、組織で使用できる読み取り専用アカウントです。 [!DNL Marketo Measure] へのアクセス権を持つ組織内のすべてのユーザーは、このアカウントを使用してSnowflake Data Warehouse リーダーアカウントにログインできます。

1. Snowflakeの URL に記載されているリンクをクリックすると、Snowflakeのログインページが表示されます。このページで、ユーザー名とパスワードを入力します。 _パスワードがない場合は、次の手順を参照してリセットしてください_。

   ![&#x200B; ユーザー名およびパスワードフィールドを含むSnowflake ログインページ &#x200B;](assets/data-warehouse-access-reader-account-4.png)

1. ログインしたら、ページ上部の「**[!UICONTROL ワークシート]**」をクリックします。

   ![&#x200B; 「ワークシート」ナビゲーションオプションを使用したSnowflake インターフェイス &#x200B;](assets/data-warehouse-access-reader-account-5.png)

1. BIZIBLE_ROI_V3 データベースオブジェクトが画面の左側に表示されます。 クエリー・ウィンドウの上部にあるドロップダウン・オプションから、「ウェアハウス」、「データベース」、「スキーマ」を入力します。 それぞれにオプションは 1 つだけにする必要があります。 これで、Snowflake クエリエディター内でクエリを実行する準備が整いました。

   ![BIZIBLE_ROI_V3 データベースとドロップダウンセレクターを含むSnowflake クエリエディター &#x200B;](assets/data-warehouse-access-reader-account-6.png)

## パスワードのリセット {#reset-your-password}

[!DNL Marketo Measure] はSnowflake ログインパスワードへのアクセス権を持っていません。 パスワードをリセットする必要がある場合は、Data Warehouse情報ページの [!UICONTROL &#x200B; パスワードのリセット &#x200B;] ボタンをクリックし、指示に従ってください。 一時パスワードが UI に直ちに表示されます。 次に Data Warehouse にログインする際に、独自のパスワードを作成するよう求められます。

>[!NOTE]
> パスワードをリセットすると、現在ログインしてい [!DNL Marketo Measure] ユーザーだけでなく、組織内のすべてのユーザーに対してパスワードがリセットされます。
> UI には一時パスワードのみが表示されます。 メールは送信されません。

![&#x200B; 「パスワードをリセット」ボタンが表示されたData Warehouseページ &#x200B;](assets/data-warehouse-access-reader-account-7.png)

![&#x200B; パスワードのリセット後に一時的なパスワードの表示 &#x200B;](assets/data-warehouse-access-reader-account-8.png)

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

  ![&#x200B; データベースおよびウェアハウス名の詳細を示すData Warehouse情報ページ &#x200B;](assets/data-warehouse-access-reader-account-9.png)
