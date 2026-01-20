---
unique-page-id: 18874753
description: 実  [!DNL Marketo Measure] Formsへの追加 –  [!DNL Marketo Measure]
title: Act-On フォームへの [!DNL Marketo Measure] の追加
exl-id: 3d246e6a-ad3b-4683-b2b7-ab3f0f4c5ab2
feature: Tracking
source-git-commit: 666812e8bf095170d611cd694b5d0ac5151d8fdd
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 6%

---

# Act-On Formsへの [!DNL Marketo Measure] の追加 {#adding-marketo-measure-to-act-on-forms}

## 道順 {#directions}

1. 編集するフォームで、右隅にある「**[!UICONTROL 設定]**」オプションを選択します。
1. 「外部 web 分析 [!UICONTROL &#x200B; というラベルの付いた領域を探します。] これは、[!DNL Marketo Measure] トラッキングコードスニペットをドロップする場所になります。

## [!DNL Marketo Measure] JavaScript {#marketo-measure-javascript}

`script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

>[!NOTE]
>
>この領域には、[!DNL Google Analytics] コードなど、既に他のトラッキングコードスニペットが存在する場合があります。 次のように、セミコロン `;` と 1 つのスペースを使用して、区切ってください。
>
>`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>**; **<script async="true" type="someothercode" src="someotherfile.js" ></script>`
