---
unique-page-id: 18874753
description: アクション オン Formsに [!DNL Marketo Measure] を追加しています –  [!DNL Marketo Measure]
title: Act-On フォームへの [!DNL Marketo Measure] の追加
exl-id: 3d246e6a-ad3b-4683-b2b7-ab3f0f4c5ab2
feature: Tracking
TQID: https://experienceleague.adobe.com/BUdHiCxfaG7a8Tays-Oqg9ZJQjSZJMM4-ChPHuF0RCg
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 77
ht-degree: 6%

---

# [!DNL Marketo Measure]をAct-On Formsに追加しています {#adding-marketo-measure-to-act-on-forms}

## 方向 {#directions}

1. 編集中のフォームで、右隅にある「**[!UICONTROL 設定]**」オプションを選択します。
1. [!UICONTROL &quot;External Web Analytics.&quot;]というラベルの付いた領域を探します これは、[!DNL Marketo Measure] トラッキングコードスニペットをドロップする場所です。

## [!DNL Marketo Measure] JavaScript {#marketo-measure-javascript}

`script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

>[!NOTE]
>
>この領域には、[!DNL Google Analytics] コードなど、他のトラッキングコードスニペットが既に存在する可能性があります。 セミコロン `;`と1つのスペースを使用して、次のように区切ってください。
>
>`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>**; **<script async="true" type="someothercode" src="someotherfile.js" ></script>`
