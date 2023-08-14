---
unique-page-id: 18874783
description: 除外 [!DNL Marketo Measure] 特定のFormsから [!DNL Marketo Measure]  — 製品ドキュメント
title: 特定のフォームからの [!DNL Marketo Measure] の除外
exl-id: ce39a3b2-2ac6-4385-b6d1-3c36b51c03fa
feature: Tracking
source-git-commit: 8ac315e7c4110d14811e77ef0586bd663ea1f8ab
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 8%

---

# 特定のフォームからの[!DNL Marketo Measure]の除外 {#excluding-marketo-measure-from-specific-forms}

デフォルトでは、 [!DNL Marketo Measure] は、サイト上のすべてのフォームに添付します。 ただし、必ずしもすべてのフォーム送信を追跡したり属性モデルに含めたりする必要はありません。 これは、すべてのフォームの入力が「良好」と見なされるわけではないからです。 この例として、購読解除ページやフォームが挙げられます。 さらに、ログインフォームはアトリビューションモデルを希薄化するので、通常は追跡されません。

## 追加方法 [!DNL Marketo Measure]-exclude コード：  {#how-to-add-marketo-measure-exclude-code}

次を防ぐには： [!DNL Marketo Measure] 特定のフォームを追跡する場合は、[!DNL Bizible-Exclude]」をフォームの「クラス」として追加します。 コードは次のようになります。

`<form id="myForm" action="/Home/TestPage" method="POST" class="Bizible-Exclude">`
