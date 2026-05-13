---
unique-page-id: 18874741
description: IFrame フォームと  [!DNL Marketo Measure]  -  [!DNL Marketo Measure]
title: IFrame フォームと [!DNL Marketo Measure]
exl-id: fe8d7403-27be-4702-a1b6-d574e1243c0a
feature: Tracking
TQID: https://experienceleague.adobe.com/qR5a7F-h839nvcMRlQ6x6qjkQK3plhZO30aEzqxD00s
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 191
ht-degree: 86%

---

# IFrame フォームと [!DNL Marketo Measure] {#iframe-forms-and-marketo-measure}

[!DNL Marketo Measure] の主な機能の 1 つは、サイト上のセッションやフォームの送信を通じてデジタルマーケティング活動を追跡することです。 一般に、Marketo JavaScript がサイトに配置されると、サイト上のすべてのフォームに自動的に添付されます。 ただし、フォームが IFrame に含まれている場合、この機能には制限が生じます。

IFrame はページ内のページと考えてください。そのため、スクリプトをサイトのすべてのページに追加するようリクエストする場合と同様に、確実にトラッキングするにはスクリプトを IFrame 内に配置する必要があります。

多くの場合、IFrame はマーケティングオートメーションプロバイダーを通じて管理されるので、そのプラットフォーム内またはフォームプロバイダーを通じて設定する必要があります。

JavaScript を IFrame の先頭に配置することをお勧めします。そこから、そのフレーム内のフォームに自動的に添付されます。

![](assets/1-1.png)

JavaScriptをIFrame フォームに追加する方法について質問がある場合は、Adobe アカウントチーム（アカウントマネージャー）または[Marketo サポート &#x200B;](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"}にお問い合わせください。
