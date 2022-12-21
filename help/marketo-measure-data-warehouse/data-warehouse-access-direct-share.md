---
description: Data Warehouseアクセス — 直接共有 — 製品ドキュメント
title: Data Warehouseアクセス — 直接共有
exl-id: 940c3316-5f94-4aa2-a656-aec5eb7b7450
source-git-commit: f13e55f009f33140ff36523212ed8b9ed5449a4d
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Data Warehouseアクセス — 直接共有 {#data-warehouse-access-direct-share}

**要件**

次のために [!DNL Marketo Measure] data warehouse への直接共有を設定するには、次の要件を満たす必要があります。

* 独自のSnowflakeインスタンス
* Snowflakeインスタンスは、Azure East US 2Snowflake地域にあります。
* 次を指定します。 [!DNL Marketo Measure] をSnowflakeアカウント id に設定します。

**制限事項**

[!DNL Marketo Measure] は、現在のSnowflakeの直接共有の制限により、Azure East US 2 にあるアカウントとのみSnowflakeの直接共有を設定できます。 データを他のSnowflake地域で利用可能にする必要がある場合は、Azure East US 2 にあるSnowflakeアカウントでデータのコピーを作成し、 [Snowflakeデータベースのレプリケーション](https://docs.snowflake.com/en/user-guide/database-replication-intro.html){target=&quot;_blank&quot;} 機能を使用して、選択したSnowflake地域/アカウントのデータをコピーできます。

**共有へのアクセス**

指定したアカウント ID の共有を作成したら、 [設定手順](https://docs.snowflake.com/en/user-guide/data-share-consumers.html){target=&quot;_blank&quot;} をSnowflakeインスタンス内で追加して、データにアクセスできるようにします。

>[!NOTE]
>
>任意のデータベース名を選択できます。 選択したルールに権限を割り当てることができます ( ルールがSnowflakeインスタンスに存在する場合 )。

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

これらの手順をSnowflakeUI から実行する手順と詳細については、を参照してください。 [Snowflakeのドキュメントを直接](https://docs.snowflake.com/en/user-guide/data-share-consumers.html){target=&quot;_blank&quot;}。
