---
unique-page-id: 18874755
description: ' [!DNL Marketo Measure] を [!DNL Marketo]  ランディングページに追加 –  [!DNL Marketo Measure]'
title: Marketo ランディングページ [!DNL Marketo Measure] の追加
exl-id: 3771d4d2-8723-452a-b23d-cea3b11ab9ee
feature: Tracking
TQID: https://experienceleague.adobe.com/oMudhh5HLf2i618ZV7RjLNMCsYYgxKoO-hp1g6ia85U
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 9%

---

# Marketo ランディングページへの[!DNL Marketo Measure]の追加 {#adding-marketo-measure-to-marketo-landing-pages}

追加の処理が必要なため、[!DNL Marketo Engage] ランディングページにトラッキングを追加する方法について説明します。[!DNL Marketo Measure] JavaScriptは、ランディングページと[!DNL Marketo Engage] フォーム自体の両方に配置されている必要があります。 これを行うには、次の手順に従って、[!DNL Marketo Measure] JavaScriptを[!DNL Marketo Engage]に読み込む必要があります。

>[!NOTE]
>
>[!DNL Google Tag Manager]などのタグ管理プロバイダーを通じてJavaScriptをデプロイする場合、[!DNL Marketo Measure] JSを[!DNL Marketo Engage]に手動で追加する必要はありません。

## [!DNL Marketo Engage] ランディングページに[!DNL Marketo Measure] スクリプトを追加する方法 {#how-to-add-marketo-measure-script-to-marketo-engage-landing-pages}

1. [!DNL Marketo Engage] アカウントにログインします。
1. ランディングページを選択し、「**[!UICONTROL ドラフトを編集]**」をクリックします。
1. HTML要素をドラッグします。
1. [!DNL Marketo Measure] JavaScriptを[!UICONTROL head] セクションに入力します。

   `<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

以下のスクリーンショットの例

1. 「**[!UICONTROL 保存]**」をクリックします。

   ![](assets/adding-bizible-to-marketo-landing-pages-1.png)

## そのほかの備考 {#additional-notes}

* [!DNL Google Analytics] コードなど、他のトラッキングコードスニペットを既に使用している場合があります。 これについては問題ありません。必ずセミコロン `;`と1つのスペースで区切ってください。 例えば、次のようになります。

`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>; <script async="true" type="someothercode" src="someotherfile.js" ></script>`

* 複数のランディングページテンプレートを使用している場合は、必ずフォームを持つすべてのテンプレートにコードを追加してください。

* ランディングページのテンプレートを編集する際に、ランディングページが使用するページを再承認する必要がある場合があります。 この記事では、[一括承認の方法](https://experienceleague.adobe.com/docs/marketo/using/product-docs/demand-generation/landing-pages/landing-page-actions/approve-multiple-landing-pages-at-once.html?lang=ja){target="_blank"}について説明します。
