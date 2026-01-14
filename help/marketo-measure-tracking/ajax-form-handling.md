---
description: Marketo Measure ユーザー向けのAJAX フォーム処理ガイダンス
title: AJAX フォームハンドリング
exl-id: 042e42ff-d8d9-4380-b878-aba4934bc4a0
feature: Tracking
source-git-commit: fcd8e276c85669ddf12bd7404fb12d3e99b2642a
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 1%

---

# AJAX フォームハンドリング {#ajax-form-handling}

[!DNL Marketo Measure] への顧客コンバージョンを手動でレポートするには、使用できるシンプルな API があります。 トラッキングコードを使用している場合、これらのJavaScript API は両方ともサイトで自動的に使用可能になります。 アクセスするために特別な操作を行う必要はありません。

## シナリオ 1 - AJAX送信を含むHTML フォーム {#scenario-html-form-with-an-ajax-submit}

AJAX（または他のメカニズム）を含むフォームを使用して、クライアントから当社のサーバーにコンバージョン日を送信する場 [!DNL Marketo Measure]、当社がモニターする標準パスを通じてお客様のコンバージョンを認識できない場合があります。 このシナリオでは、（以下に示す）単純な API を使用できます。

独自のフォーム送信を処理する場合は、JavaScriptから明示的に [!DNL Marketo Measure] を呼び出すことができます。 [!DNL Marketo Measure] は、フォームからすべての関連情報を収集し、サーバーに非同期で投稿します。

**以下は、JQuery を使用したコードサンプルです（フォームの ID が「formId」である場合）。**

```javascript
///////////////////////////////////////////////////////////////////////
// Preamble for all API usage.
window['Bizible'] = window['Bizible'] || { _queue: [], Push: function (o, p) {this._queue.push({ type: o, data: p }); } };

// Give Marketo Measure the JQuery Selector for the form and we'll collect the data automatically.
Bizible.Push('Form',$('#*formId*'));
```

**以下は、JQuery を使用しないコードサンプルです（フォームの ID が「formId」である場合）。**

```javascript
///////////////////////////////////////////////////////////////////////
// Preamble for all API usage.
window['Bizible'] = window['Bizible'] || { _queue: [], Push: function (o, p) {this._queue.push({ type: o, data: p }); } };

// Give Marketo Measure the Form ID and we'll collect the data automatically.
Bizible.Push('Form','MyFormID');
```

## シナリオ 2 – 非HTML フォームで収集されたリード情報 {#scenario-lead-information-collected-in-a-non-html-form}

変換されたリードの情報を、JavaScriptまたは HTML フォームを含まないシンプルなテキストフィールドを使用して収集する場合、このソリューションは最適です。 このシナリオで使用する API を以下で共有します。

```javascript
///////////////////////////////////////////////////////////////////////
// Preamble for all API usage.
window['Bizible'] = window['Bizible'] || { _queue: [], Push: function (o, p) {this._queue.push({ type: o, data: p }); } };

// If your site is using Ajax, or you are running a secure site, it is best to send us the data directly.
Bizible.Push('User', {
eMail: 'user@gmail.com' // required
});
```

このコードでは、「[!UICONTROL  メール ]」フィールドは必須です。 [!DNL Marketo Measure] は、このデータをサーバーに非同期で投稿します。

## シナリオ 3 – ありがとうページからのユーザー情報のレポート {#scenario-report-user-information-from-the-thank-you-page}

フォームを送信した後で、ありがとうページから [!DNL Marketo Measure] にリード情報を報告する方が便利な場合があります。 この情報をレポートする最も簡単な方法は、フォーム送信からの情報を保持するページに非表示の要素を追加 [!DNL Bizible.js] ることで、「ありがとうございました」ページが読み込まれたときに、この情報を読み取ります。

**例：**

```html
<div id="bizible.reportUser" style="display:none"
data-email="user@gmail.com">
```

非表示の要素が div、script またはその他のタグタイプであるかどうかは関係ありません。 [!DNL Marketo Measure] は id=&quot;bizible.reportUser&quot;を探し、情報を読み取ります。
