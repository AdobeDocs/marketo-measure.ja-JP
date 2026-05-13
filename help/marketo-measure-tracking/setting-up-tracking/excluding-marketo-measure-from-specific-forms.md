---
unique-page-id: 18874783
description: 特定のFormsから [!DNL Marketo Measure] を除外しています –  [!DNL Marketo Measure]
title: 特定のフォームからの [!DNL Marketo Measure] の除外
exl-id: ce39a3b2-2ac6-4385-b6d1-3c36b51c03fa
feature: Tracking
TQID: https://experienceleague.adobe.com/RtGjsV86NEJPvUpFGnthwVGsQVpX0LqMQdC2xBSFwZc
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 93
ht-degree: 3%

---

# 特定のFormsから[!DNL Marketo Measure]を除外しています {#excluding-marketo-measure-from-specific-forms}

既定では、サイトのすべてのフォームに[!DNL Marketo Measure]が添付されます。 ただし、すべてのフォーム送信が必ずしも追跡されるか、アトリビューションモデルに含まれる必要はありません。 これは、すべてのフォーム入力が「良好」と見なされるわけではないからです。 たとえば、登録解除ページやフォームがあります。 さらに、ログインフォームはアトリビューションモデルを希薄化するため、通常は追跡されません。

## [!DNL Marketo Measure]-exclude コードの追加方法：  {#how-to-add-marketo-measure-exclude-code}

[!DNL Marketo Measure]が特定のフォームをトラッキングできないようにするには、フォームに「[!DNL Bizible-Exclude]」を「クラス」として追加するだけです。 コードは次のとおりです。

`<form id="myForm" action="/Home/TestPage" method="POST" class="Bizible-Exclude">`
