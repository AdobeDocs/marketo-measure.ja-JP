---
unique-page-id: 35586069
description: Marketo Measure Js での GDPR に対する同意の確保 — Marketo Measure — 製品ドキュメント
title: Marketo Measure Js での GDPR に対する同意の確保
exl-id: 9afc5e4d-cf97-4c49-b9ee-ee1cc99c1f90
source-git-commit: c7d3bbce1f0c6a99409822c06c43961c93cd9458
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 20%

---

# Marketo Measure Js での GDPR に対する同意の確保 {#ensuring-consent-for-gdpr-in-marketo-measure-js}

EU 一般データ保護規則 (GDPR) は、2018 年 5 月 25 日に施行された欧州連合の法律です。

## 概要 {#overview}

GDPR の目的は、個人データの使用および保護に関して、EU（欧州連合）および EEA（欧州経済圏）内のデータ主体の権利を強化することです。 「個人データ」とは、識別された自然人や識別可能な自然人に関する情報を指します。 GDPR は、EU 内または EEA 外で、EU 内のデータ主体に対するマーケティング商品やサービスを行っている、または EU 内のデータ主体の行動を追跡している組織に適用されます。ヨーロッパで個人データの処理を伴うデータ主体と取引を行う場合、この法律が適用されます。規制違反者に対する大規模な罰金を科し、コンプライアンス違反に対する罰則は重要です。1 回の違反に対する最大罰金は、2,000 万ユーロまたは世界的年間売上高の 4%のいずれか大きい方です。

デフォルトでは、 [!DNL bizible.js] は、同意を待つように特に設定されていない限り、ユーザーの分析データを収集します。 条件 [!DNL bizible.js] は、ユーザーの同意を待つように設定されています。同意が得られるまで cookie を作成したり、analytics データを送信したりしません。

## 同意を待つ方法 {#how-to-wait-for-consent}

次の 2 つの方法で [!DNL bizible.js] 同意を待つ

オプション 1 — デフォルトを置き換える [!DNL bizible.js] 次のスクリプトタグ：

`<script id="bizible-settings" type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async="" data-consent-button-id="ConsentButtonId"></script>`

**次を使用する場合、 [!DNL Google Tag Manager] スクリプトをインストール**&#x200B;を削除する場合は、GTM によって data-attribute が削除されることに注意してください。そのため、代わりに次のスクリプトを使用します。

`<span id="bizible-settings" data-consent-button-id="ConsentButtonId"></span>`
`<script type="text/javascript" src=https://cdn.bizible.com/scripts/bizible.js async=""></script>`

>[!NOTE]
>
>この場合、 [!DNL bizible.js] は、id が「ConsentButtonId」のHTML要素にオンクリックイベントを添付します。

このHTML要素がクリックされると、 [!DNL bizible.js] は、ユーザーの同意を受け取ったことを覚えておき、通常どおり analytics データの収集を開始するための cookie を作成します。

**- または -**

オプション 2 — デフォルトを置き換える [!DNL bizible.js] 次のスクリプトタグ：

`<script id="bizible-settings" type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async="" data-requires-user-consent="true"></script>`

これは [!DNL bizible.js] ：同意に達するまで追跡しません。これは、次の JS API を使用しておこなうことができます。

*window[&#39;Bizible&#39;] =窓[&#39;Bizible&#39;] || { _queue: []、プッシュ：function (o, p) { this._queue.push({ type:o、データ：p });} };*

*Bizible.Push(&#39;Consent&#39;, true);*

**次を使用する場合、 [!DNL Google Tag Manager] スクリプトをインストール**&#x200B;を削除する場合は、GTM によって data-attribute が削除されることに注意してください。そのため、代わりに次のスクリプトを使用します。

`<span id="bizible-settings" data-requires-user-consent="true"></span>`
`<script type="text/javascript" src=https://cdn.bizible.com/scripts/bizible.js async=""></script>`

>[!NOTE]
>
>bizible.js は、JS API が呼び出された後でのみ、ユーザーの同意を受け取り、通常どおり分析データの収集を開始したことを覚えておくために、cookie を作成します。

一方、お客様は、この API を使用してユーザーの同意を取り消すこともできます。

`window['Bizible'] = window['Bizible'] || { _queue: [], Push: function (o, p) { this._queue.push({ type: o, data: p }); } };`

`Bizible.Push('Consent', false);`

このコードを実行すると、 [!DNL bizible.js] 以前に作成され、ユーザーが再同意した場合にのみ analytics データの収集を再開します。
