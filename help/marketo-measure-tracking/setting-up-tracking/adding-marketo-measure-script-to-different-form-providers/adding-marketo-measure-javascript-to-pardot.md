---
unique-page-id: 18874757
description: ' [!DNL Marketo Measure] - [!DNL Pardot]  への  [!DNL Marketo Measure]JavaScriptの追加'
title: ' [!DNL Marketo Measure]  に  [!DNL Pardot]JavaScriptを追加しています'
exl-id: e49190ad-aa86-4f8f-a9ed-48de9e937a7e
feature: Tracking
source-git-commit: 666812e8bf095170d611cd694b5d0ac5151d8fdd
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 2%

---

# [!DNL Marketo Measure] への [!DNL Pardot] JavaScriptの追加 {#adding-marketo-measure-javascript-to-pardot}

[!DNL Pardot] forms では、フォームの送信を認識するためにサイトにスクリプトを配置するだけでなく、フォームテンプレート内で追加の処理を行う必要 [!DNL Marketo Measure] あります。 このプロセスは簡単です。[!DNL Marketo Measure] トラッキングスクリプトを [!DNL Pardot] フォームテンプレートに配置するだけで済みます。

## 詳しい手順 {#step-by-step-instructions}

[!DNL Pardot] アカウントにログインしたら、次の手順に従います。

1. **[!UICONTROL マーケティング]** に移動します。

1. 「**[!UICONTROL ランディングページ]**」をクリックします。

1. **[!UICONTROL レイアウトテンプレート]** を選択します。

   ![](assets/1-3.png)

1. 適切なレイアウトテンプレートを決定し、右側の **[!UICONTROL 編集]** をクリックします。

   ![](assets/2-1.png)

1. HTML ページの閉じるヘッダータグの直前に [!DNL Marketo Measure] JavaScript コードをコピー&amp;ペーストします。

   `<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

1. 該当するすべてのランディングページレイアウトテンプレートで、次の手順に従います。

1. [!DNL Marketo Measure] JavaScriptが一般的なサイトページにも表示されていることを確認します。

   [!DNL Pardot] レイアウトテンプレート内のコードは次のようになります。

```text
<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>
   </head>
   <body>
```

## そのほかの備考 {#additional-notes}

[!DNL Pardot] の IFrame に次のHTML タグがある場合：

`<base href="http://go.pardot.com">`

_また_ IFrame 自体は実際にはセキュアでない（HTTP）ページではなく、セキュアな（HTTPS）ページです。[!DNL Pardot] IFrame でスクリプトを読み込むと、ブラウザーは HTTPS ページにスクリプトの HTTP バージョンを読み込もうとしますが、失敗し、トラッキングが中断されます。 解決策は、[!DNL Pardot] IFrame 上のスクリプトを更新して、セキュリティで保護されたバージョンのスクリプトを読み込むことです。

`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

この領域には、[!DNL Google Analytics] コードなど、既に他のトラッキングコードスニペットが存在する場合があります。 次の例に示すように、セミコロン `;` と 1 つのスペースで区切ってください。

`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>; <script async="true" type="othercode_example" src="otherfile_example.js" ></script>`
