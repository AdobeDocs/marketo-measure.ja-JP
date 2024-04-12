---
unique-page-id: 18874741
description: IFrame フォームと  [!DNL Marketo Measure]  -  [!DNL Marketo Measure]
title: IFrame フォームと [!DNL Marketo Measure]
exl-id: fe8d7403-27be-4702-a1b6-d574e1243c0a
feature: Tracking
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: ht
source-wordcount: '185'
ht-degree: 100%

---

# IFrame フォームと [!DNL Marketo Measure] {#iframe-forms-and-marketo-measure}

[!DNL Marketo Measure] の主な機能の 1 つは、サイト上のセッションやフォームの送信を通じてデジタルマーケティング活動を追跡することです。一般に、Marketo JavaScript がサイトに配置されると、サイト上のすべてのフォームに自動的に添付されます。ただし、フォームが IFrame に含まれている場合、この機能には制限が生じます。

IFrame はページ内のページと考えてください。そのため、スクリプトをサイトのすべてのページに追加するようリクエストする場合と同様に、確実にトラッキングするにはスクリプトを IFrame 内に配置する必要があります。

多くの場合、IFrame はマーケティングオートメーションプロバイダーを通じて管理されるので、そのプラットフォーム内またはフォームプロバイダーを通じて設定する必要があります。

JavaScript を IFrame の先頭に配置することをお勧めします。そこから、そのフレーム内のフォームに自動的に添付されます。

![](assets/1-1.png)

IFrame フォームへの JavaScript の追加に関してご質問がある場合は、アドビのアカウントチーム（担当のアカウントマネージャー）または [Marketo サポート](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"}にお問い合わせください。
