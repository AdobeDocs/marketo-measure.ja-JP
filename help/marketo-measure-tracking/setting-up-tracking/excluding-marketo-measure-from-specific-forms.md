---
unique-page-id: 18874783
description: 特定  [!DNL Marketo Measure] Formsからの除外 –  [!DNL Marketo Measure]
title: 特定のフォームからの [!DNL Marketo Measure] の除外
exl-id: ce39a3b2-2ac6-4385-b6d1-3c36b51c03fa
feature: Tracking
source-git-commit: 666812e8bf095170d611cd694b5d0ac5151d8fdd
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 4%

---

# 特定のFormsからの [!DNL Marketo Measure] の除外 {#excluding-marketo-measure-from-specific-forms}

デフォルトでは、[!DNL Marketo Measure] はサイト上のすべてのフォームに添付します。 ただし、必ずしもすべてのフォーム送信を追跡したり、属性モデルに含めたりする必要があるわけではありません。 これは、すべてのフォーム入力が「良好」と見なされるわけではないからです。 例えば、登録解除ページ/フォームなどです。 さらに、ログインフォームはアトリビューションモデルを希薄化させるので、通常、追跡されません。

## [!DNL Marketo Measure] 除外コードの追加方法：  {#how-to-add-marketo-measure-exclude-code}

[!DNL Marketo Measure] が特定のフォームを追跡できないようにするには、フォーム上で「[!DNL Bizible-Exclude]」を「クラス」として追加します。 コードは次のようになります。

`<form id="myForm" action="/Home/TestPage" method="POST" class="Bizible-Exclude">`
