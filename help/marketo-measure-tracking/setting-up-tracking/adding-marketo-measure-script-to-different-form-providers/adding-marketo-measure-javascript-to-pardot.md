---
unique-page-id: 18874757
description: 追加中 [!DNL Marketo Measure] JavaScript をに設定 [!DNL Pardot] - [!DNL Marketo Measure]
title: 追加中 [!DNL Marketo Measure] JavaScript をに設定 [!DNL Pardot]
exl-id: e49190ad-aa86-4f8f-a9ed-48de9e937a7e
feature: Tracking
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 2%

---

# 追加中 [!DNL Marketo Measure] JavaScript をに設定 [!DNL Pardot] {#adding-marketo-measure-javascript-to-pardot}

[!DNL Pardot] フォームは、フォームテンプレート内で、スクリプトをサイトに配置する以外の追加の処理を行う必要があります。 [!DNL Marketo Measure] フォームの送信を認識するために使用されます。 この処理は簡単で、 [!DNL Marketo Measure] スクリプトを [!DNL Pardot] フォームテンプレート。

## 詳細な手順 {#step-by-step-instructions}

次にログインし、 [!DNL Pardot] アカウントを使用する場合は、次の手順に従います。

1. に移動します。 **[!UICONTROL マーケティング]**.

1. 「**[!UICONTROL ランディングページ]**」をクリックします。

1. 選択 **[!UICONTROL レイアウトテンプレート]**.

   ![](assets/1-3.png)

1. 適切なレイアウトテンプレートを決定し、 **[!UICONTROL 編集]** を右にドラッグします。

   ![](assets/2-1.png)

1. をコピーして貼り付けます。 [!DNL Marketo Measure] JavaScript コードを使用して、ヘッダーページ上の close header タグの直前にHTMLを追加します。

   `<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

1. 該当するすべてのランディングページレイアウトテンプレートに対して、次の手順に従います。

1. 次を確認します。 [!DNL Marketo Measure] JavaScript も一般的なサイトページにあります。

   内 [!DNL Pardot] レイアウトテンプレートのコードは次のようになります。

```text
<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>
   </head>
   <body>
```

## そのほかの備考 {#additional-notes}

次の場合、 [!DNL Pardot] IFrame には次のHTMLタグがある。

`<base href="http://go.pardot.com">`

_および_ IFrame 自体は、 [!DNL Pardot] IFrame の場合、ブラウザーは HTTPS ページでスクリプトの HTTP バージョンを読み込もうとしますが、これが失敗し、トラッキングが機能しなくなります。 解決策は、 [!DNL Pardot] 安全なバージョンのスクリプトを読み込むためのフレーム：

`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

この領域には、例えば [!DNL Google Analytics] コード。 必ずセミコロンで区切ってください `;` 次の例のように、1 つのスペースを指定します。

`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>; <script async="true" type="othercode_example" src="otherfile_example.js" ></script>`
