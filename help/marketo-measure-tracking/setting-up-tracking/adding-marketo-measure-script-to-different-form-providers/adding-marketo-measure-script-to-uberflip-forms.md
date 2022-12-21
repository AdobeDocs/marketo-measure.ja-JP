---
unique-page-id: 18874749
description: 追加中 [!DNL Marketo Measure] スクリプト [!DNL Uberflip] Forms - [!DNL Marketo Measure]  — 製品ドキュメント
title: 追加中 [!DNL Marketo Measure] スクリプト [!DNL Uberflip] Forms
exl-id: fb123e15-523d-4931-b4c1-705fe49be3d0
source-git-commit: b59c79236d3e324e8c8b07c5a6d68bd8176fc8a9
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# 追加中 [!DNL Marketo Measure] スクリプト [!DNL Uberflip] Forms {#adding-marketo-measure-script-to-uberflip-forms}

現在 [!DNL Uberflip] コンテンツを管理するには、次の必要な手順を実行して、 [!DNL Marketo Measure] は、これらのフォーム送信を追跡しています。 サクセスマネージャー： [!DNL Uberflip] これに関しては、もう一度お手伝いをいただけるはずです。

1. このスクリプトの追加先 [!DNL Uberflip]&#39;s [!UICONTROL カスタムコード/HTML] 」セクションに入力します。

   `<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

1. これを確認します [!DNL Marketo Measure] プリアンブルコードは、ページ読み込みとAJAXページ変更の両方で実行されます。 これを [!UICONTROL カスタムコード >JS] セクション

   `window['Bizible'] = window['Bizible'] || { _queue: [], Push: function (o, p) {this._queue.push({ type: o, data: p }); } };`

   このプリアンブルは、 [!DNL Hubs.onLoad] そして [!DNL Hubs.onPageChange] 以下に示すAJAX JavaScript イベントフックを使用します。 ( 注意：これらのイベントフックには他のコードも含まれている場合があります。 必ずプリアンブルも含めてください )。

   `Hubs.onLoad = function () {`

   `window['Bizible'] = window['Bizible'] || { _queue: [], Push: function (o, p) {this._queue.push({ type: o, data: p }); } };`

   `}`

   `Hubs.onPageChange = function () {`

   `window['Bizible'] = window['Bizible'] || { _queue: [], Push: function (o, p) {this._queue.push({ type: o, data: p }); } };`

   `}`

1. フォーム CTA の送信時に Bizible にデータをプッシュする関数を作成し定義します。 これは、 [!UICONTROL カスタムコード >JavaScript] 」セクションに入力します。 ( 注意：この関数は、ctaData パラメーター Uberflip が提供するだけですが、ユーザーがコードをカスタマイズしてこのデータを渡す場合に備えて、他のパラメーター ctaId および ctaName を含めることができます )。

   `function bizibleFormCode(ctaId, ctaData, ctaName) {`
   `var email = ctaData["email"];`
   `if(email){`
   `Bizible.Push('User', {`
   `eMail: email, // required`
   `}); }`

   `}`

1. フォーム CTA が送信されたら、 [!DNL Marketo Measure] 関数は、以下の単位で実行されます。 これは、 [!UICONTROL カスタムコード >JS] 」セクションに入力します。 ( 注意：Hubs.onCtaFormSubmitSuccess JavaScript イベントフック内に他のコードがある場合もありますが、この関数呼び出しも必ず含めてください )。

   `Hubs.onCtaFormSubmitSuccess = function (ctaId, ctaData, ctaName) {`
   `bizibleFormCode(ctaId, ctaData, ctaName);`\
   `}`
