---
unique-page-id: 30082018
description: 遅延 Cookie 同期 — [!DNL Marketo Measure]  — 製品ドキュメント
title: Cookie 同期の遅延
exl-id: 394053ed-5642-48e4-b83c-c483a58ebbd7
source-git-commit: ae5b77744d523606ce6cfcf48d7e8d5049d5ccb7
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# Cookie 同期の遅延 {#delayed-cookie-sync}

このデフォルトへの変更 [!DNL Marketo Measure] JavaScript は、 [!DNL bizible.js] API サポート。訪問者のユーザーアクティビティを一時的に保存するように JS を設定できますが、に情報を送信しないようにすることができます。 [!DNL Marketo Measure] サーバーに送信されます。

## ハウツー {#how-to}

デフォルトの [!DNL bizible.js] スクリプトタグに次の情報が含まれます。

`<script id="bizible-settings" type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async="" data-consent-button-id="ConsentButtonId"></script>`

data-consent-button-id=&quot;ConsentButtonId&quot;属性は、 [!DNL bizible.js] をクリックして、分析データを送信しない場合は、該当する id を持つHTML要素がクリックされるまで送信しないようにします。

または、 [!UICONTROL data-consent-button-id] を存在しない（例：「foobar」）ものにし、次の API を使用して [!DNL bizible.js] ユーザーが同意したこと：

`window['Bizible'] = window['Bizible'] || { _queue: [], Push: function (o, p) {this._queue.push({ type: o, data: p }); } };`
`Bizible.Push("Consent", true });`

>[!NOTE]
>
>ユーザーの同意は Cookie に保存されます。つまり、ユーザーが一度同意した後で、その後のページでこの呼び出しを実行する必要はありません。

## 制限事項 {#limitation}

理由： [!DNL bizible.js] では、未送信の Web アクティビティを顧客のファーストパーティ Cookie に一時的に保存し、ファーストパーティ Cookie のサイズは制限されます。一度に保存できる未送信のリクエストは 3 つだけです。

保留中のリクエストが 3 つ既にある場合、それ以降のアクティビティは無視されます。これは、最初のページビューを保持するためのものです。このページビューには、貴重なリファラー情報が含まれています。
