---
unique-page-id: 18874706
description: セキュリティセッションの制限 — する IP アド許可リストに加えるレス — Marketo Measure — 製品ドキュメント
title: セキュリティセッションの制限 — する IP アド許可リストに加えるレス
exl-id: aaf5190f-893c-4872-8d03-93f516e70a59
feature: Tracking
source-git-commit: 8ac315e7c4110d14811e77ef0586bd663ea1f8ab
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 11%

---

# セキュリティセッションの制限：許可リストに追加する IP アドレス {#security-session-restrictions-ip-addresses-to-allowlist}

存在する場合 [セッションセキュリティ設定](https://help.salesforce.com/articleView?id=admin_sessions.htm&amp;type=0){target="_blank"} インプレースで、特定の IP アドレスがデータをプッシュ/プルできないようにする [!DNL Salesforce] インスタンス、許可するには次の IP 範囲を許可リストに加えるする必要があります [!DNL Marketo Measure] にデータをプッシュ [!DNL Salesforce]:

* 52.162.84.192 - 52.162.84.207
* 23.100.229.112 - 23.100.229.127
* 20.186.163.0 - 20.186.163.15

追加するには [!DNL Marketo Measure] Salesforce の信頼済み IP 範囲への IP: **[!UICONTROL 設定]** > **[!UICONTROL 管理設定]** > **[!UICONTROL セキュリティ管理]** > **[!UICONTROL ネットワークアクセス]** > **[!UICONTROL 新規]**.

![](assets/1.png)
