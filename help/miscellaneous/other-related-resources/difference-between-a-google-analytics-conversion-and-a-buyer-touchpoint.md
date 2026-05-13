---
unique-page-id: 18874648
description: Google Analytics コンバージョンとBuyer Touchpointの違い –  [!DNL Marketo Measure]
title: Google Analytics コンバージョンと Buyer Touchpoint の違い
exl-id: d09d963c-3207-467c-852a-d1edd49511fa
feature: Touchpoints
TQID: https://experienceleague.adobe.com/lgrksIiybtRf6YujoQci-RffEe5-wiEdX2BI71RaBYg
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 496
ht-degree: 5%

---

# Google Analytics コンバージョンと Buyer Touchpoint の違い {#difference-between-a-google-analytics-conversion-and-a-buyer-touchpoint}

[!DNL Google Analytics (GA)]目標とは何か、およびBuyer Touchpointとの違いについて説明します。

**Google Analyticsのコンバージョンは何ですか？**

[!UICONTROL Google Analytics]のコンバージョン率は、特定のweb サイトでのマーケターまたはweb デベロッパーによる「目標」の記述方法によって決まります。 Googleによると、目標は、「購入する（コマースサイトの場合）、ゲームレベルを完了する（モバイルゲームアプリの場合）、連絡先情報フォームを送信する（マーケティングまたはリードジェネレーションサイトの場合）」と考えることができます。 多くのマーケターは、目標やコンバージョンを、情報フォームに情報を入力する担当者として捉えています。

しかし、特定の行動を管理するために目標を設定することはできません。 web開発者が設定できる目標タイプがあります。 その例をいくつか紹介します。

<table> 
 <colgroup> 
  <col> 
  <col> 
  <col> 
 </colgroup> 
 <tbody> 
  <tr> 
   <td><strong>目標の種類</strong></td> 
   <td><p><strong>説明</strong></p></td> 
   <td><strong>例</strong></td> 
  </tr> 
  <tr> 
   <td><p>宛先</p></td> 
   <td>特定の場所の読み込み</td> 
   <td><em>ご登録ありがとうございます！</em> web ページまたはアプリ画面</td> 
  </tr> 
  <tr> 
   <td>期間</td> 
   <td>特定の時間以上続くセッション</td> 
   <td>サポートサイトで10分以上</td> 
  </tr> 
  <tr> 
   <td>Pages/Screens/per session</td> 
   <td>ユーザーが特定の数のページまたはスクリーンを閲覧</td> 
   <td>5 ページまたは画面が読み込まれました</td> 
  </tr> 
  <tr> 
   <td>イベント</td> 
   <td>イベントとして定義されたアクションがトリガーされます</td> 
   <td>ソーシャルレコメンデーション、動画の再生、クリック</td> 
  </tr> 
 </tbody> 
</table>

多くのマーケターは、コンバージョンを「配信先の目標」として設定します。つまり、通常、フォームの後に「ありがとう」ページを作成し、正式なコンバージョンを検討します。

つまり、Googleでは「ありがとうございます」ページビューをコンバージョンと見なします。 Google Analyticsを利用すれば、多くのマーケターはこの点に気づきます。

ただし、バイヤータッチポイントの行動は異なります。

**購入者のタッチポイントの違い**

[!DNL Marketo Measure] JavaScriptは、特定のサイトのすべてのフォームに関するセッション データとフォーム送信を追跡します。 [!DNL Marketo Measure]の観点から目標をコーディングする必要はありません。 このプロセスは自動です。 フォーム送信の場合、[!DNL Marketo Measure]は、匿名ユーザーが特定のフォームの情報フィールドに入力するたびにフォームの完了状況を報告し、フォーム送信ボタンもクリックします。 [!DNL Marketo Measure]様は、フォーム送信を記録するためにサンキューページを必要としません。

[!DNL Marketo Measure]は、次の場合にフォーム タッチポイントを作成します。

* これらのコンバージョンに関連付けられたリード/コンタクトがCRMに表示されます。
* [!DNL Marketo Measure] JSは、フォームを含むweb ページに存在します。
* フォームは30分のセッション内に送信されます。

次の場合、[!DNL Marketo Measure]は宛先Google Analytic コンバージョンを無視します。

* ボットは、web サイトでフォームを送信します（通常、これらのボットはクライアントのCRMにフォームを送信しません）。
* ユーザーは、最初のフォーム送信後に、さらにフォームを送信します。 [!DNL Marketo Measure]は、そのセッションからの最初のコンバージョンのみをプッシュします。
* ユーザーはフォーム送信を複数回クリックします。 [!DNL Marketo Measure]は、最初のフォーム送信のみを考慮します。
* ユーザーは「ありがとうございます」ページを複数回リロードします。
* ユーザーは広告ブロッキングツールを使用しています。

GAと[!DNL Marketo Measure]の間には、コンバージョンが何であるかについての基本的な違いがあることがわかります。 したがって、コンバージョン数とフォームのタッチポイント数が異なる可能性があります。
