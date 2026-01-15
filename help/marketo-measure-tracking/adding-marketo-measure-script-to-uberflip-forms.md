---
description: Marketo Measure ユーザー向けの  [!DNL Marketo Measure] Forms ガイダンスへの  [!DNL Uberflip]  スクリプトの追加
title: ' [!DNL Marketo Measure] Formsへの  [!DNL Uberflip]  スクリプトの追加'
exl-id: fb123e15-523d-4931-b4c1-705fe49be3d0
feature: Tracking
source-git-commit: 0299ef68139df574bd1571a749baf1380a84319b
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Formsへ [!DNL Marketo Measure] スクリプト [!DNL Uberflip] 追加 {#adding-marketo-measure-script-to-uberflip-forms}

現在 [!DNL Uberflip] を使用してコンテンツを管理している場合は、これらの必要な手順を実行して、[!DNL Marketo Measure] がこれらのフォーム送信を追跡していることを確認することが重要です。 [!DNL Uberflip] のサクセスマネージャーも、これを支援できます。

1. このスクリプトを [!DNL Uberflip] の [!UICONTROL &#x200B; カスタムコード >HTML] セクションに追加します。

   `<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

1. この [!DNL Marketo Measure] プリアンブルコードが、ページの読み込み時とAJAX ページの変更時の両方で実行されるようにします。 [!UICONTROL &#x200B; カスタムコード/JS] セクション内でこれを実行します。

   `window['Bizible'] = window['Bizible'] || { _queue: [], Push: function (o, p) {this._queue.push({ type: o, data: p }); } };`

   以下に従って、このプリアンブルを [!DNL Hubs.onLoad] と [!DNL Hubs.onPageChange] AJAX JavaScript イベントフックの両方に追加します。 （メモ：これらのイベントフックには、他のコードも含めることができます。 必ずプリアンブルも含めてください）。

   `Hubs.onLoad = function () {`

   `window['Bizible'] = window['Bizible'] || { _queue: [], Push: function (o, p) {this._queue.push({ type: o, data: p }); } };`

   `}`

   `Hubs.onPageChange = function () {`

   `window['Bizible'] = window['Bizible'] || { _queue: [], Push: function (o, p) {this._queue.push({ type: o, data: p }); } };`

   `}`

1. フォームCTAの送信時に Bizible にデータをプッシュする関数を作成し定義します。 これは、「カスタムコード [!UICONTROL JavaScript] セクションに移動します。 （メモ：この関数は、Uberflip が提供する ctaData パラメーターのみを必要としますが、ユーザーがこのデータを渡すためにコードをカスタマイズする場合に備えて、他のパラメーター ctaId および ctaName を含めることもできます）。

   `function bizibleFormCode(ctaId, ctaData, ctaName) {`
   `var email = ctaData["email"];`
   `if(email){`
   `Bizible.Push('User', {`
   `eMail: email, // required`
   `}); }`

   `}`

1. フォームCTAが送信されたら、[!DNL Marketo Measure] 関数が以下ごとに実行されていることを確認します。 これは、[!UICONTROL &#x200B; カスタムコード/JS] セクション内で行われます。 （メモ：Hubs.onCtaFormSubmitSuccess JavaScript イベントフック内に他のコードがある場合は、この関数呼び出しも含めてください）。

   `Hubs.onCtaFormSubmitSuccess = function (ctaId, ctaData, ctaName) {`
   `bizibleFormCode(ctaId, ctaData, ctaName);`\
   `}`
