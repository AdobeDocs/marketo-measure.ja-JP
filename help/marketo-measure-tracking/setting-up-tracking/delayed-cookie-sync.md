---
unique-page-id: 30082018
description: Cookie 同期の遅延 — [!DNL Marketo Measure]  — 製品ドキュメント
title: Cookie の同期の遅延
exl-id: 394053ed-5642-48e4-b83c-c483a58ebbd7
feature: Tracking
source-git-commit: 8ac315e7c4110d14811e77ef0586bd663ea1f8ab
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 3%

---

# Cookie の同期の遅延 {#delayed-cookie-sync}

このデフォルトへの変更 [!DNL Marketo Measure] JavaScript は、 [!DNL bizible.js] API サポート。訪問者のユーザーアクティビティを一時的に保存するように JS を設定できますが、に情報を送信しないようにすることができます。 [!DNL Marketo Measure] サーバーに送信されます。

## ハウツー {#how-to}

デフォルトの [!DNL bizible.js] script タグに次の情報が含まれます。

`<script id="bizible-settings" type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async="" data-consent-button-id="ConsentButtonId"></script>`

data-consent-button-id=&quot;ConsentButtonId&quot;属性は、に示します。 [!DNL bizible.js] をクリックして、分析データを送信しない場合は、該当する id を持つHTML要素がクリックされるまで送信しないようにします。

または、ユーザーが [!UICONTROL data-consent-button-id] を存在しないもの（例：「foobar」）にし、次の API を使用して [!DNL bizible.js] ユーザーが同意したこと：

`window['Bizible'] = window['Bizible'] || { _queue: [], Push: function (o, p) {this._queue.push({ type: o, data: p }); } };`
`Bizible.Push("Consent", true });`

>[!NOTE]
>
>ユーザーの同意は Cookie に保存されます。つまり、ユーザーが一度同意した後で、その後のページでこの呼び出しを実行する必要はありません。

## 制限事項 {#limitation}

理由： [!DNL bizible.js] では、未送信の Web アクティビティを顧客のファーストパーティ Cookie に一時的に保存し、ファーストパーティ Cookie のサイズは制限されます。一度に保存できる未送信のリクエストは 3 つだけです。

保留中のリクエストが 3 つ既にある場合、それ以降のアクティビティは無視されます。これは、重要なリファラー情報を含む最初のページビューを保持するためです。
