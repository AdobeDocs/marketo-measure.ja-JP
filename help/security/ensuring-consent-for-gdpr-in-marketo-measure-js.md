---
description: Marketo Measure JS での GDPR への同意の確認
title: Marketo Measure JS での GDPR への同意の確認
exl-id: 9afc5e4d-cf97-4c49-b9ee-ee1cc99c1f90
feature: Tracking
source-git-commit: c6090ce0c3ac60cd68b1057c369ce0b3b20aeeee
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 100%

---


# Marketo Measure JS での GDPR への同意の確認 {#ensuring-consent-for-gdpr-in-marketo-measure-js}

EU 一般データ保護規則（GDPR）は、2018年5月25日に施行された欧州連合の法律です。

## 概要 {#overview}

GDPR の目的は、EU（欧州連合）と EEA（欧州経済圏）内のデータ主体の個人データの使用と保護の方法に関する権利を強化することです。「個人データ」とは、識別された、または識別可能な自然人に関する情報を指します。GDPR は、EU 内または EEA 外で、EU 内のデータ主体に対するマーケティング商品やサービスを行っている、または EU 内のデータ主体の行動を追跡している組織に適用されます。ヨーロッパで個人データの処理を伴うデータ主体と取引を行う場合、この法律が適用されます。規制違反者に対する大規模な罰金を科し、コンプライアンス違反に対する罰則は重要です。1 回の違反に対する最大罰金は、2,000 万ユーロまたは世界的年間売上高の 4%のいずれか大きい方です。

デフォルトでは、同意を待つように設定されていない限り、[!DNL bizible.js] はユーザの分析データを収集します。[!DNL bizible.js] がユーザの同意を待つように設定されている場合、同意に達するまで Cookie は作成されず、分析データも送信されません。

## 同意を待つ方法 {#how-to-wait-for-consent}

[!DNL bizible.js] を設定して同意を待つ方法は 2 つあります。

オプション 1 - デフォルトの [!DNL bizible.js] スクリプトタグを次のように置き換えます。

`<script id="bizible-settings" type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async="" data-consent-button-id="ConsentButtonId"></script>`

**[!DNL Google Tag Manager] を使用してスクリプトをインストールする場合は**、GTM がデータ属性を削除します。そのため、代わりに次のスクリプトを使用します。

```html
<span id="bizible-settings" data-consent-button-id="ConsentButtonId"></span>
<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async></script>
```

>[!NOTE]
>この場合、[!DNL bizible.js] は、ID「ConsentButtonId」を持つ HTML 要素にオンクリックイベントを添付します。

この HTML 要素をクリックすると、[!DNL bizible.js] は Cookie を作成してユーザーの同意が得られたことを記憶し、通常どおり分析データの収集を開始します。

**または**

オプション 2 - デフォルトの [!DNL bizible.js] スクリプトタグを次のように置き換えます。

`<script id="bizible-settings" type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async="" data-requires-user-consent="true"></script>`

同意に達するまで追跡しないように [!DNL bizible.js] に指示します。これは、次の JS API を使用して実行できます。

*window[&#39;Bizible&#39;] = window[&#39;Bizible&#39;] || { _queue: [], Push: function (o, p) { this._queue.push({ type: o, data: p }); } };*

*Bizible.Push(&#39;Consent&#39;, true);*

**[!DNL Google Tag Manager] を使用してスクリプトをインストールする場合は**、GTM がデータ属性を削除します。そのため、代わりに次のスクリプトを使用します。

```html
<span id="bizible-settings" data-requires-user-consent="true"></span>
<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async></script>
```

>[!NOTE]
>bizible.js は、ユーザの同意が得られたことを記憶するために Cookie を作成し、JS API が呼び出された後にのみ通常どおり分析データの収集を開始します。

一方、お客様は、この API を使用してユーザーの同意を取り消すこともできます。

`window['Bizible'] = window['Bizible'] || { _queue: [], Push: function (o, p) { this._queue.push({ type: o, data: p }); } };`

`Bizible.Push('Consent', false);`

このコードを実行すると、[!DNL bizible.js] が以前に作成したすべての Cookie が削除され、ユーザが再同意した場合にのみ分析データの収集が再開されます。
