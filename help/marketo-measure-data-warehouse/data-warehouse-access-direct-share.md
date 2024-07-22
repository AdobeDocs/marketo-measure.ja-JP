---
description: Data Warehouseアクセス – 直接共有 – 製品ドキュメント
title: データウェアハウスへのアクセス - Direct Share
exl-id: 940c3316-5f94-4aa2-a656-aec5eb7b7450
feature: Data Warehouse
source-git-commit: 1a274c83814f4d729053bb36548ee544b973dff5
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 4%

---

# データウェアハウスへのアクセス - Direct Share {#data-warehouse-access-direct-share}

## 要件 {#requirements}

データウェアハウス [!DNL Marketo Measure] 直接共有を設定するには、次の要件を満たす必要があります。

* 独自のSnowflakeインスタンスを持っています。
* Snowflakeインスタンスは Azure East US 2 Snowflakeリージョンにあります。
* [!DNL Marketo Measure] にSnowflakeアカウント ID を提供します。

## 制限事項 {#limitations}

現在のSnowflake直接共有の制限により、[!DNL Marketo Measure] は Azure East US 2 にあるアカウントでのみSnowflake直接共有を設定できます。 他のSnowflakeリージョンでデータを使用可能にする必要がある場合は、Azure East US 2 にあるSnowflakeアカウントにデータのコピーを作成し、[Snowflakeデータベースレプリケーション ](https://docs.snowflake.com/en/user-guide/database-replication-intro.html){target="_blank"} 機能を使用して、選択したSnowflakeリージョン/アカウントにデータをコピーすることをお勧めします。

## Snowflakeアカウント ID を入力 {#enter-snowflake-account-id}

Marketo Measure アプリで「**設定**」セクションを開き、**Data Warehouse** ページに移動します。 「**直接共有**」セクションで、表示されたボックスに [Snowflakeアカウント ID](https://docs.snowflake.com/en/user-guide/admin-account-identifier.html){target="_blank"} を入力し、「**接続**」をクリックします。

![](assets/data-warehouse-access-direct-share-1.png)

## 共有へのアクセス {#accessing-the-share}

指定したアカウント ID の共有を作成したら、Snowflakeインスタンス内で [ 設定手順 ](https://docs.snowflake.com/en/user-guide/data-share-consumers.html){target="_blank"} を完了して、データにアクセスする必要があります。

>[!NOTE]
>
>任意のデータベース名を選択できます。 Snowflakeインスタンスに権限が存在する限り、任意のロールに権限を割り当てることができます。

* アカウント管理者の役割を使用

```
USE ROLE ACCOUNTADMIN
```

* 使用可能な共有を表示します（付与された共有の名前を表示します）

```
SHOW SHARES
```

* 共有用のデータベースを作成します

```
CREATE DATABASE <database_name> FROM SHARE <provider_account>.<share_name>
```

* 共有データベースに対する権限の付与

```
GRANT IMPORTED PRIVILEGES ON DATABASE <database_name> TO ROLE <role_name>
GRANT IMPORTED PRIVILEGES ON ALL SCHEMAS IN DATABASE <database_name> TO ROLE <role_name>
```

SnowflakeUI からこれらの手順を実行するための詳細な手順については、[Snowflakeのドキュメントを直接参照してください ](https://docs.snowflake.com/en/user-guide/data-share-consumers.html){target="_blank"}。
