---
unique-page-id: 18874759
description: 追加中 [!DNL Marketo Measure] から [!DNL Hubspot] - [!DNL Marketo Measure]
title: 追加中 [!DNL Marketo Measure] から [!DNL Hubspot]
exl-id: 633e7ef7-7959-461e-881f-dcc543595b66
feature: Tracking
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 1%

---

# 追加中 [!DNL Marketo Measure] から [!DNL Hubspot] {#adding-marketo-measure-to-hubspot}

を追加する方法を説明します。 [!DNL Marketo Measure] 追跡する JavaScript [!DNL Hubspot] ランディングページとフォームの送信。

Hubspot は、ランディングページやフォーム、および Web サイトをホストできるという点で、他のマーケティング自動化システムとは少し異なります。 次の手順は、 [!DNL Marketo Measure] ～の活動を追跡する [!DNL Hubspot] — ホストされるページ。 Web サイトの電源を CMS 以外の [!DNL Hubspot] （例えば、Wordpress）、 [!DNL Marketo Measure] JavaScript をその CMS に対しても送信します。

>[!NOTE]
>
>タグ管理プロバイダー ( [!DNL Google Tag Manager]を手動でハードコードする必要はありません。 [!DNL Marketo Measure] JavaScript を Web サイトに挿入します。

## はじめに {#getting-started}

次にログインし、 [!DNL Hubspot] アカウントを作成するには、次の手順に従います。

1. 「コンテンツ」に移動します。

1. クリック **[!UICONTROL コンテンツ設定]**.

1. Within [!UICONTROL コンテンツ設定]、「 Site Header 」HTML（下図を参照）をクリックします。

1. 次のスクリプトを `<header>`:

   `<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

   次のようになります。

```text
<!-- Marketo Measure Javascript -->
<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async="">
```

>[!TIP]
>
>この領域には、既に他のトラッキングコードスニペット (Google Analyticsコードなど ) が存在する場合があります。 必ずセミコロンで区切ってください `;` そして次のような 1 つのスペース
>
>`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>; <script async="true" type="someothercode" src="someotherfile.js" ></script>`
