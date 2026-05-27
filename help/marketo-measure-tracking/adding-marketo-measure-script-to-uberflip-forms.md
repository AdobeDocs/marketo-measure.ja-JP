---
description: Marketo Measure ユーザー向けの [!DNL Uberflip] Forms ガイダンスに [!DNL Marketo Measure]  スクリプトを追加する
title: 'Formsに [!DNL Marketo Measure]  スクリプトを追加しています [!DNL Uberflip] '
exl-id: fb123e15-523d-4931-b4c1-705fe49be3d0
feature: Tracking
source-git-commit: 7a4661c8d42214d32e5360dc45d6d880b08ef37c
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# [!DNL Marketo Measure] スクリプトを[!DNL Uberflip] Formsに追加しています {#adding-marketo-measure-script-to-uberflip-forms}

現在[!DNL Uberflip]を使用してコンテンツを管理している場合は、次の必要な手順を実行して、[!DNL Marketo Measure]がフォーム送信を追跡していることを確認することが重要です。 [!DNL Uberflip]のサクセスマネージャーも、これを支援できる必要があります。

1. このスクリプトを[!DNL Uberflip]の[!UICONTROL &#x200B; カスタムコード >HTML] セクションに追加します。

   `<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

1. この[!DNL Marketo Measure] プリアンブルコードがページ読み込み時とAJAX ページの変更時の両方で実行されることを確認します。 これは、[!UICONTROL &#x200B; カスタムコード >JS] セクション内で行います

   `window['Bizible'] = window['Bizible'] || { _queue: [], Push: function (o, p) {this._queue.push({ type: o, data: p }); } };`

   このプリアンブルを以下の[!DNL Hubs.onLoad]と[!DNL Hubs.onPageChange]のAJAX JavaScript イベントフックの両方に追加します。 （注意：これらのイベントフックには他のコードも含まれる場合があります。 プリアンブルも必ず含めてください）。

   `Hubs.onLoad = function () {`

   `window['Bizible'] = window['Bizible'] || { _queue: [], Push: function (o, p) {this._queue.push({ type: o, data: p }); } };`

   `}`

   `Hubs.onPageChange = function () {`

   `window['Bizible'] = window['Bizible'] || { _queue: [], Push: function (o, p) {this._queue.push({ type: o, data: p }); } };`

   `}`

1. Form CTAの送信時にBizibleにデータをプッシュする関数を作成して定義します。 これは、[!UICONTROL &#x200B; カスタムコード >JavaScript] セクションに入ります。 （注意：この関数は、Uberflipが提供するctaData パラメーターのみを必要としますが、ユーザーがこのデータを渡すためにコードをカスタマイズしたい場合に備えて、他のパラメーターctaIdとctaNameを含めることができます）。

   `function bizibleFormCode(ctaId, ctaData, ctaName) {`
   `var email = ctaData["email"];`
   `if(email){`
   `Bizible.Push('User', {`
   `eMail: email, // required`
   `}); }`

   `}`

1. フォーム CTAを送信する際は、以下に示す[!DNL Marketo Measure]関数が実行されていることを確認してください。 これは、[!UICONTROL &#x200B; カスタムコード >JS] セクション内で行われます。 （注意：Hubs.onCtaFormSubmitSuccess JavaScript イベントフック内に他のコードがある場合があります。この関数呼び出しを含めるようにしてください）。

   `Hubs.onCtaFormSubmitSuccess = function (ctaId, ctaData, ctaName) {`
   `bizibleFormCode(ctaId, ctaData, ctaName);`\
   `}`
