---
description: SalesforceのIP範囲を「Marketo Measure」にリストして、セッション制限が適用されたときに許可リストに加えるが接続できるようにします
title: セキュリティセッションの制限 – 許可リストへのIP アドレス
exl-id: aaf5190f-893c-4872-8d03-93f516e70a59
feature: Tracking
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
    internal-label: Marketo Measure
feature_v2:
  - id: dcbeff6e-0253-5a4b-9ac2-1b67cc4a6286
    internal-label: Tracking
source-git-commit: 940fee4abd0e09b6bf513b5e7526d3c242bd31c7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 12%
---
# セキュリティセッション制限：許可リストに登録する IP アドレス {#security-session-restrictions-ip-addresses-to-allowlist}

特定のIP アドレスが[!DNL Salesforce] インスタンスにデータをプッシュ/プルすることを防ぐ[Session Security Settings](https://help.salesforce.com/articleView?id=admin_sessions.htm&type=0){target="_blank"}が設定されている場合、[!DNL Marketo Measure]が[!DNL Salesforce]にデータをプッシュできるようにするには、次のIP範囲を許可リストに加えるする必要があります。

* 52.162.84.192 - 52.162.84.207
* 23.100.229.112 - 23.100.229.127
* 20.186.163.0 - 20.186.163.15

[!DNL Marketo Measure]個のIPをSalesforceの信頼済みIP範囲に追加するには、**[!UICONTROL 設定]** > **[!UICONTROL 管理セットアップ]** > **[!UICONTROL セキュリティコントロール]** > **[!UICONTROL ネットワークアクセス]** > **[!UICONTROL 新規]**&#x200B;をクリックします。

![Marketo Measure IPを](assets/compliance-resources-1.png)の信頼済みIP範囲に追加するには
