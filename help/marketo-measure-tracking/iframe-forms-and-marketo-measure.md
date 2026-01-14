---
description: Marketo Measure ユーザー向けの IFrame Forms and [!DNL Marketo Measure] guidance
title: IFrame フォームと [!DNL Marketo Measure]
exl-id: fe8d7403-27be-4702-a1b6-d574e1243c0a
feature: Tracking
source-git-commit: fcd8e276c85669ddf12bd7404fb12d3e99b2642a
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 77%

---

# IFrame フォームと [!DNL Marketo Measure] {#iframe-forms-and-marketo-measure}

[!DNL Marketo Measure] の主な機能の 1 つは、サイト上のセッションやフォームの送信を通じてデジタルマーケティング活動を追跡することです。一般に、Marketo JavaScript がサイトに配置されると、サイト上のすべてのフォームに自動的に添付されます。ただし、フォームが IFrame に含まれている場合、この機能には制限が生じます。

IFrame はページ内のページと考えてください。そのため、スクリプトをサイトのすべてのページに追加するようリクエストする場合と同様に、確実にトラッキングするにはスクリプトを IFrame 内に配置する必要があります。

多くの場合、IFrame はマーケティングオートメーションプロバイダーを通じて管理されるので、そのプラットフォーム内またはフォームプロバイダーを通じて設定する必要があります。

JavaScript を IFrame の先頭に配置することをお勧めします。そこから、そのフレーム内のフォームに自動的に添付されます。

![JavaScriptは、の先頭部分に配置することをお勧めします &#x200B;](assets/adding-pages-1.png)

JavaScriptの IFrame フォームへの追加に関するご質問は、Adobe アカウントチーム（アカウントマネージャー）または [Marketo サポート &#x200B;](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"} にお問い合わせください。
