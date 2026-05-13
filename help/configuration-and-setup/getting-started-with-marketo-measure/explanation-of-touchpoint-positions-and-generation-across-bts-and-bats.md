---
description: BTとBAT間のタッチポイントの位置と生成の説明 –  [!DNL Marketo Measure]
title: BT と [!DNL BATs] にわたる Touchpoint の位置と生成の説明
exl-id: 4903f917-a366-4767-a126-5216d2377399
feature: Touchpoints
TQID: https://experienceleague.adobe.com/MrUpDP1i5V-j2RzGmndOxMf8V4qw86pVlkVR29JGCgU
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 792
ht-degree: 3%

---

# BTおよび[!DNL BATs]間のタッチポイントの位置と生成の説明 {#explanation-of-touchpoint-positions-and-generation-across-bts-and-bats}

**バイヤージャーニーを通じたタッチポイントのポジションとフローの生成**

Buyer Touchpointの位置とそのトリガー方法を理解することは、[!DNL Marketo Measure] データを使用してレポートを正常に作成するために重要です。 見込み客がバイヤーズジャーニーを進む中で何をしたか、そしてタッチポイントデータでどのような表示になるかを明確に把握する必要があります。 このトピックに関する詳細なコンテキストについては、[[!UICONTROL &#x200B; タッチポイント生成とマッピング &#x200B;]](/help/configuration-and-setup/getting-started-with-marketo-measure/touchpoint-generation-and-mapping.md)記事を確認することをお勧めします。

[!DNL Marketo Measure]には、バイヤーズジャーニーの様々なステップによってトリガーされる、様々なタッチポイントのポジションがあります。 [!DNL Marketo Measure] データに関するレポートには、Buyer Touchpoints （BT）とBuyer Attribution Touchpoints （BAT）の2つのタッチポイントデータがあります。 これらのデータセットは、オブジェクトに関連する位置が少し異なります。 このトピックに関する詳細なコンテキストについては、[購入者のタッチポイント （BT）と購入者のアトリビューションのタッチポイント （BAT）の違い](/help/configuration-and-setup/getting-started-with-marketo-measure/difference-between-buyer-touchpoints-and-buyer-attribution-touchpoints.md)の記事を確認することをお勧めします。

**購入者の顧客接点（BT）**：これらは、個人とそのジャーニーに関連付けられた顧客接点であり、その個人に固有です。 Buyer Touchpointのデータをもとに、次のようなレポートを作成できます。

* [!DNL Marketo Measure] 101: ID別リード
* [!DNL Marketo Measure] 101: チャネル別リード
* [!DNL Marketo Measure] 101: リード/取引先責任者（ID）
* [!DNL Marketo Measure] 101: チャネル別リード/取引先責任者

次に、Buyer Touchpointの役職の概要を示します。この役職では、個人がジャーニーのどの段階にいるのか、その役職を獲得するためにどのような行動を取ったのかを把握できます。

<table> 
 <tbody>
  <tr>
   <th>Buyer Touchpoint（BT）ポジション</th> 
   <th>タッチポイントタイプ（タッチポイントをトリガーできるアクション）</th> 
   <th>タッチポイントの説明</th> 
  </tr>
  <tr>
   <td>ファーストタッチ（FT）</td> 
   <td>ウェブ訪問</td> 
   <td>個人が企業と最初に接するマーケティング上のインタラクション</td> 
  </tr>
  <tr>
   <td>リード作成（LC）</td> 
   <td>フォーム入力<strong>または</strong> キャンペーン/プログラムのインクルード</td> 
   <td>最初のフォームは、個人が持つフォームです（通常はフォーム送信ですが、キャンペーン/プログラムのインクルージョンにもできます）</td> 
  </tr>
  <tr>
   <td>Post LC</td> 
   <td>フォーム入力<strong>または</strong> キャンペーン/プログラムのインクルード</td> 
   <td>個人がLC （またはその後のキャンペーン/プログラムのインクルージョン）の後に完了したフォーム</td> 
  </tr>
 </tbody>
</table>

**購入者アトリビューションタッチポイント（BATS）**：これらは、商談とそのジャーニーに関連付けられているタッチポイントです。 これらの顧客接点は、商談とその連絡先に接続されているため、収益に接続されています。 Buyer Attribution Touchpointのデータをもとに、次のようなレポートを作成できます。

* [!DNL Marketo Measure] 101: ID別の商談
* [!DNL Marketo Measure] 101: ID チャネル別の商談

<table> 
 <tbody>
  <tr>
   <th>Buyer Attribution Touchpoint（BAT）ポジション</th> 
   <th>タッチポイントタイプ（タッチポイントをトリガーできるアクション）</th> 
   <th>タッチポイントの説明</th> 
  </tr>
  <tr>
   <td>ファーストタッチ（FT）</td> 
   <td>ウェブ訪問</td> 
   <td>コンタクトが自社と最初に行ったマーケティング上のインタラクション</td> 
  </tr>
  <tr>
   <td>リード作成（LC）</td> 
   <td>フォーム入力<strong>または</strong> キャンペーン/プログラムのインクルード</td> 
   <td>連絡先が最初に入力したフォーム（通常はフォーム送信ですが、キャンペーン/プログラムのインクルージョンにもできます）</td> 
  </tr>
  <tr>
   <td>機会の創出</td> 
   <td>フォーム入力<strong>または</strong> Web訪問<strong>または</strong> キャンペーン/プログラムの包含</td> 
   <td>商談が創出されたタイミングに最も近いマーケティングインタラクション</td> 
  </tr> 
  <tr>
   <td>クローズ済み/失注</td> 
   <td>フォーム入力<strong>または</strong> Web訪問<strong>または</strong> キャンペーン/プログラムの包含</td> 
   <td>商談が成約に最も近いマーケティングインタラクション（成約または失注）</td> 
  </tr>
  <tr>
   <td>ミドルタッチ</td> 
   <td>フォーム入力<strong>または</strong> キャンペーン/プログラムのインクルード</td> 
   <td>連絡先がオンラインフォームに入力し、それがマイルストーンの顧客接点と一致しない場合</td> 
  </tr>
 </tbody>
</table>

[!DNL Marketo Measure]には、個人のジャーニーと商談を明確に理解するために、2つのタッチポイントデータが含まれています。 このふたつのタッチポイントデータセットにより、funnelの上部からfunnelの下部にかけて何が起こったのかを明確に把握できます。

次の例は、Buyer Touchpoints （BT）からBuyer Attribution Touchpoints （BAT）へのデータの流れを示しています。 この例では、人物Aと人物Bは、作成日が2020年3月7日で、終了日が2020年6月5日の同じ商談の一部です。

**人物A** Buyer Touchpoint データセット

* ファーストタッチ（FT） – 有料検索.AdWords - 9/1/2019
* リードジェネレーション（LC） – オーガニック検索。Google - 2019年11月20日
* Post LC （フォーム入力） – ウェビナー – 2020年3月4日

**人物B** Buyer Touchpoint データセット

* ファーストタッチ（FT） – ペイドソーシャル.Facebook - 8/26/2019
* リードジェネレーション（LC） – オーガニック検索.Yahoo - 2/20/2020
* Post LC （フォーム入力） - Email - 5/1/2020

**商談** Buyer Attribution Touchpoint データは次のように読まれます…

* ファーストタッチ（FT） – ペイドソーシャル.Facebook - 8/26/2019
   * （アカウント/商談に対する&#x200B;_ファーストタッチ_&#x200B;があるため、**人物B**&#x200B;から）
* リードジェネレーション（LC） – オーガニック検索。Google - 2019年11月20日
   * （**人物A**&#x200B;から、アカウント/商談に対して真の&#x200B;_リード作成_&#x200B;を持っているため）
* 商談作成（OC） – ウェビナー – 2020年3月4日
   * （2020年3月7日に作成された商談に対する最も最近のインタラクションが&#x200B;**人物A**&#x200B;からのLC後のタッチポイントは&#x200B;_OC タッチポイント_&#x200B;になります）
* クローズ済み – メール - 2020年5月1日
   * （2020年5月6日に商談がクローズされたのは最新のインタラクションであるため、**人物B**&#x200B;からのLC後のタッチポイントは&#x200B;_クローズ済み顧客接点_&#x200B;になります）
