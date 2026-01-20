---
unique-page-id: 18874759
description: 追加  [!DNL Marketo Measure] to [!DNL Hubspot] - [!DNL Marketo Measure]
title: 追加  [!DNL Marketo Measure]  先  [!DNL Hubspot]
exl-id: 633e7ef7-7959-461e-881f-dcc543595b66
feature: Tracking
source-git-commit: 666812e8bf095170d611cd694b5d0ac5151d8fdd
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 1%

---

# [!DNL Marketo Measure] への [!DNL Hubspot] の追加 {#adding-marketo-measure-to-hubspot}

[!DNL Marketo Measure] JavaScriptを追加して、[!DNL Hubspot] ランディングページとフォーム送信をトラッキングする方法を説明します。

Hubspot は、ランディングページ/フォームや web サイトをホストできるという点で、他のマーケティング自動化システムとは少し異なります。 以下の手順は、[!DNL Marketo Measure] ーザーがホストするページでアクティビティ [!DNL Hubspot] 追跡するためのものです。 [!DNL Hubspot] 以外のCMS（Wordpress など）を使用して web サイトの機能を強化する場合は、[!DNL Marketo Measure] JavaScriptもそのCMSに追加する必要があります。

>[!NOTE]
>
>[!DNL Google Tag Manager] などの Tag Management プロバイダーを通じてJavaScriptをデプロイする場合は、[!DNL Marketo Measure] JavaScriptを手動で Web サイトにハードコードする必要はありません。

## はじめに {#getting-started}

[!DNL Hubspot] アカウントにログインしたら、次の手順に従います。

1. コンテンツに移動します。

1. **[!UICONTROL コンテンツ設定]** をクリックします。

1. [!UICONTROL &#x200B; コンテンツ設定 &#x200B;] 内で、「サイトヘッダーHTML」（下図を参照）をクリックします。

1. `<header>` 内に次のスクリプトを追加します。

   `<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

   次のようになります。

```text
<!-- Marketo Measure Javascript -->
<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async="">
```

>[!TIP]
>
>この領域には、Google Analytics コードなど、既に他のトラッキングコードスニペットが存在する場合があります。 次のように、セミコロン `;` と 1 つのスペースで区切ってください。
>
>`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>; <script async="true" type="someothercode" src="someotherfile.js" ></script>`
