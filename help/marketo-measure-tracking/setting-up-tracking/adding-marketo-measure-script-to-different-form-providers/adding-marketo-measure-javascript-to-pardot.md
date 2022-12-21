---
unique-page-id: 18874757
description: 追加中 [!DNL Marketo Measure] JavaScript をに設定 [!DNL Pardot] - [!DNL Marketo Measure]  — 製品ドキュメント
title: 追加中 [!DNL Marketo Measure] JavaScript をに設定 [!DNL Pardot]
exl-id: e49190ad-aa86-4f8f-a9ed-48de9e937a7e
source-git-commit: ae5b77744d523606ce6cfcf48d7e8d5049d5ccb7
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---

# 追加中 [!DNL Marketo Measure] JavaScript をに設定 [!DNL Pardot] {#adding-marketo-measure-javascript-to-pardot}

[!DNL Pardot] フォームを使用するには、フォームテンプレート内でスクリプトを配置する以外に、 [!DNL Marketo Measure] フォームの送信を認識するため。 このプロセスは単純です。それは、 [!DNL Marketo Measure] スクリプトを [!DNL Pardot] フォームテンプレート。

## 詳細な手順 {#step-by-step-instructions}

次にログインし、 [!DNL Pardot] アカウントに追加するには、次の手順に従います。

1. に移動します。 **[!UICONTROL マーケティング]**.

1. クリック **[!UICONTROL ランディングページ]**.

1. 選択 **[!UICONTROL レイアウトテンプレート]**.

   ![](assets/1-3.png)

1. 適切なレイアウトテンプレートを決定し、 **[!UICONTROL 編集]** 右に

   ![](assets/2-1.png)

1. をコピーして貼り付けます。 [!DNL Marketo Measure] JavaScript コードを使用して、ヘッダーページ上の close header タグの直前にHTMLを追加します。

   `<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

1. 該当するすべてのランディングページレイアウトテンプレートに対して、次の手順に従います。

1. 次を確認します。 [!DNL Marketo Measure] JavaScript も一般的なサイトページにあります。

   内 [!DNL Pardot] レイアウトテンプレートの場合、コードは次のようになります。

```text
<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>
   </head>
   <body>
```

## そのほかの備考 {#additional-notes}

この [!DNL Pardot] IFrame には次のHTMLタグがある。

`<base href="http://go.pardot.com">`

_および_ IFrame 自体は、非セキュアなページ (HTTP) ではなく、セキュアなページ (HTTPS) 上にあります ( [!DNL Pardot] IFrame の場合、ブラウザーは HTTPS ページに HTTP バージョンのスクリプトを読み込もうとしますが、これは失敗し、トラッキングを妨げます。 解決策は、 [!DNL Pardot] セキュアバージョンのスクリプトを読み込むためのフレーム：

`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

また、この領域には、 [!DNL Google Analytics] コード。 必ずセミコロンで区切ってください `;` 次の例のように、1 つのスペース

`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>; <script async="true" type="othercode_example" src="otherfile_example.js" ></script>`
