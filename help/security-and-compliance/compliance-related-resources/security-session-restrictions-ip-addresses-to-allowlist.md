---
unique-page-id: 18874706
description: セキュリティセッションの制限 – IP アドレスからへのアクセス制限 – Marketo Measure – 製品ドキュメント
title: セキュリティセッションの制限 – 許可リストへのIP アドレス
exl-id: aaf5190f-893c-4872-8d03-93f516e70a59
feature: Tracking
TQID: https://experienceleague.adobe.com/Ka7ff5qarBVEm4JdSGCbaUM3Mrug0r3ZOPSKPrnc3Zo
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 84
ht-degree: 8%

---

# セキュリティセッションの制限：許可リストに追加する IP アドレス {#security-session-restrictions-ip-addresses-to-allowlist}

特定のIP アドレスが[!DNL Salesforce] インスタンスにデータをプッシュ/プルすることを防ぐ[Session Security Settings](https://help.salesforce.com/articleView?id=admin_sessions.htm&type=0){target="_blank"}が設定されている場合、[!DNL Marketo Measure]が[!DNL Salesforce]にデータをプッシュできるようにするには、次のIP範囲を許可リストに加えるする必要があります。

* 52.162.84.192 - 52.162.84.207
* 23.100.229.112 - 23.100.229.127
* 20.186.163.0 - 20.186.163.15

[!DNL Marketo Measure]個のIPをSalesforceの信頼済みIP範囲に追加するには、**[!UICONTROL 設定]** > **[!UICONTROL 管理セットアップ]** > **[!UICONTROL セキュリティコントロール]** > **[!UICONTROL ネットワークアクセス]** > **[!UICONTROL 新規]**&#x200B;をクリックします。

![](assets/1.png)
