---
unique-page-id: 18874755
description: 追加中 [!DNL Marketo Measure] から [!DNL Marketo] ランディングページ — [!DNL Marketo Measure]  — 製品ドキュメント
title: 追加中 [!DNL Marketo Measure] Marketoランディングページ
exl-id: 3771d4d2-8723-452a-b23d-cea3b11ab9ee
source-git-commit: 82cc8269bfdb26b6acf039d0ce0e06564f5e2612
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 5%

---

# 追加中 [!DNL Marketo Measure] Marketoランディングページ {#adding-marketo-measure-to-marketo-landing-pages}

にトラッキングを追加する方法を説明します。 [!DNL Marketo Engage] 追加の処理が必要な場合のランディングページ。 [!DNL Marketo Measure] JavaScript は、ランディングページと [!DNL Marketo Engage] フォーム自体に含まれます。 これをおこなうには、 [!DNL Marketo Measure] JavaScript を [!DNL Marketo Engage] 以下の指示に従って説明したように

>[!NOTE]
>
>タグ管理プロバイダー ( [!DNL Google Tag Manager]手動で [!DNL Marketo Measure] JS から [!DNL Marketo Engage].

## 追加方法 [!DNL Marketo Measure] スクリプト [!DNL Marketo Engage] ランディングページ {#how-to-add-marketo-measure-script-to-marketo-engage-landing-pages}

1. にログインします。 [!DNL Marketo Engage] アカウント
1. ランディングページを選択し、「**[!UICONTROL ドラフトを編集]**」をクリックします。
1. HTML要素内にドラッグします。
1. 次を入力します。 [!DNL Marketo Measure] JavaScript を [!UICONTROL head] セクション：

   `<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

下のスクリーンショットの例

1. 「**[!UICONTROL 保存]**」をクリックします。

   ![](assets/adding-bizible-to-marketo-landing-pages-1.png)

## そのほかの備考 {#additional-notes}

* 例えば、既に他のトラッキングコードスニペットが存在している場合もあります。 [!DNL Google Analytics] コード。 これに関して問題はありません。必ずセミコロンで区切ってください `;` 1 つのスペース 次に例を示します。

`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>; <script async="true" type="someothercode" src="someotherfile.js" ></script>`

* 複数のランディングページテンプレートが使用されている可能性があります。フォームを持つすべてのテンプレートに、必ずコードを追加してください。

* ランディングページのテンプレートを編集する際に、ランディングページが使用するページを再承認する必要が生じる場合があります。 この記事では、 [一括承認の方法](https://experienceleague.adobe.com/docs/marketo/using/product-docs/demand-generation/landing-pages/landing-page-actions/approve-multiple-landing-pages-at-once.html){target=&quot;_blank&quot;}。
