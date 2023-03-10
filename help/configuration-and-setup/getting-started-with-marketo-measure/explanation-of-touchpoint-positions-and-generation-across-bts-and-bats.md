---
description: BT と BAT に関するタッチポイントの位置と世代の説明 — [!DNL Marketo Measure]  — 製品ドキュメント
title: BT と [!DNL BATs]
exl-id: 4903f917-a366-4767-a126-5216d2377399
source-git-commit: b910e5aedb9e178058f7af9a6907a1039458ce7a
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 2%

---

# BT と [!DNL BATs] {#explanation-of-touchpoint-positions-and-generation-across-bts-and-bats}

**バイヤージャーニーでのタッチポイントポジションの生成とフロー**

購入者のタッチポイントの位置と、それらがどのようにトリガーされるかを理解することが、を使用して正常にレポートする上で重要です。 [!DNL Marketo Measure] データ。 見込み客が購入者のジャーニーを通じて何をしたかを明確に把握し、さらにタッチポイントデータでどのように表示されるかを把握したい場合があります。 このトピックの詳細については、 [[!UICONTROL タッチポイントの生成とマッピング]](/help/configuration-and-setup/getting-started-with-marketo-measure/touchpoint-generation-and-mapping.md) 記事。

[!DNL Marketo Measure] には、購入者のジャーニーの様々なステップでトリガーされる様々なタッチポイントの位置があります。 次のレポートを作成する場合： [!DNL Marketo Measure] データには、タッチポイントデータとして、バイヤータッチポイント (BT) とバイヤー属性タッチポイント (BAT) の 2 組があります。 これらのデータセットは、異なるオブジェクトに関連するので、位置がわずかに異なることに気が付くかもしれません。 このトピックの詳細については、 [購入者タッチポイント (BT) と購入者アトリビューションタッチポイント (BAT) の違い](/help/configuration-and-setup/getting-started-with-marketo-measure/difference-between-buyer-touchpoints-and-buyer-attribution-touchpoints.md) 記事。

**購入者タッチポイント (BT)**:これらは、個人とそのジャーニーに関連付けられたタッチポイントで、その個人に固有のものです。 すぐに使用できる次のレポートは、購入者タッチポイントデータから作成されます。

* [!DNL Marketo Measure] 101:リード — ID 別
* [!DNL Marketo Measure] 101:リード — チャネル別
* [!DNL Marketo Measure] 101:リード/連絡先 — ID 別
* [!DNL Marketo Measure] 101:チャネル別のリード/連絡先

次に、購入者タッチポイントのポジションの概要を示します。これは、個人がジャーニーでどこにいるか、およびそのポジションを獲得するためにとったアクションを示します。

<table> 
 <tbody>
  <tr>
   <th>購入者タッチポイント (BT) の位置</th> 
   <th>タッチポイントタイプ ( タッチポイントをトリガーできるアクション )</th> 
   <th>タッチポイントの説明</th> 
  </tr>
  <tr>
   <td>ファーストタッチ（F）</td> 
   <td>ウェブ訪問</td> 
   <td>個人がブランドと最初にやり取りするマーケティングインタラクション</td> 
  </tr>
  <tr>
   <td>リード作成（LC）</td> 
   <td>フォーム入力 <strong>または</strong> キャンペーン/プログラムの追加</td> 
   <td>個人が最初に入力するフォーム（通常はフォーム送信ですが、キャンペーン/プログラムを含めることもできます）</td> 
  </tr>
  <tr>
   <td>Post LC</td> 
   <td>フォーム入力 <strong>または</strong> キャンペーン/プログラムの追加</td> 
   <td>個人のフォームは、その LC（または後続のキャンペーン/プログラムを含む）の後に完了します。</td> 
  </tr>
 </tbody>
</table>

**購入者の属性タッチポイント (BATS)**:これらは、オポチュニティとそのジャーニーに関連付けられたタッチポイントです。 これらのタッチポイントは、商談とその連絡先に関連付けられるので、売上高に関連付けられます。 すぐに使用できる次のレポートは、購入者の属性タッチポイントデータから作成されています。

* [!DNL Marketo Measure] 101:ID 別の商談
* [!DNL Marketo Measure] 101:ID チャネル別の商談

<table> 
 <tbody>
  <tr>
   <th>購入者の属性タッチポイント (BAT) の位置</th> 
   <th>タッチポイントタイプ ( タッチポイントをトリガーできるアクション )</th> 
   <th>タッチポイントの説明</th> 
  </tr>
  <tr>
   <td>ファーストタッチ（F）</td> 
   <td>ウェブ訪問</td> 
   <td>連絡先がブランドとの最初のマーケティングインタラクション</td> 
  </tr>
  <tr>
   <td>リード作成（LC）</td> 
   <td>フォーム入力 <strong>または</strong> キャンペーン/プログラムの追加</td> 
   <td>連絡先が持つ最初のフォーム入力（通常はフォーム送信ですが、キャンペーン/プログラムを含めることもできます）</td> 
  </tr>
  <tr>
   <td>商談の作成</td> 
   <td>フォーム入力 <strong>または</strong> ウェブ訪問 <strong>または</strong> キャンペーン/プログラムの追加</td> 
   <td>商談が作成されたときに最も近いマーケティングインタラクション。</td> 
  </tr> 
  <tr>
   <td>クローズ済みの獲得/損失</td> 
   <td>フォーム入力 <strong>または</strong> ウェブ訪問 <strong>または</strong> キャンペーン/プログラムの追加</td> 
   <td>商談がクローズされた（獲得または失われた）ときに最も近いマーケティングインタラクション</td> 
  </tr>
  <tr>
   <td>ミドルタッチ</td> 
   <td>フォーム入力 <strong>または</strong> キャンペーン/プログラムの追加</td> 
   <td>連絡先がオンラインフォームに入力し、マイルストーンタッチポイントと一致しない場合</td> 
  </tr>
 </tbody>
</table>

[!DNL Marketo Measure] には、個人のジャーニーと商談を明確に理解するために、この 2 組のタッチポイントデータが用意されています。 これら 2 つのタッチポイントデータセットを使用すると、ファネルの上からファネルの下までの出来事を明確に把握できます。

次の例は、購入者タッチポイント (BT) から購入者属性タッチポイント (BAT) へのデータのフローを示しています。 この例では、「Person A」と「Person B」は共に、「Created Date」が3/7/2020、「Close Date」が5/6/2020の同じ商談の一部です。

**担当者 A** 購入者タッチポイントデータセット

* ファーストタッチ (FT) — 有料検索.AdWords - 9/1/2019
* リード作成 (LC) — オーガニック検索。Google - 11/20/2019
* Post LC（フォームの入力） — ウェビナー — 3/4/2020

**ユーザー B** 購入者タッチポイントデータセット

* ファーストタッチ (FT) — 有料 Social.Facebook- 8/26/2019
* リード作成 (LC) — オーガニック検索.Yahoo - 2/20/2020
* Post LC（フォームの入力） - Email-5/1/2020

**商談** 購入者の属性タッチポイントデータは次のように読み取られます。

* ファーストタッチ (FT) — 有料 Social.Facebook- 8/26/2019
   * （から） **ユーザー B** 彼らは真実を持っているので _ファーストタッチ_ （顧客/商談）
* リード作成 (LC) — オーガニック検索。Google - 11/20/2019
   * （から） **担当者 A** 彼らは真実を持っているので _リードの作成_ （顧客/商談）
* 商談の作成 (OC) — ウェビナー — 3/4/2020
   * (Post LC タッチポイント： **担当者 A** は _OC タッチポイント_ これは、商談の作成に必要な最新のインタラクションだったため、3/7/2020)
* 獲得 — メール — 5/1/2020
   * (Post LC タッチポイント： **ユーザー B** は _クローズ済みの獲得タッチポイント_ これは、商談がクローズされる最新のインタラクションであったため、5/6/2020)
