---
unique-page-id: 18874648
description: Google Analytics コンバージョンとBuyer Touchpointの違い  [!DNL Marketo Measure]
title: Google Analytics コンバージョンと Buyer Touchpoint の違い
exl-id: d09d963c-3207-467c-852a-d1edd49511fa
feature: Touchpoints
source-git-commit: 4787f765348da71bc149c997470ce678ba498772
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 5%

---

# Google Analytics コンバージョンと Buyer Touchpoint の違い {#difference-between-a-google-analytics-conversion-and-a-buyer-touchpoint}

[!DNL Google Analytics (GA)] の目標の概要と、Buyer Touchpointとの違いについて説明します。

**Google Analyticsのコンバージョンとは**

[!UICONTROL Google Analytics] コンバージョンは、マーケターまたは web デベロッパーが特定の web サイト上で「目標」の完了をコード化する方法によって決定されます。 Googleによれば、目標は「購入する（e コマースサイトの場合）、ゲームレベルを達成する（モバイルゲームアプリの場合）、または連絡先情報フォームを送信する（マーケティングまたはリードジェネレーションサイトの場合）」と考えることができます。 ほとんどの場合、マーケターは、目標/コンバージョンを情報フォームに入力するユーザーと見なします。

ただし、特定の動作を管理するように目標をコーディングすることはできません。 代わりに、web 開発者が設定できる目標タイプがあります。 以下に、その例の一部を示します。

<table> 
 <colgroup> 
  <col> 
  <col> 
  <col> 
 </colgroup> 
 <tbody> 
  <tr> 
   <td><strong>目標タイプ</strong></td> 
   <td><p><strong>説明</strong></p></td> 
   <td><strong>例</strong></td> 
  </tr> 
  <tr> 
   <td><p>作成先</p></td> 
   <td>特定の場所の読み込み</td> 
   <td><em> ご登録いただきありがとうございます。</em> web ページまたはアプリの画面</td> 
  </tr> 
  <tr> 
   <td>期間</td> 
   <td>一定時間以上続くセッション</td> 
   <td>10 分以上の時間をサポートサイトに費やす</td> 
  </tr> 
  <tr> 
   <td>セッションあたりのページ/Screens数</td> 
   <td>ユーザーが特定の数のページまたは画面を表示した場合</td> 
   <td>5 ページまたはスクリーンが読み込まれました</td> 
  </tr> 
  <tr> 
   <td>イベント</td> 
   <td>イベントとして定義されたアクションがトリガーされる</td> 
   <td>ソーシャルレコメンデーション、ビデオ再生、クリック</td> 
  </tr> 
 </tbody> 
</table>

ほとんどのマーケターは、コンバージョンを「宛先目標」として設定します。つまり、通常、フォームの後に「ありがとうございます」ページを作成して、正式なコンバージョンと見なします。

つまり、Googleでは「ありがとうございます」ページビューをコンバージョンと見なします。 Google Analyticsの観点から見ると、これは大部分のマーケターにとって問題のない認識です。

ただし、購入者タッチポイントの動作は異なります。

**買い手タッチポイントの違い**

JavaScript[!DNL Marketo Measure]、特定のサイトのすべてのフォーム上のセッションデータとフォーム送信を追跡します。 [!DNL Marketo Measure] の観点から目標をコーディングする必要はありません。 この処理は自動的に行われます。 フォーム送信の場合、[!DNL Marketo Measure] は、匿名ユーザーが特定のフォームの情報フィールドに入力し、フォーム送信ボタンをクリックするたびにフォームの完了をレポートします。 フォームの送信を記録するために、「ありがとうございます」ページは必要ありませ [!DNL Marketo Measure]。

[!DNL Marketo Measure] は、次の場合にフォームタッチポイントを作成します。

* これらのコンバージョンに関連付けられているリード/連絡先が CRM に表示されます。
* [!DNL Marketo Measure] JS は、フォームを含む web ページに存在します。
* フォームは、30 分のセッション内で送信されます。

[!DNL Marketo Measure] は、次の場合に Destination Google Analytic 変換を無視します。

* ボットが web サイト上のフォームを送信します（これらのボットは通常、フォームをクライアントの CRM に送信しません）。
* ユーザーが最初のフォーム送信後にフォームを送信する。 [!DNL Marketo Measure] は、そのセッションからの最初のコンバージョンのみをプッシュします。
* ユーザーがフォーム送信を複数回クリックします。 [!DNL Marketo Measure] は、最初のフォーム送信のみを考慮します。
* このユーザーは、ありがとうページを複数回リロードします。
* ユーザーは任意の広告ブロックツールを使用しています。

ご覧のように、GA と [!DNL Marketo Measure] がコンバージョンであると見なすものの間には基本的な違いがあります。 したがって、コンバージョン数とフォームタッチポイント数は異なる可能性があります。
