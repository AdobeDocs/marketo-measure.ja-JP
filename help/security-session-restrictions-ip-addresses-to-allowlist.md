---
description: セッション制限が適用されるときにMarketo Measureが接続できるように、Salesforce許可リストに加えるの IP 範囲をリストに表示します。
title: セキュリティセッションの制限 – IP アドレスから許可リスト
exl-id: aaf5190f-893c-4872-8d03-93f516e70a59
feature: Tracking
source-git-commit: fcd8e276c85669ddf12bd7404fb12d3e99b2642a
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 7%

---

# セキュリティセッションの制限：許可リストに追加する IP アドレス {#security-session-restrictions-ip-addresses-to-allowlist}

[Session Security Settings](https://help.salesforce.com/articleView?id=admin_sessions.htm&type=0){target="_blank"} が設定され、特定の IP アドレスによる [!DNL Salesforce] インスタンスへのデータのプッシュ/プルが防止されている場合は、[!DNL Marketo Measure] ーザーがデータを [!DNL Salesforce] にプッシュできるように、次の IP 範囲を許可リストに加えるする必要があります。

* 52.162.84.192 - 52.162.84.207
* 23.100.229.112 - 23.100.229.127
* 20.186.163.0 - 20.186.163.15

Salesforceで信頼済み IP 範囲に [!DNL Marketo Measure] の IP を追加するには、**[!UICONTROL 設定]**/**[!UICONTROL 管理設定]**/**[!UICONTROL セキュリティ制御]**/**[!UICONTROL ネットワークアクセス]**/**[!UICONTROL 新規]** をクリックします。

![&#x200B; で信頼済み IP 範囲にMarketo Measure IP を追加するには &#x200B;](assets/compliance-resources-1.png)
