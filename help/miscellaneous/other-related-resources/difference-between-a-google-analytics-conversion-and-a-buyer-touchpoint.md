---
unique-page-id: 18874648
description: Google Analyticsコンバージョンと購入者タッチポイントの違い — [!DNL Marketo Measure]  — 製品ドキュメント
title: Google Analytics コンバージョンと Buyer Touchpoint の違い
exl-id: d09d963c-3207-467c-852a-d1edd49511fa
feature: Touchpoints
source-git-commit: 8ac315e7c4110d14811e77ef0586bd663ea1f8ab
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 4%

---

# Google Analytics コンバージョンと Buyer Touchpoint の違い {#difference-between-a-google-analytics-conversion-and-a-buyer-touchpoint}

詳細を見る [!DNL Google Analytics (GA)] 目標は、および購入者タッチポイントとの差別化方法です。

**Google Analyticsのコンバージョンとは**

[!UICONTROL Google Analytics] コンバージョンは、特定の Web サイトでのマーケターまたは Web 開発者が「目標」達成をコードする方法によって完全に決定されます。 Googleの目標は、「（e コマースサイトの）購入、（モバイルゲームアプリの）ゲームレベルの完了、（マーケティングやリードジェネレーションサイトの）連絡先情報フォームの送信」と考えることができます。 ほとんどの場合、マーケターは、情報フォームに記入した人物として目標/コンバージョンを確認します。

ただし、目標をコード化して特定の動作を管理することはできません。 Web 開発者が設定できる目標タイプがあります。 次に、その例を示します。

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
   <td><p>宛先</p></td> 
   <td>特定の場所が読み込まれます</td> 
   <td><em>ご登録いただき、ありがとうございます。</em> web ページまたはアプリ画面</td> 
  </tr> 
  <tr> 
   <td>期間</td> 
   <td>特定の時間以上持続するセッション</td> 
   <td>サポートサイトに 10 分以上滞在した</td> 
  </tr> 
  <tr> 
   <td>セッションあたりのページ数/画面数</td> 
   <td>ユーザーが特定の数のページまたは画面を表示する</td> 
   <td>5 ページまたは画面が読み込まれました</td> 
  </tr> 
  <tr> 
   <td>イベント</td> 
   <td>イベントとして定義されたアクションがトリガーされる</td> 
   <td>ソーシャルレコメンデーション、ビデオ再生、広告クリック</td> 
  </tr> 
 </tbody> 
</table>

ほとんどのマーケターは、変換結果を「宛先の目標」として設定します。つまり、通常、正式なコンバージョンと見なすためのフォームの後に「ありがとうございます」ページを作成します。

つまり、Googleでは「ありがとうございます」ページの表示をコンバージョンと見なします。 Google Analyticsの観点から見ると、これはほとんどのマーケターが満足できるものです。

ただし、購入者のタッチポイントの動作は非常に異なります。

**購入者のタッチポイントの違いは何ですか。**

[!DNL Marketo Measure] JavaScript は、特定のサイトのすべての形式でセッションデータとフォーム送信を追跡します。 の目標をコーディングする必要はありません。 [!DNL Marketo Measure] 視点。 このプロセスは自動的に実行されます。 フォーム送信の場合、 [!DNL Marketo Measure] は、匿名ユーザーが特定のフォームの情報フィールドに入力し、さらにフォーム送信ボタンをクリックするたびに、フォーム入力をレポートします。 [!DNL Marketo Measure] は、フォームの送信を記録するためのありがとうページを必要としません。

[!DNL Marketo Measure] は、次の場合にフォームタッチポイントを作成します。

* これらのコンバージョンに関連付けられたリード/連絡先が CRM に表示されます。
* The [!DNL Marketo Measure] JS がフォームを含む Web ページに存在する。
* 30 分以内にフォームが送信されます。

[!DNL Marketo Measure] は、次の場合に宛先Google Analytics の変換を無視します。

* ボットは、Web サイト上のフォームを送信します（これらのボットは通常、クライアントの CRM に送信しません）。
* ユーザーが最初のフォーム送信後に送信するフォームの数が増えました。 [!DNL Marketo Measure] は、そのセッションからの最初のコンバージョンのみをプッシュします。
* ユーザーがフォーム送信を複数回クリックします。 [!DNL Marketo Measure] は最初のフォーム送信のみを考慮します。
* ユーザーが、「ありがとうございます」ページを複数回再読み込みします。
* ユーザーが任意の広告ブロックツールを使用している。

ご覧のように、GA と [!DNL Marketo Measure] コンバージョンがであると考えます。 したがって、コンバージョンの数とフォームのタッチポイントの数が異なる可能性が非常に高くなります。
