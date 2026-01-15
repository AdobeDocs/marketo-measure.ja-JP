---
description: Marketo Measure ユ  [!DNL Marketo Measure]  ザー向けのForms実践版ガイダンスの追加
title: Act-On フォームへの [!DNL Marketo Measure] の追加
exl-id: 3d246e6a-ad3b-4683-b2b7-ab3f0f4c5ab2
feature: Tracking
source-git-commit: 0299ef68139df574bd1571a749baf1380a84319b
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 6%

---

# Act-On Formsへの [!DNL Marketo Measure] の追加 {#adding-marketo-measure-to-act-on-forms}

## 道順 {#directions}

1. 編集するフォームで、右隅にある「**[!UICONTROL 設定]**」オプションを選択します。
1. 「外部 web 分析 [!UICONTROL  というラベルの付いた領域を探します。] これは、[!DNL Marketo Measure] トラッキングコードスニペットをドロップする場所になります。

## [!DNL Marketo Measure] JavaScript {#marketo-measure-javascript}

`script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

>[!NOTE]
>
>この領域には、[!DNL Google Analytics] コードなど、既に他のトラッキングコードスニペットが存在する場合があります。 次のように、セミコロン `;` と 1 つのスペースを使用して、区切ってください。
>
>`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>**; **<script async="true" type="someothercode" src="someotherfile.js" ></script>`
