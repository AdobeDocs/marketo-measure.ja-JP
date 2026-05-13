---
unique-page-id: 18874759
description: ' [!DNL Marketo Measure] を [!DNL Hubspot] から [!DNL Marketo Measure]に追加中'
title: ' [!DNL Marketo Measure] を [!DNL Hubspot]に追加中'
exl-id: 633e7ef7-7959-461e-881f-dcc543595b66
feature: Tracking
TQID: https://experienceleague.adobe.com/3To9-9GZMHJf6vVOUPTedkJBpqU1TZNxKeVBHIm0PKY
product_v2: id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 177
ht-degree: 1%

---

# [!DNL Marketo Measure]を[!DNL Hubspot]に追加中 {#adding-marketo-measure-to-hubspot}

[!DNL Marketo Measure] JavaScriptを追加して[!DNL Hubspot] ランディングページとフォーム送信をトラッキングする方法について説明します。

Hubspotは、ランディングページ/フォームやweb サイトをホストできるという点で、他のマーケティングオートメーションシステムとは少し異なります。 以下の手順は、[!DNL Hubspot]でホストされているページで[!DNL Marketo Measure]のアクティビティを追跡するためのものです。 [!DNL Hubspot]以外のCMS（Wordpressなど）でweb サイトを強化する場合は、[!DNL Marketo Measure] JavaScriptをそのCMSにも追加する必要があります。

>[!NOTE]
>
>[!DNL Google Tag Manager]などのタグ管理プロバイダーを通じてJavaScriptをデプロイする場合、[!DNL Marketo Measure] JavaScriptを手動でweb サイトにハードコードする必要はありません。

## はじめに {#getting-started}

[!DNL Hubspot] アカウントにログインしたら、次の手順に従います。

1. コンテンツに移動します。

1. **[!UICONTROL コンテンツ設定]**&#x200B;をクリックします。

1. [!UICONTROL Content Settings]内で、サイトヘッダーのHTMLをクリックします（以下の画像を参照）。

1. `<header>`内に次のスクリプトを追加します。

   `<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

   例えば、次のようになります。

```text
<!-- Marketo Measure Javascript -->
<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async="">
```

>[!TIP]
>
>Google Analyticsのコードなど、他のトラッキングコードスニペットが既にこの領域に存在する場合があります。 次のように、セミコロン `;`と1つのスペースで区切ってください。
>
>`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>; <script async="true" type="someothercode" src="someotherfile.js" ></script>`
