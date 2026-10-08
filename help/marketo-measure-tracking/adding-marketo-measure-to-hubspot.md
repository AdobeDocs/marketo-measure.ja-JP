---
description: Marketo Measure ユーザーの[!DNL Marketo Measure]を[!DNL Hubspot]に追加しています
title: '[!DNL Marketo Measure]を[!DNL Hubspot]に追加中'
exl-id: 633e7ef7-7959-461e-881f-dcc543595b66
feature: Tracking
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
    internal-label: Marketo Measure
feature_v2:
  - id: dcbeff6e-0253-5a4b-9ac2-1b67cc4a6286
    internal-label: Tracking
source-git-commit: 940fee4abd0e09b6bf513b5e7526d3c242bd31c7
workflow-type: tm+mt
source-wordcount: '184'
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

```html
<!-- Marketo Measure Javascript -->
<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async="">
```

>[!TIP]
>
>Google Analyticsのコードなど、他のトラッキングコードスニペットが既にこの領域に存在する場合があります。 次のように、セミコロン `;`と1つのスペースで区切ってください。
>
>`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>; <script async="true" type="someothercode" src="someotherfile.js" ></script>`
