---
description: セキュリティセッションの制限 – IP アドレスから許可リスト
title: セキュリティセッションの制限 – IP アドレスから許可リスト
exl-id: aaf5190f-893c-4872-8d03-93f516e70a59
feature: Tracking
source-git-commit: c6090ce0c3ac60cd68b1057c369ce0b3b20aeeee
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 8%

---


# セキュリティセッションの制限：許可リストに追加する IP アドレス {#security-session-restrictions-ip-addresses-to-allowlist}

[Session Security Settings](https://help.salesforce.com/articleView?id=admin_sessions.htm&type=0){target="_blank"} が設定され、特定の IP アドレスによる [!DNL Salesforce] インスタンスへのデータのプッシュ/プルが防止されている場合は、[!DNL Marketo Measure] ーザーがデータを [!DNL Salesforce] にプッシュできるように、次の IP 範囲を許可リストに加えるする必要があります。

* 52.162.84.192 - 52.162.84.207
* 23.100.229.112 - 23.100.229.127
* 20.186.163.0 - 20.186.163.15

Salesforceで信頼済み IP 範囲に [!DNL Marketo Measure] の IP を追加するには、**[!UICONTROL 設定]**/**[!UICONTROL 管理設定]**/**[!UICONTROL セキュリティ制御]**/**[!UICONTROL ネットワークアクセス]**/**[!UICONTROL 新規]** をクリックします。

![ 信頼できる IP 範囲を追加するためのSalesforce ネットワーク アクセス ページ ](assets/1.png)
