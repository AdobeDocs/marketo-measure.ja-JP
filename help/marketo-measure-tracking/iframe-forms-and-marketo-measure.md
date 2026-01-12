---
description: IFrame フォームと  [!DNL Marketo Measure]  -  [!DNL Marketo Measure]
title: IFrame フォームと [!DNL Marketo Measure]
exl-id: fe8d7403-27be-4702-a1b6-d574e1243c0a
feature: Tracking
source-git-commit: c6090ce0c3ac60cd68b1057c369ce0b3b20aeeee
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 85%

---


# IFrame フォームと [!DNL Marketo Measure] {#iframe-forms-and-marketo-measure}

[!DNL Marketo Measure] の主な機能の 1 つは、サイト上のセッションやフォームの送信を通じてデジタルマーケティング活動を追跡することです。一般に、Marketo JavaScript がサイトに配置されると、サイト上のすべてのフォームに自動的に添付されます。ただし、フォームが IFrame に含まれている場合、この機能には制限が生じます。

IFrame はページ内のページと考えてください。そのため、スクリプトをサイトのすべてのページに追加するようリクエストする場合と同様に、確実にトラッキングするにはスクリプトを IFrame 内に配置する必要があります。

多くの場合、IFrame はマーケティングオートメーションプロバイダーを通じて管理されるので、そのプラットフォーム内またはフォームプロバイダーを通じて設定する必要があります。

JavaScript を IFrame の先頭に配置することをお勧めします。そこから、そのフレーム内のフォームに自動的に添付されます。

![HTML コード ](assets/1-1.png)

JavaScriptの IFrame フォームへの追加に関するご質問は、Adobe アカウントチーム（アカウントマネージャー）または [Marketo サポート ](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"} にお問い合わせください。
