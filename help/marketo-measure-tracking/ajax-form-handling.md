---
description: Marketo Measure ユーザー向けAJAX フォーム処理ガイダンス
title: AJAX フォームハンドリング
exl-id: 042e42ff-d8d9-4380-b878-aba4934bc4a0
feature: Tracking
source-git-commit: 7a4661c8d42214d32e5360dc45d6d880b08ef37c
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 1%

---

# AJAX フォームハンドリング {#ajax-form-handling}

顧客のコンバージョンを[!DNL Marketo Measure]に手動で報告するには、使用できるシンプルなAPIがあります。 トラッキングコードがある場合、これらのJavaScript APIは両方とも、サイトで自動的に利用できます。 特別なアクセスは必要ありません。

## シナリオ 1 - AJAX送信を含むHTML フォーム {#scenario-html-form-with-an-ajax-submit}

AJAXを含むフォームを使用して、クライアントから当社のサーバーにコンバージョン日を送信する場合、[!DNL Marketo Measure]は、当社が監視する標準パスを通じてお客様のコンバージョンを認識できない場合があります。 このシナリオでは、シンプルなAPIを使用できます（以下を参照）。

独自のフォーム送信を処理する場合は、JavaScriptから[!DNL Marketo Measure]を明示的に呼び出すことができます。 [!DNL Marketo Measure]は、フォームからすべての関連情報を収集し、サーバーに非同期で投稿します。

**以下は、JQueryを使用したコードサンプルです（フォームのIDが「formId」であると仮定）。**

```javascript
///////////////////////////////////////////////////////////////////////
// Preamble for all API usage.
window['Bizible'] = window['Bizible'] || { _queue: [], Push: function (o, p) {this._queue.push({ type: o, data: p }); } };

// Give Marketo Measure the JQuery Selector for the form and we'll collect the data automatically.
Bizible.Push('Form',$('#*formId*'));
```

**以下は、JQueryを使用していないコードサンプルです（フォームのIDが「formId」であると仮定）。**

```javascript
///////////////////////////////////////////////////////////////////////
// Preamble for all API usage.
window['Bizible'] = window['Bizible'] || { _queue: [], Push: function (o, p) {this._queue.push({ type: o, data: p }); } };

// Give Marketo Measure the Form ID and we'll collect the data automatically.
Bizible.Push('Form','MyFormID');
```

## シナリオ 2 - HTML以外のフォームで収集されたリード情報 {#scenario-lead-information-collected-in-a-non-html-form}

コンバージョンしたリードの情報が、JavaScriptやhtml フォームのないシンプルなテキストフィールドを使用して収集される場合、このソリューションは有効です。 以下の共有は、このシナリオで使用するAPIです。

```javascript
///////////////////////////////////////////////////////////////////////
// Preamble for all API usage.
window['Bizible'] = window['Bizible'] || { _queue: [], Push: function (o, p) {this._queue.push({ type: o, data: p }); } };

// If your site is using Ajax, or you are running a secure site, it is best to send us the data directly.
Bizible.Push('User', {
eMail: 'user@gmail.com' // required
});
```

このコードでは、[!UICONTROL email] フィールドが必須です。 [!DNL Marketo Measure]は、このデータをサーバーに非同期で投稿します。

## シナリオ 3 – 感謝ページからユーザー情報を報告する {#scenario-report-user-information-from-the-thank-you-page}

場合によっては、フォームが送信された後で、お礼のページから[!DNL Marketo Measure]にリード情報を報告する方が便利です。 この情報を報告する最も簡単な方法は、フォーム送信の情報を保持するページに非表示の要素を追加することです。この情報は、「ありがとうございます」ページが読み込まれたときに[!DNL Bizible.js]によって読み取られます。

**例：**

```html
<div id="bizible.reportUser" style="display:none"
data-email="user@gmail.com">
```

非表示の要素がdiv、スクリプト、またはその他のタグタイプのいずれであっても問題ありません。 [!DNL Marketo Measure]は、情報を読み取るためにid=&quot;bizible.reportUser&quot;を探します。
