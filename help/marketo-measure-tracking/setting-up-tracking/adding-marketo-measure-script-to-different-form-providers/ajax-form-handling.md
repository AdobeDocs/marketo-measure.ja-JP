---
unique-page-id: 18874745
description: AJAX Form Handling - [!DNL Marketo Measure]  — 製品ドキュメント
title: AJAX フォームハンドリング
exl-id: 042e42ff-d8d9-4380-b878-aba4934bc4a0
feature: Tracking
source-git-commit: 8ac315e7c4110d14811e77ef0586bd663ea1f8ab
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 2%

---

# AJAX フォームハンドリング {#ajax-form-handling}

顧客のコンバージョンをに手動でレポートするには [!DNL Marketo Measure]を使用するには、非常にシンプルな API を提供しています。 追跡コードがある場合、これらの両方の JavaScript API がサイトで自動的に使用可能になります。 アクセスするために特別な操作は必要ありません。

## シナリオ 1 - AJAX送信を含むHTMLフォーム {#scenario-html-form-with-an-ajax-submit}

AJAX（またはその他のメカニズム）を含むフォームを使用して、変換日をクライアントからアドビのサーバーに送信する場合は、 [!DNL Marketo Measure] は、監視する標準パスを通じての顧客コンバージョンを認識していない可能性があります。 このシナリオでは、シンプルな API（以下で提供）を活用できます。

独自のフォーム送信を処理する場合は、 [!DNL Marketo Measure] を JavaScript から取得します。 [!DNL Marketo Measure] は、フォームからすべての関連情報を収集し、アドビのサーバーに非同期で投稿します。

**JQuery を使用するコードサンプルを以下に示します（フォームの ID が「formId」の場合）。**

```jquery
///////////////////////////////////////////////////////////////////////  
// Preamble for all API usage.  
window['Bizible'] = window['Bizible'] || { _queue: [], Push: function (o, p) {this._queue.push({ type: o, data: p }); } };  
  
// Give Marketo Measure the JQuery Selector for the form and we'll collect the data automatically.  
Bizible.Push('Form',$('#*formId*'));
```

**JQuery を使用しないコード例を次に示します（フォームの ID が「formId」の場合）。**

```jquery
///////////////////////////////////////////////////////////////////////  
// Preamble for all API usage.  
window['Bizible'] = window['Bizible'] || { _queue: [], Push: function (o, p) {this._queue.push({ type: o, data: p }); } };  
  
// Give Marketo Measure the Form ID and we'll collect the data automatically.
Bizible.Push('Form','MyFormID');
```

## シナリオ 2 — 非HTML形式で収集されたリード情報 {#scenario-lead-information-collected-in-a-non-html-form}

変換後のリードからの情報が、HTML フォームのない JavaScript または単純なテキストフィールドを使用して収集される場合、このソリューションは機能します。 以下に、このシナリオで使用する API を示します。

```jquery
///////////////////////////////////////////////////////////////////////  
// Preamble for all API usage.  
window['Bizible'] = window['Bizible'] || { _queue: [], Push: function (o, p) {this._queue.push({ type: o, data: p }); } };  
  
// If your site is using Ajax, or you are running a secure site, it is best to send us the data directly.  
Bizible.Push('User', {
eMail: 'user@gmail.com' // required  
});  
```

このコードでは、 [!UICONTROL 電子メール] フィールドは必須です。 [!DNL Marketo Measure] は、このデータをアドビのサーバーと非同期で投稿します。

## シナリオ 3 - 「ありがとうございます」ページからのユーザー情報のレポート {#scenario-report-user-information-from-the-thank-you-page}

場合によっては、リード情報をに報告する方が便利です。 [!DNL Marketo Measure] 「ありがとうございます」ページから、フォームの送信後に選択します。 この情報をレポートする最も簡単な方法は、フォーム送信からの情報を保持するページに非表示要素を追加し、 [!DNL Bizible.js] は、「ありがとうございます」ページが読み込まれた際に、この情報を読み取ります。

**例：**

```html
<div id="bizible.reportUser" style="display:none"  
data-email="user@gmail.com">  
```

非表示の要素が div、script、またはその他のタグタイプであるかどうかは関係ありません。 [!DNL Marketo Measure] は、情報を読み取るために id=&quot;bizible.reportUser&quot;を探します。
