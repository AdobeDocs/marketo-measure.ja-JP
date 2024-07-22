---
unique-page-id: 18874755
description: ランディ  [!DNL Marketo Measure]  グペ  [!DNL Marketo]  ジへの追加 –  [!DNL Marketo Measure]
title: Marketo ランディングページ [!DNL Marketo Measure] の追加
exl-id: 3771d4d2-8723-452a-b23d-cea3b11ab9ee
feature: Tracking
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 7%

---

# Marketo ランディングページへの [!DNL Marketo Measure] の追加 {#adding-marketo-measure-to-marketo-landing-pages}

追加の処理が必要なランディングページ [!DNL Marketo Engage] トラッキングを追加する方法を説明します。 JavaScript[!DNL Marketo Measure]、ランディングページと [!DNL Marketo Engage] フォーム自体の両方で配置されている必要があります。 これを行うには、次の手順に従って、[!DNL Marketo Measure] JavaScriptを [!DNL Marketo Engage] に読み込む必要があります。

>[!NOTE]
>
>[!DNL Google Tag Manager] などの Tag Management プロバイダーを通じてJavaScriptをデプロイする場合は、[!DNL Marketo Measure] JS を手動で [!DNL Marketo Engage] に追加する必要はありません。

## ランディングページへ [!DNL Marketo Measure] スクリプト [!DNL Marketo Engage] 追加方法 {#how-to-add-marketo-measure-script-to-marketo-engage-landing-pages}

1. [!DNL Marketo Engage] アカウントにログインします。
1. ランディングページを選択し、「**[!UICONTROL ドラフトを編集]**」をクリックします。
1. HTML要素内をドラッグします。
1. [!UICONTROL head] セクションに [!DNL Marketo Measure] のJavaScriptを入力します。

   `<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

以下のスクリーンショットの例

1. 「**[!UICONTROL 保存]**」をクリックします。

   ![](assets/adding-bizible-to-marketo-landing-pages-1.png)

## そのほかの備考 {#additional-notes}

* [!DNL Google Analytics] コードなど、他のトラッキングコードスニペットが既に用意されている場合もあります。 これは問題ありません。セミコロン `;` と 1 つのスペースで区切ってください。 例えば、次のようになります。

`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>; <script async="true" type="someothercode" src="someotherfile.js" ></script>`

* 複数のランディングページテンプレートを使用している可能性があります。フォームが含まれるすべてのテンプレートに必ずコードを追加してください。

* ランディングページ用のテンプレートを編集する際に、ランディングページが使用されるページを再承認する必要が生じる場合があります。 この記事では [ 一括承認方法 ](https://experienceleague.adobe.com/docs/marketo/using/product-docs/demand-generation/landing-pages/landing-page-actions/approve-multiple-landing-pages-at-once.html){target="_blank"} を説明します。
