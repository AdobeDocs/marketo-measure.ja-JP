---
description: Data Warehouseアクセス — 直接共有 — 製品ドキュメント
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

の場合 [!DNL Marketo Measure] data warehouse への直接共有を設定するには、次の要件を満たす必要があります。

* 独自のSnowflakeインスタンスがある。
* Snowflakeインスタンスが Azure East US 2Snowflake地域にあります。
* 次の項目を指定します。 [!DNL Marketo Measure] をSnowflakeアカウント id に設定します。

## 制限事項 {#limitations}

[!DNL Marketo Measure] は、現在のSnowflakeの直接共有の制限により、Azure East US 2 にあるアカウントとのみSnowflakeの直接共有を設定できます。 他のSnowflake地域でデータを利用できるようにする必要がある場合は、Azure East US 2 にあるSnowflakeアカウントでデータのコピーを作成し、 [Snowflakeデータベースのレプリケーション](https://docs.snowflake.com/en/user-guide/database-replication-intro.html){target="_blank"} の機能を使用して、選択したSnowflake地域/アカウントにデータをコピーできます。

## Snowflakeアカウント ID を入力 {#enter-snowflake-account-id}

を開きます。 **設定** セクションに移動して、 **Data Warehouse** ページに貼り付けます。 Adobe Analytics の **直接共有** セクションに、 [Snowflakeアカウント ID](https://docs.snowflake.com/en/user-guide/admin-account-identifier.html){target="_blank"} が表示されたボックスで、をクリックします。 **接続**.

![](assets/data-warehouse-access-direct-share-1.png)

## 共有へのアクセス {#accessing-the-share}

指定したアカウント ID の共有を作成したら、 [設定手順](https://docs.snowflake.com/en/user-guide/data-share-consumers.html){target="_blank"} をSnowflakeインスタンス内でクリックして、データにアクセスします。

>[!NOTE]
>
>任意のデータベース名を選択できます。 Snowflakeインスタンス内に存在する限り、任意の役割に権限を割り当てることができます。

* アカウント管理者の役割を使用する

```
USE ROLE ACCOUNTADMIN
```

* 使用可能な共有を表示（付与された共有の名前が表示されます）

```
SHOW SHARES
```

* 共有用のデータベースを作成する

```
CREATE DATABASE <database_name> FROM SHARE <provider_account>.<share_name>
```

* 共有データベースに対する権限の付与

```
GRANT IMPORTED PRIVILEGES ON DATABASE <database_name> TO ROLE <role_name>
GRANT IMPORTED PRIVILEGES ON ALL SCHEMAS IN DATABASE <database_name> TO ROLE <role_name>
```

これらの手順をSnowflakeUI から実行する手順と詳細については、を参照してください。 [Snowflakeのドキュメントを直接](https://docs.snowflake.com/en/user-guide/data-share-consumers.html){target="_blank"}.
